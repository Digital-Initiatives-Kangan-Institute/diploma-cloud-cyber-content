# YAT Scenario — System Usage Flow Across Clusters

> **Document type:** Meta — scenario design/spec. Uses assessment/UoC language freely (this is *not* in-world intranet content). Companion to `cluster-2-scenario.md` and the per-cluster `consolidated_uoc.md` files.

**Status:** Direction set by Tim (2026-06-08). Markers: **[AGREED]** = confirmed with Tim · **[TBD]** = follow-on work not yet done · **[VERIFY]** = factual claim to confirm before it lands in a student-facing artefact.

---

## 1. Purpose

The Semester 1 clusters share a **small set of scenario systems** rather than inventing a fresh, disconnected world each cluster. In any given cluster a system is used as either:

- a **practice** vehicle — used in teaching/delivery to rehearse the skills, or
- an **assessment** vehicle — the system the formal assessment evidence is produced against.

This document records (a) how the systems map to clusters, (b) the rule that guarantees **no assessment deliverable is ever disclosed across a parallel cluster**, and (c) the learning benefit of keeping students inside a small, familiar set of systems all semester.

## 2. The three systems

- **LMS** — YAT's learning management system. Plausibly **large user base** (web-scale-credible). Migrated to the cloud and made highly available in CL1.
- **Website** — YAT's web infrastructure as defined in the scenario (the cloud infrastructure behind YAT's public web presence). Plausibly **large user base** (web-scale-credible).*(Distinct from the Astro site that delivers these scenario materials — that is the delivery platform, per `website.md`, not a scenario system.)*
- **Ledgerline** — YAT's bookkeeping / general-ledger system, used by internal finance staff. **Small internal user base — not web-scale** (per `cluster-2-scenario.md §5`).

## 3. Usage matrix [AGREED]

| System | CL1 — Cloud Design & Build | CL2 — Cloud Disaster Recovery | CL3 — Cloud Infrastructure Improvement |
|---|---|---|---|
| **LMS** | **Assessment** | Practice | — |
| **Website** | — | **Assessment** | Practice |
| **Ledgerline** | Practice | — | **Assessment** |

The bold cell in each cluster column is that cluster's **assessment** vehicle.

## 4. Two principles the matrix satisfies

### 4.1 No-leakage invariant [AGREED]

> **Every system is an *assessment* vehicle in at most one cluster. Wherever a system is reused in another cluster, it is on the *practice* side only.**

Because no system is assessed in two clusters, **no cluster's assessed deliverable can ever be the answer to another cluster's assessment**. Cross-cluster reuse provides *familiarity*, never a disclosed deliverable.

This holds even though **CL2 and CL3 run in parallel** (both weeks 9–18):

- The **website** is *assessed* in CL2 and *practised* in CL3 at the same time. CL2's assessed deliverable is each student's own **DR plan**; CL3's website work is **improve-loop practice**. Practising on the website neither produces nor discloses any CL2 deliverable. The website's *design* is a **supplied input** to CL2 anyway (students must have it to plan DR against) — the design is not secret; the protected artefact is the student's own DR plan.
- **Ledgerline** is *assessed* in CL3 and **not used in CL2 at all** — no parallel exposure.

### 4.2 Practice ≠ assessment within every cluster (transfer of learning) [AGREED]

In every cluster the **practice system differs from the assessment system**, so students cannot pattern-match a practised answer onto the assessment — they must transfer the skill (the principle from `cluster-2-scenario.md §6`):

- CL1 — practise on **Ledgerline**, assessed on **LMS**.
- CL2 — practise on **LMS**, assessed on **Website**.
- CL3 — practise on **Website**, assessed on **Ledgerline**.

Across the semester the three systems **rotate** through both roles: each cluster's assessment vehicle becomes a later cluster's practice vehicle (LMS: CL1 assess → CL2 practice; Website: CL2 assess → CL3 practice), and Ledgerline runs the reverse (CL1 practice → CL3 assess).

## 5. Familiarity benefit [AGREED]

Students work across **only three systems** all semester, inside one continuous YAT world, and meet each system more than once in different roles. They are not asked to absorb a new, unrelated scenario each cluster — their effort goes into the cloud skills, not re-learning a backstory. The small, recurring system set is what makes that continuity cheap.

## 6. Key cross-cluster dependency [AGREED]

- **CL2 AT1 (DR plan)** plans against a **supplied website infrastructure design**. Supplying it is legitimate precisely because the website is **not** a CL3 *assessment* vehicle (only a CL3 *practice* vehicle) — so no CL3 deliverable is disclosed. This also removes any **timing dependency**: CL2 AT1 does not wait on CL3 producing a design.
- CL2 DR-planning targets the **defined as-is website infrastructure** — a fixed snapshot, independent of any improvements students make during CL3 website practice.
