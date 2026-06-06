# S1-CL2 Cloud Disaster Recovery — Scenario Design

> **STATUS: DRAFT — design capture.** This document records what has been **agreed** (Tim's direction) and what remains **TBD** for the two CL2 scenario projects: the **LMS** (assessment) and the **Accounting / Ledgerline** system (practice). It's a design/spec document — *not* in-world intranet content — so it uses assessment/UoC language freely. The website project doc-sets get built **from** this. Companion: the cluster's `consolidated_uoc.md` (topic → group → AT mapping) in `../S1-CL2-Cloud-Disaster-Recovery/`.

Markers: **[AGREED]** = confirmed with Tim · **[TBD]** = proposal / not yet confirmed · **[VERIFY]** = factual claim to confirm before it lands in a student-facing doc.

---

## 1. Relationship to Cluster 1

- **[AGREED]** The CL1 projects (the LMS cloud migration + the Accounting cloud migration) are **completed and closed** in-world. In the CL2 (and CL3) website states they are shown as finished/archived.
- **[AGREED]** CL2 runs as **new projects** — a fresh engagement each, with their own full project-doc sets, appearing in the new website states (`s1-cl2-at1`, `s1-cl2-at2`).
- **Timeline continuity:** CL1 migrated the LMS to the cloud (AT2) and made it highly available, single-region cross-AZ (AT3). CL2 is where **multi-region / DR** lives — the depth deliberately deferred from CL1 to CL2.

---

## 2. The cluster narrative spine — the inciting event

- **[AGREED]** At the start of CL2, **YAT announces a strategic partnership / offshore campus in India** — anchored on **GIFT City, Gujarat** (the Special Economic Zone where Deakin and the University of Wollongong have opened campuses; Swinburne Sarawak and RMIT Vietnam are the same TNE pattern). **A single primary partner** — no multiple partners; the added complexity isn't right for Diploma level.
- **Consequence that drives the units:** YAT's systems must now serve an **offshore/global user base**, be **resilient across regions**, and be **provisioned repeatably**. One event motivates all three units:

| Unit | What the offshore partnership gives it |
|---|---|
| **ICTCLD503** (web-scale) | A genuine **global user base** + global reach (latency, CDN, scale-out as the partner's students come online). |
| **ICTCLD501** (DR) | The infrastructure becomes **business-critical across borders** + multi-region — DR, RTO/RPO and cross-border data-residency now matter. |
| **ICTCLD505** (IaC) | The canonical IaC motivation — **stand up the same stack in a second region, as code**. |

- **[AGREED]** Depth is **"serve multiple regions," not "replicate data multi-region."** The UoC is met by global *serving* (CDN/edge/read replicas) + a DR *plan* + *parameterised* IaC — none of which require live multi-region data replication. This also right-sizes the complexity and largely de-risks the AWS Academy single-region constraint (the hard multi-region content is **designed / planned / templated**, not necessarily run live).

---

## 3. Assessment structure (recap — per Tim's direction)

- **[AGREED] AT1 — DR Plan** *(modelled on CL1 AT1 Business Case)* — **Part A** written DR plan (with appendices carrying the impact analysis, the web-scale/microservice **solution design**, and KE) + **Part B** a **presentation of the DR plan for approval** (the design-approval gate — approval before implementing; carries ICTCLD501's verbal walkthrough + sign-off).
- **[AGREED] AT2 — DR Implementation** *(modelled on CL1 AT2 Deployment Report)* — **single part**: a written **Deployment Report** for finalisation/approval of the build (microservice implementation, IaC, monitoring, IaC user docs, build sign-off).
- Full item-level mapping lives in `consolidated_uoc.md`.

---

## 4. Project 1 — LMS (the **ASSESSMENT** scenario)

**Continuity:** the same LMS CL1 migrated and made HA. CL2 extends it to serve the India campus.

**Scope for CL2:**
- **503 — re-architect for web-scale / global reach:** CloudFront/edge caching, read replicas, auto-scaling, serve India users at acceptable latency.
- **503 — microservice carve-out [AGREED]:** a **webhook-driven, serverless, append-only audit/access-log microservice**. It ingests LMS access/activity events via a **generic webhook** (the LMS is just an example producer — no live LMS or LMS docs needed) and writes the **CERT-In logs to an India-resident store**. Designing the webhook payload contract *is* the assessed task (`[ICTCLD503 PC 2.1]`); standalone-testable with sample events. Components: webhook → SQS/SNS → Lambda → DynamoDB/S3.
- **501 — DR plan** for the now-business-critical, multi-region LMS: risk/impact analysis, RTO/RPO, recovery to a second region (backup-and-restore or pilot-light, **planned and evaluated** — not necessarily implemented live).
- **505 — parameterised IaC** to provision the LMS infrastructure with **region as a parameter** ("stand up the India footprint as code").

**Data-residency driver (LMS):**
- **[VERIFY]** **DPDP Act 2023 + DPDP Rules 2025** — *permissive* "negative list" model: Indian personal data may be transferred abroad by default. So the bulk of LMS data **can stay in Australia**.
- **[VERIFY]** **CERT-In Directions 2022** — operational **logs must be retained in India for 180 days** (+ 6-hour breach reporting). This is the genuine localisation hook for the LMS.
- **Architectural answer:** primary AU region; global reach via CloudFront; the **audit-log microservice ships the India-cohort access logs to an India-resident store** (CERT-In); main database stays in AU (DPDP permits). DR to a second region. *(Lab: primary `us-east-1` = AU; India store on the `us-west-2` stand-in — see §9.1.)*

---

## 5. Project 2 — Accounting / Ledgerline (the **PRACTICE** scenario)

**Continuity:** Ledgerline from CL1 — the practice system students rehearse on before being assessed on the LMS. **It is a bookkeeping / general-ledger system used by internal finance staff — NOT a payment gateway** (it may *integrate* with gateways, but it records transactions; it doesn't process payments).

**Scope for CL2 (practice — teach → practice in delivery):**
- **501 — DR plan** for the financial system. A financial/accounting system is the canonical DR case (regulatory exposure, tight RTO/RPO) — a strong practice vehicle.
- **505 — parameterised IaC** to provision the **India backup target**.
- **503 — microservice IS exercised; web-scale-*serving* is not.** The **same audit-log microservice** runs here with **transaction payloads**: each relevant Ledgerline transaction → webhook → an **immutable audit record on the India store** (financial audit trail / Companies Act). Real practice on the 503 **microservice design + serverless deploy** (`PC 2.x`, `3.x`, `PE 2/3`). The **global-serving half** of 503 (CDN / global user base) is *not* exercised by an internal bookkeeping system — that stays LMS-only.

**Data-residency driver (Accounting) — different instrument by design:**
- **[AGREED]** **RBI is the wrong hook** — RBI's payment-data localisation binds *payment-system operators / gateways*. The Indian gateway localises payment data locally; Ledgerline's ledger is general bookkeeping, not payment-system data. A student *should* be able to reason this out.
- **[VERIFY]** The real driver on the **books of account** is **India's Companies Act / Companies (Accounts) Rules** — an Indian entity keeping books in electronic mode must keep a **daily backup on servers physically located in India** (even if the primary system sits abroad), and keep them accessible from India. *(Hinges on **[TBD]** YAT-India being an Indian legal entity — e.g. a GIFT City subsidiary — whose books fall under the Act.)*
- **Architectural answer:** books **primary in AU**, with a **daily cross-region backup to AWS Mumbai (`ap-south-1`)** — a **backup-and-restore DR tier** (RPO ≈ 24h; RTO = restore time). Mechanisms: RDS cross-region snapshot copy / S3 Cross-Region Replication / AWS Backup cross-region copy. The Companies Act sets the floor (daily); the DR plan decides whether that floor meets the business's recovery objectives.

---

## 6. Why two different legal drivers — the practice↔assessment contrast

This is deliberate, and it's the mechanism that stops students pattern-matching practice onto assessment. **Same competency, different correct answer:**

| | Practice — Accounting / Ledgerline | Assessment — LMS |
|---|---|---|
| **Driver** | Companies Act — *books of account* | CERT-In — *operational logs* |
| **Bound data** | the ledger / database | the 180-day logs |
| **Design answer** | replicate the **datastore** to an India region (daily) | ship **logs** to an India store; main DB can stay in AU (DPDP permits) |
| **Audit-log microservice (503)** | same engine, **transaction-audit payloads** → India store | same engine, **access-log payloads** → India store |
| **Underlying skill (shared)** | identify the residency-bound slice → provision an India target → wire up the replication/backup → feed the audit microservice |

The **audit-log microservice is one design, taught once, run in both** — only the webhook payload differs (transaction records vs access events). It also sits *beside* the primary-data DR backup: the **books / LMS DB** go via the cross-region backup (501/505); the **audit/log slice** goes via the microservice (503). Two slices, two mechanisms, both landing in India.

A student who practised "replicate the database to Mumbai" can't transplant it onto the LMS, where the database largely *doesn't* move — it's the logs that must. They have to identify the applicable instrument and design from it. That's transfer-of-learning, and it's the "questions in context, not abstract recall" principle.

---

## 7. Data-residency approach

- **[AGREED, approach]** **Option 2 — provide mock "Data Residency & Sovereignty Requirements" docs** (one per project), **grounded in the real instruments** (DPDP, CERT-In, Companies Act) but simplified/sharpened to create exactly the constraints the scenario needs.
  - *Why not Option 1 (students research the raw law):* the real DPDP regime is permissive — a sharp student could correctly conclude "no India footprint needed," collapsing the scenario; and the framework is too tangled to assess consistently. The UoC wants students to *work with* legislative requirements as an **input**, not research them.
  - Students may still be pointed at the real instruments as **background reading** (exercises Reading FS + legislative-requirements exposure) — but the assessment rests on the controlled requirements doc, so everyone designs against the same constraints.
- **[TBD] Residency dial = "light"** — park a *defined, bounded* slice of data in India (LMS: logs; Accounting: the books backup), designed + templated, not full multi-region replication.

---

## 8. Website build-out (downstream of this doc)

- **[AGREED]** In the `s1-cl2-*` / `s1-cl3-*` states, the **CL1 projects are marked completed/closed**.
- **[AGREED]** Create **two new CL2 projects** with **full project-doc sets**, appearing in the appropriate CL2 states. Each parallels the CL1 project-doc pattern. **[TBD]** project slugs/names (draft-naming pragmatism — defer).
- **Per-project doc set (to author — parallels CL1):**
  - Engagement / MSA + **role brief** (the offshore-expansion brief)
  - **Functional & non-functional requirements** (web-scale + global reach; DR/RTO-RPO; IaC)
  - **Audit-log microservice brief** (the business need + "triggered by a generic webhook"; the student designs the payload contract)
  - **Data Residency & Sovereignty Requirements** (the mock, grounded doc — §7)
  - **Consultation notes** (stakeholder interview about the India expansion)
  - **Architecture / design inputs** as needed (current-state of the CL1-hardened LMS; Ledgerline current state)
  - Cost / SLA inputs as relevant
- **State-versioned ICT docs** (network diagram, environment overview, etc.) fork into a CL2 state reflecting the post-CL1, pre-expansion baseline.

---

## 9. Open items / risks (must resolve before authoring student-facing artefacts)

1. **[RESOLVED — approach agreed] AWS Academy region lock + cross-region simulation.** Verified 2026-06-06: the Learner Lab (Foundation Services) restricts access to **`us-east-1` + `us-west-2` only** — Mumbai (`ap-south-1`) is unavailable, and **RDS Multi-AZ is not supported**. **Approach:** *simulate* the cross-region architecture using **`us-west-2` as the stand-in for India (`ap-south-1`)** — primary in `us-east-1`, cross-region backup/DR to `us-west-2`. The **cross-region mechanics are built live** (RDS cross-region snapshot copy / S3 CRR / AWS Backup all work between the two allowed regions) — so this is hands-on, not design-only. **Acknowledged-simulated:** the geography/latency (Oregon ≠ India) and RDS Multi-AZ (in-region DB HA stays design-only; cross-region *snapshot copy* works). **Genuinely real:** CloudFront's global edge reach (503's "global user base" is not simulated). The **IaC parameterises `region`** — `ap-south-1` in the design/production intent, `us-west-2` in the lab — which is exactly what `[ICTCLD505 PC 3.5]` assesses. Student deliverables must **label the substitution** (target = India/`ap-south-1`; implemented in lab as `us-west-2`). **[TBD]** confirm Kangan's exact lab product matches Foundation Services (15-min smoke test / lab guide).
2. **[VERIFY] Legal wording** — confirm the Companies Act books-of-account India-backup rule and the CERT-In log-retention specifics before they go into the requirements docs. (Keep regulatory detail illustrative, not a law exam.)
3. **[RESOLVED]** Microservice (503) = a **webhook-driven serverless append-only audit/access-log service** — LMS access logs (CERT-In) for assessment; Ledgerline transaction-audit records (Companies Act) for practice. Same engine, different payloads.
4. **[PARTIALLY RESOLVED]** The 503 **microservice** is now practised on Ledgerline (the audit service). Only the **global-serving / web-scale half** of 503 still needs a practice vehicle — taught worked-examples + an AWS lab sample web app. **[TBD]**
5. **[TBD]** Confirm the **"light" residency dial**.
6. **[TBD]** New project **slugs / naming**.
7. **[TBD]** GIFT City / IFSCA specifics — use GIFT City as the *narrative anchor*; don't build the data rules on IFSCA's niche special-zone regime.

---

## 10. Decision log (this session, 2026-06-06)

- Offshore-India partnership as the cluster spine; single primary partner (GIFT City). **[AGREED]**
- LMS = assessment scenario (goes global); Accounting/Ledgerline = practice parallel. **[AGREED]**
- "Serve multiple regions," not multi-region data replication. **[AGREED]**
- Ledgerline is bookkeeping, not a payment gateway; residency driver = Companies Act (books backup to India), not RBI. **[AGREED]**
- Architecture: AU-primary + daily backup to AWS Mumbai (`ap-south-1`). **[AGREED]**
- CL1 projects closed; CL2 = new projects with full doc sets. **[AGREED]**
- Two different legal drivers (Companies Act vs CERT-In) as the deliberate practice↔assessment contrast. **[AGREED]**
- Data residency via Option 2 (mock, grounded in real law), "light" dial. **[AGREED approach / TBD dial]**
- Microservice (503) = webhook-driven serverless **append-only audit/access-log service**; same engine both projects (LMS access logs / Ledgerline transaction audit), different payloads. Gives Ledgerline a real 503 microservice to practise on; the LMS is just a generic webhook producer (no live LMS / LMS docs needed). **[AGREED]**
