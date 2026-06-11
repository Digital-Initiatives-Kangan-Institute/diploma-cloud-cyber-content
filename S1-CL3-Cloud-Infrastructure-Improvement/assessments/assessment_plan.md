# S1-CL3 Cloud Infrastructure Improvement — Cluster Assessment Plan

> **STATUS: DRAFT.** Turns the cluster's settled design into the spec the AT instruments are built from, with the coverage proof that every UoC item lands in an assessment.
>
> **What is settled** (discussed and approved with Tim, 2026-06-07):
> - The cluster is one integrated engagement — **lead a team to improve a cloud system's infrastructure** — combining **ICTCLD504** (the technical improve-cycle) and **BSBXTW401** (leading the team that does it).
> - **Three ATs in an individual → group → individual rhythm:** **AT1 (individual)** Engagement Setup · **AT2 (group)** Improvement Design + Approval · **AT3 (individual)** Implement. The rhythm keeps the evidence unambiguous per phase.
> - **Collaboration is assessed where it is real — the design (AT2)** — not the point-and-click implementation.
> - **Owned-dimension model:** each student owns one improvement dimension (security / reliability / scalability / cost) through AT2 (design it) and AT3 (implement it), giving individual 504 evidence inside a group effort.
> - **Team-leadership evidence:** each student **leads at least one team meeting** in AT2, captured by an **assessor observation checklist** (the primary performance evidence, incl. *managed a conflict*) + a **student reflection** appendix (secondary; carries the leadership KE). *How* the assessor stimulates a conflict is the assessor's conduct, out of the instrument's scope.
> - **Heavy reuse:** the improve-loop + lab-pack from **CL1 AT3**; the Solution Design + Deployment Report templates, instrument generators and scenario world from **CL2**.
>
> **What is TBD** (Rule 1/2): group size; the source-assessment reuse audit for 504/401; scenario specifics (project slug, role names). *(Vehicle resolved: CL3 **assesses on Ledgerline**, **practises on the website**, per `scenario-flow.md`; `[ICTCLD504 KE 6]` resolved — see §2.)*
>
> **Companion documents:** `consolidated_uoc.md` (every PC/FS/PE/KE/AC in 11 groups under 4 phases); `scenario/cluster-3-scenario-{assessment,practice}.md` + `scenario/scenario-flow.md`; `S1-CL2-.../assessments/assessment_plan.md` (the cluster this most closely parallels).

---

## 1. Integration approach

**Goal (as CL1/CL2):** one integrated cluster assessment that reads as a single engagement, not two units stapled together — a single scenario, a single team-lead voice, a single artefact thread.

**Shape:** the cluster runs as one continuous engagement — *analyse & set up → design & approve → implement & finalise* — with the student as **team lead** throughout. The two units interweave: **504 is the work** (improve the architecture); **401 is how it is run** (lead the team that does it). It is, in effect, **CL1 AT3's improve-loop widened** (security + reliability + scalability + cost, not only HA), **run by a team**, **on a different existing system**.

**The thread:**
- **AT1 (individual)** — each student sets up the engagement: authors the **team plan / Role Brief** (the leadership planning) and the **requirements & architecture analysis** (the technical analysis). These are the documents we currently *pre-populate* for the lower clusters — in CL3 the student-as-lead authors them.
- **AT2 (group)** — the team collaborates to **design the improvement**. Each student **owns one dimension** and **leads the meeting** on it; the team integrates the dimensions into one improved architecture, **presents it for the deploy sign-off**.
- **AT3 (individual)** — each student **implements, tests and finalises their dimension**.

**Two approval moments (UoC-faithful):** end of AT2 = **deploy sign-off** (`[ICTCLD504 PC 2.5]`); end of AT3 = **final sign-off** (`[ICTCLD504 PC 4.3]`).

**Knowledge evidence — contextual, on the student's own work:** the technical KE rides the analysis/design/deploy documents; the leadership KE (conflict resolution, teamwork challenges) rides the AT2 **reflection** appendix. No abstract recall.

---

## 2. Scenario

**Reuse the YAT world.** By CL3 YAT's systems are in the cloud; **Ledgerline** (the Accounting system) sits at a **single-AZ baseline** (on-prem in CL1 → migrated to single-AZ cloud by the end of CL1 → improved in CL3). The engagement: **improve Ledgerline's cloud infrastructure** for security, reliability, scalability and cost, with the student promoted to **MTS team lead** of the improvement team.

