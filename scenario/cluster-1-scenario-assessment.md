# Cluster 1 — Scenario (Assessment)

> **Role:** Assessment · **Vehicle:** LMS (DOODLE) · per `scenario-flow.md`.
>
> Lean cluster-and-role delta of the greater YAT scenario. The cross-cluster system/usage model is in `scenario-flow.md`; the in-world artefacts are the intranet content; the system detail is in the ICT specs. This doc records only what is specific to **CL1 assessment on the LMS**. Meta/design doc — uses assessment language freely.

## 1. Engagement

YAT engages **MTS Consulting** to migrate its **Learning Management System (DOODLE)** from its end-of-life on-premises deployment to AWS, and then make it highly available. The engagement runs in three phases that map one-to-one onto the cluster's three assessment tasks:

- **AT1 — Business Case:** strategic and current-state analysis, cost-benefit analysis, and a board-ready Business Case (with presentation) recommending the cloud migration.
- **AT2 — Cloud Foundation Build:** implement the approved single-AZ AWS foundation (the Baseline Design) and document it in a Deployment Report.
- **AT3 — High Availability Hardening:** harden the single-AZ baseline to a Multi-AZ deployment that meets the 99.9% availability target.

The student is the **MTS Consultant** delivering the engagement (MSA `YAT-MTS-2026-001`). In-world this is the **MTS – LMS Cloud Infrastructure** project on the intranet.

## 2. Scenario deltas (what makes the LMS the assessment vehicle)

- **Mission-critical, student-facing, 24/7** — drives the **99.9%** availability target and the HA-hardening work in AT3.
- **End-of-life on-prem hardware** plus YAT's student-growth trajectory — the migration driver, aligned to the ICT Strategic Plan.
- **Open-source stack** (DOODLE + MySQL) — no commercial-licensing dimension (the deliberate cost-shape contrast with the Accounting practice vehicle).
- **Data residency** — all student PII remains in Australia (`ap-southeast-2`; Privacy Act, APP 8).

## 3. Vehicle state

The LMS moves through three states across the cluster, each held in the state-versioned ICT records:

- **On-prem** (`s1-cl1-at1` / `at2`) — `environment-overview.md`, `lms-application-spec.md`, the on-prem network diagram.
- **Cloud single-AZ baseline** (`s1-cl1-at3`) — `lms-application-spec-cloud.md`, the LMS Infrastructure Specifications, and the LMS Cloud Architecture — Baseline Design.
- **Cloud Multi-AZ HA** (`s1-cl2-at1` onward) — the HA-hardened ICT state and network diagram.

## 4. Assessed focus

Units **ICTCLD401**, **ICTCLD502**, **ICTICT517**. The full item-level UoC mapping and the AT instruments live in `S1-CL1-Cloud-Design-Build/`.

## 5. References

- `scenario-flow.md` — cross-cluster system/usage model and the no-leakage invariant
- `cluster-1-scenario-practice.md` — the practice contrast (Ledgerline)
- Intranet: **MTS – LMS Cloud Infrastructure** project; **LMS Application Specification**; **LMS Cloud Architecture — Baseline Design**
- `S1-CL1-Cloud-Design-Build/` — assessment tasks and UoC mapping
