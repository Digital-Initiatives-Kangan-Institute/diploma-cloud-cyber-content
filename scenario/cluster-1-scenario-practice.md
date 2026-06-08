# Cluster 1 — Scenario (Practice)

> **Role:** Practice · **Vehicle:** Ledgerline (Accounting & Office Administration) · per `scenario-flow.md`.
>
> Lean cluster-and-role delta of the greater YAT scenario — see `scenario-flow.md`, the intranet content, and the ICT specs. This doc records only what is specific to **CL1 practice on Ledgerline**. Meta/design doc.

## 1. Engagement

YAT engages **MTS Consulting** to evaluate the future operating model for its **Accounting & Office Administration system (Ledgerline)** — renew on-premises vs migrate to AWS — and to produce a board-ready Business Case. This is an **analysis-and-planning engagement only** (no build): MTS recommends, the YAT board decides. In delivery it is the vehicle students rehearse the Business-Case and design skills on, before being assessed on those skills against the LMS. In-world this is the **MTS – Accounting System Cloud Migration** project on the intranet.

## 2. Scenario deltas (why Ledgerline is a deliberate practice contrast)

Same competency, different system profile — so students must **transfer** the skill rather than pattern-match a practised answer onto the assessment:

- **Internal, staff-only, business-hours** — a **99.5%** business-hours target, *not* the LMS's 99.9% / 24/7.
- **Commercial licensing** — Ledgerline per-user + Microsoft SQL Server per-core (~$27k/yr) — a cost dimension the open-source LMS lacks, and material to the cost-benefit analysis (licence-included vs bring-your-own).
- **Payroll outsourced**; financial records carry a **7-year retention** obligation; RPO ≤ 1 hour / RTO ≤ 1 business day.
- **Data residency** — financial records and billing PII remain in Australia.

## 3. Vehicle state

On-premises throughout CL1 — the evaluation recommends, the board decides, and no migration happens in-cluster. Held in `accounting-application-spec.md`, the Accounting System Server Specifications, and `accounting-operational-costing.md`.

## 4. Practised focus

Rehearses the CL1 assessment skills — principally the AT1 Business Case, plus the analysis and design that feed the AT2/AT3 work — on the Accounting evaluation. Units as per the assessment vehicle: **ICTCLD401**, **ICTCLD502**, **ICTICT517**.

## 5. References

- `scenario-flow.md`; `cluster-1-scenario-assessment.md` — the assessment contrast (LMS)
- Intranet: **MTS – Accounting System Cloud Migration** project; **Accounting System Application Specification**; **Accounting System Operational Costing**