**Vehicle (per `scenario-flow.md`):** CL3 **assesses on Ledgerline** (single-AZ cloud — the "already in the cloud, now improve it" system) and **practises on the website** (students rehearse the improve-loop on the website before being assessed on Ledgerline). *(Forced by the no-leakage invariant: the website is assessed in CL2, so it cannot also be CL3's assessed system.)* **`[ICTCLD504 KE 6]`** (object storage for static web sites) is evidenced as a **contextual knowledge question** in AT2 — e.g. *"How does the accounting system differ from a system that needs to store objects such as images (for example, a website), and how would you provision that storage if it were needed?"* The student reasons by contrast from their own Ledgerline system; KE 6 is *knowledge*, so this evidences it cleanly without Ledgerline itself having to use static-web object storage.

**The team:** a **real student group** (the MTS improvement team). AT1 evidences each student's planning individually; AT2 is where the group collaborates and each student leads.

**Baseline:** Ledgerline's **current single-AZ cloud infrastructure** is supplied as a **baseline lab-pack** (the CL1 AT3 pattern, re-pointed at Ledgerline) — students analyse it, improve it, deploy and test the improvements.

---

## 3. Cluster assessment structure

| Component | Working title | Mode | Format | Unit focus |
|---|---|---|---|---|
| **AT1** | Engagement Setup | **Individual** | Engagement-setup pack (Role Brief / team plan + requirements & analysis) | **BSBXTW401** el 1 + **ICTCLD504** el 1 |
| **AT2** | Improvement Design & Approval | **Group** | Improvement Design (per-dimension) + led-meeting observation + reflection + approval presentation | **ICTCLD504** el 2 + **BSBXTW401** el 2–4 |
| **AT3** | Implementation | **Individual** | As-deployed Deployment Report (the student's dimension) | **ICTCLD504** el 3–4 |

**AT1 — Engagement Setup (individual).** Each student authors the engagement-setup documents a team lead produces at kickoff:
- **Team plan / Role Brief** — team objectives & responsibilities, per-member performance expectations and behaviours, accountability strategies, contingency plans, and the task allocation. → `[BSBXTW401 el 1]` + el 2 (allocate) + `[PE 1]`.
- **Requirements & architecture analysis** — review the supplied baseline, evaluate it and its business impact, weigh options, confirm decisions, and set the security/reliability/scalability/cost goals + performance metrics. → `[ICTCLD504 el 1]`.

**AT2 — Improvement Design & Approval (group).** The team designs the improved architecture across a series of working meetings.
- **Owned-dimension design** — each student designs the improvement for their dimension; the team integrates them into one architecture. → `[ICTCLD504 el 2]` (PC 2.1–2.3).
- **Led meetings** — each student leads/facilitates at least one meeting (on their dimension). The assessor records a **team-leadership observation checklist** (communicate objectives, allocate/instruct, facilitate collaboration, coach/support, resolve a task issue, **manage a conflict**). → `[BSBXTW401 el 2–3]`, `[PE 2, PE 5]`. **Primary** leadership evidence.
- **Reflection appendix** — each student reflects on 2 conflicts/challenges (what happened, how handled, learned, improve next time). → `[BSBXTW401 KE 5, KE 10]`, `[FS Interact with others]`. **Secondary/backup** evidence.
- **Performance review** — each student reviews the team's performance on their workstream (measure vs plan, feedback, development opportunities, action plans). → `[BSBXTW401 el 4]`, `[PE 3, PE 4]`.
- **Approval presentation** — the team presents the design for the **deploy sign-off**. → `[ICTCLD504 PC 2.4–2.5]`, `[FS Oral communication]`.

**AT3 — Implementation (individual).** Each student deploys their owned dimension's improvement to the lab, monitors/tests it against the metrics and goals, applies refinements, and documents the **as-deployed** result (changes vs the approved design + test results), describes a **long-term improvement strategy**, and obtains **final sign-off**. → `[ICTCLD504 el 3–4]`, `[PE 2, PE 4, PE 5]`.

**Template basis:** AT1's analysis + AT2's design reuse the **Solution Design** document type (CL2); AT3 reuses the **Deployment Report** type (CL2). The **team plan / Role Brief**, the **observation checklist** and the **reflection** appendix are new (BSBXTW401).

---

## 4. Authoring basis / provenance

**CL3 is the lightest cluster with the heaviest reuse.** The engagement workflow (analyse → design → approve → deploy → test → document → sign-off) is structurally CL1 AT3 + CL2, re-pointed at Ledgerline with a team-leadership overlay.

**Reusable / already proven:**
- **CL1 AT3** — the improve-an-existing-baseline shape + the **lab-pack standard** (`documentaion/lab-pack-standard.md`) for the supplied Ledgerline baseline.
- **CL2** — the **Solution Design** + **Deployment Report** templates and their generators; the Kangan **Project Assessment** instrument generators; the **scenario world** + intranet; the validators.

**New authoring (the ~30% that is CL3-specific):**
1. The **BSBXTW401 instruments** — the team plan / Role Brief template, the **led-meeting observation checklist**, the **reflection** appendix prompt, the performance-review template.
2. The **Ledgerline baseline lab-pack** (the current single-AZ cloud infra to improve).
3. The **Ledgerline scenario** context (the improvement engagement, the team-lead role).

**TBD:** if standalone source assessments for ICTCLD504 / BSBXTW401 surface, audit them for reusable practical tasks before finalising.

---

## 5. Group coverage map

Every group in `consolidated_uoc.md` (82 items) mapped to where it is covered.

| Group | Phase | Where | Mode | How evidenced |
|---|---|---|---|---|
| **G1** — Analyse cloud architecture (504 el 1) | 1 | **AT1** | individual | Requirements & architecture analysis of the supplied baseline. `504 PC 1.1–1.6`, `PE 1` (assess), `PE 3` (goals), `KE 1/2/3`. |
| **G2** — Plan team outcomes (401 el 1) | 1 | **AT1** | individual | Team plan / Role Brief — objectives, performance expectations, accountability, contingencies. `401 PC 1.1–1.4`, `KE 1/2/9`. |
| **G3** — Design & improve architecture (504 el 2) | 2 | **AT2** | group (owned dimension) | Per-dimension improvement design + integrated architecture + present + sign-off. `504 PC 2.1–2.5`, `PE 1` (improve), `KE 4/5/6/8/9`. |
| **G4** — Coordinate the team (401 el 2) | 1–2 | **AT1 + AT2** | individual / observed | Allocate tasks (AT1 plan, `PE 1`); communicate + facilitate collaboration (AT2 led meetings). `401 PC 2.1–2.4`, `KE 3/6/7`. |
| **G5** — Deploy, monitor & test (504 el 3) | 3 | **AT3** | individual | Deploy/monitor/test/refine the owned dimension. `504 PC 3.1–3.4`, `PE 2/4`, `KE 7/10`. |
| **G6** — Support the team (401 el 3) | 2 | **AT2** | observed + reflection | Led-meeting observation (coach, resolve issues, **manage conflict**) + reflection. `401 PC 3.1–3.4`, `PE 2/5`, `KE 4/5/8/10`. |
| **G7** — Finalise improvements (504 el 4) | 3 | **AT3** | individual | As-deployed report + long-term strategy + final sign-off. `504 PC 4.1–4.3`, `PE 5`. |
| **G8** — Monitor team performance (401 el 4) | 2 | **AT2** | individual | Performance review of the workstream team. `401 PC 4.1–4.4`, `PE 3/4`. |
| **G9** — Foundation skills | — | **all ATs (implicit)** | — | Co-evidenced across the deliverables, meetings and presentation; marking guides note where each is naturally evidenced. |
| **G10** — Assessment conditions: environment & resource access | — | **delivery env** | — | Provided by the scenario website + AWS Academy labs (cloud vendor, managed DB, console/CLI, IDE, SSH/RDP, requirements) + the simulated-environment condition. |
| **G11** — Assessment conditions: assessor requirements | — | **institutional** | — | Satisfied by the institution's assessor-qualification policy; one statement per AT cover sheet. |

**PE distribution check.** AT1: `504 PE 1` (assess), `504 PE 3`, `401 PE 1`. AT2: `504 PE 1` (improve), `401 PE 2/3/4/5`. AT3: `504 PE 2/4/5`. All 10 PE placed.

**KE distribution check.** AT1: `504 KE 1/2/3`; `401 KE 1/2/9`. AT2: `504 KE 4/5/6/8/9`; `401 KE 3/4/5/6/7/8/10`. AT3: `504 KE 7/10`. All 20 KE placed.

**Verification:** every group G1–G11 has a row; every PC, PE and KE is allocated; FS (G9) cross-cutting; AC is the environment (G10) + the institutional assessor condition (G11). No item is unaddressed.

---

## 6. Required authoring worklist

### AT1 — Engagement Setup
1. **Team plan / Role Brief template + exemplar** (NEW — BSBXTW401) — objectives, per-member performance expectations, accountability, contingencies, task allocation.
2. **Requirements & analysis exemplar** (504 el 1) — reuse the Solution Design document type, scoped to the analysis half.
3. **AT1 Student + Assessor instruments** (individual) — task, the authored-setup deliverable spec, marking guide with bidirectional UoC traceability.

### AT2 — Improvement Design & Approval
4. **Improvement Design exemplar** (504 el 2) — reuse the Solution Design type; owned-dimension structure.
5. **Led-meeting observation checklist** (NEW — BSBXTW401) — the leadership behaviours the assessor records, incl. *managed a conflict*.
6. **Reflection appendix prompt** (NEW) + **performance-review template** (NEW).
7. **Approval presentation** brief + observation/sign-off record (reuse CL2 Part C pattern).
8. **AT2 Student + Assessor instruments** (group) — group deliverable + the individual observation/reflection/review evidence.

### AT3 — Implementation
9. **As-deployed Deployment Report exemplar** (504 el 3–4) — reuse the Deployment Report type.
10. **AT3 Student + Assessor instruments** (individual).
11. **Assessor operational artefacts** — the **Ledgerline baseline lab-pack** (the current single-AZ cloud infra), provided as appendices / lab artefacts.

### Cluster-level
12. **`assessment_plan.md`** — this document.
13. **`mappings/`** — per-unit Assessment Mapping `.docx` (504, 401).
14. **Realign the scenario** (the Ledgerline improvement engagement, the MTS team-lead role).

---

## 7. Open questions / TBDs

1. **Vehicle** — **resolved:** assess on **Ledgerline** (single-AZ cloud), practise on the **website**, per `scenario-flow.md` (no-leakage). `[ICTCLD504 KE 6]` (object storage for static web sites) **resolved** — evidenced as a contextual knowledge question contrasting Ledgerline with an object-storage-dependent system (see §2).
2. **Team model specifics** — group size; how groups are formed; how each student's led meeting is scheduled/observed. TBD.
3. **BSBXTW401 source assessment** — if a standalone source surfaces, audit for reusable team-leadership tasks. TBD.
4. **504 / 401 verbatim transcription** — confirm the `_Complete_` `.md` are verbatim against the source `.docx` (Step-1 validation) before finalising instruments.
5. **Delivery practice vehicle** — **resolved:** the **website** is the CL3 practice vehicle (assessment is on Ledgerline). Delivery sequencing still TBD (delivery, not assessment).
6. **Pre-validation** — run the institutional Pre-Validation Tool over each AT before submission.

---

## 8. Critical-path next steps (if this plan is approved)

Not committed — natural sequencing only.

1. **Vehicle confirmed** — assess on Ledgerline, practise on the website (per `scenario-flow.md`).
2. **Author AT1** — the team plan / Role Brief template + exemplar and the requirements/analysis exemplar; derive the individual instruments.
3. **Author AT2** — the Improvement Design exemplar (owned-dimension); the **observation checklist** + **reflection** + **performance review**; the approval presentation; derive the group instruments.
4. **Author AT3** — the as-deployed Deployment Report exemplar; derive the individual instruments; build the **Ledgerline baseline lab-pack**.
5. **Realign the scenario** + generate the `mappings/` docs; build a UoC-coverage validator; run the Pre-Validation Tool.

---

## Changelog

- **2026-06-07:** Initial draft (v1). Built on the settled integrated design — *lead a team to improve a cloud system's infrastructure* — with the three-AT individual → group → individual rhythm (AT1 setup / AT2 group design / AT3 implement), the owned-dimension technical model, and the team-leadership evidence approach (led-meeting observation checklist + reflection + performance review). Coverage mapped across both units (all 80 items; 10 PE, 20 KE placed). Heavy reuse from CL1 AT3 (improve-loop + lab-pack) and CL2 (Solution Design + Deployment Report). Vehicle (website) and team-model specifics flagged TBD.
- **2026-06-08 (v2 — re-vehicled):** **Vehicle resolved per `scenario-flow.md`: CL3 assesses on Ledgerline (single-AZ cloud), practises on the website.** (v1 had the website as the system to improve; the no-leakage invariant moves *assessment* to Ledgerline since the website is assessed in CL2, and makes the website CL3's *practice* vehicle.) All vehicle context re-pointed website→Ledgerline (engagement, baseline lab-pack, scenario). **Structure, AT rhythm, coverage map and KE/PE distributions unchanged — only the subject system changed.** `[ICTCLD504 KE 6]` resolved — evidenced as a contextual knowledge question contrasting Ledgerline with an object-storage-dependent system (e.g. a website).
- **2026-06-11 (v3 — AC consistency):** Aligned the Assessment Conditions treatment with CL1/CL2. The trailing assessor-requirements clause in each unit is now tagged as that unit's last AC item (`[ICTCLD504 AC 8]`, `[BSBXTW401 AC 2]`) in `consolidated_uoc.md`, collected in a new **G11 — assessment conditions: assessor requirements** (mirroring CL2's G13). Item total **80 → 82** (AC 8 → 10). §5 coverage map splits **G10** (environment & resource access) from **G11** (assessor requirements); the companion-doc group count, the §5 item count, and the verification line are updated to match. **Structure, AT shape, and PE/KE distributions unchanged.** Revalidated: `validate_consolidated.py --assessor-ac` → 82/82 PASS.
