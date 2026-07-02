# Topic 2 — Designing for reliability · Coverage

**Topic 2 of 8** · **AT1 content Topic** (Design — Solution Design, reliability strand) · teaching source: AWS reliability pillar (Multi-AZ, backup/restore, cross-Region DR) + bespoke for the Ledgerline cost-benefit framing · *DRAFT 2026-07-02*.

This file is the **coverage spec** for the Topic.

**Depth ceiling: DESIGN.** Design the reliability *improvements* on paper to the goals set in Topic 1 — the build is AT3. Justify each choice against the goals and against cost; do not over-engineer, and do not implement.

---

## What this Topic must cover

The reliability half of the Solution Design: review the architecture and design the changes that enhance reliability (and, jointly, security/scalability/cost) — app-tier Multi-AZ, DB backup/restore, and cross-Region DR to Melbourne — applying cloud design and migration principles and the security layers that underpin them. The **cost-benefit centrepiece** is the *rejection* of a Multi-AZ database as disproportionate: the DB is left single-AZ with backup/restore + cross-Region DR, and that trade-off is argued explicitly. Three components:

- **C1 — Reliability improvement design.** Review and improve the architecture to enhance reliability (with security/scalability/cost); design app-tier Multi-AZ + DB backup/restore + cross-Region DR; the features and techniques of cloud services used to improve reliability, and the Multi-AZ-database cost-benefit rejection as the reliability centrepiece.
- **C2 — Cloud design & migration principles.** The design principles for cloud applications and the migration principles that govern moving the baseline to the improved architecture.
- **C3 — Security layers underpinning the design.** The tools and uses of security layers and security-focused content within cloud services that keep the improved architecture secure (encryption is the baseline).

---

## 1. UoC mapping

| UoC item | Descriptor | Component |
|---|---|---|
| [ICTCLD504 PC 2.3] | Review and improve architecture required to enhance security, reliability, scalability and cost optimisation | C1 |
| [ICTCLD504 PE 1] | assess, identify and improve cloud architecture on a cloud platform, according to design decisions | C1 |
| [ICTCLD504 KE 9] | features of cloud services, including techniques to improve security, reliability, scalability and costs | C1 |
| [ICTCLD504 KE 4] | design principles for cloud applications | C2 |
| [ICTCLD504 KE 5] | migrating principles for cloud applications | C2 |
| [ICTCLD504 KE 8] | tools and uses of security layers and security-focused content within cloud services | C3 |

> Taught here; formally **evidenced** in AT1 (Solution Design — reliability sections, incl. the Multi-AZ-database cost-benefit) + the Part A KE appendix.

---

## 2. AT alignment

| AT1 element | How Topic 2 aligns |
|---|---|
| **Design — element 2 (improve architecture: reliability)** | Direct — design the reliability improvements (app-tier Multi-AZ, DB backup/restore, cross-Region DR) against the goals, with security/scalability/cost jointly optimised (C1). |
| **Design — cost-benefit reasoning** | The rejected Multi-AZ database is the AT1 cost-benefit centrepiece — the design justifies leaving the DB single-AZ (C1). |
| **Design — KE appendix** | Cloud design/migration principles + security layers underpinning the improvement (C2, C3). |

**Practice-activity alignment:** design the reliability improvements for the **practice vehicle**, including one cost-benefit trade-off argued explicitly, to the goals set in Topic 1.

---

## Out of scope for this Topic (covered elsewhere)

- **Baseline review, goals & metrics** → Topic 1.
- **Scalability design & the four resource components** → Topic 3.
- **Documenting, presenting & sign-off** → Topic 4.
- **Building/deploying the reliability improvement** → AT3 (Topics 7–8); the DB tier stays design-level (the lab role denies `rds:ModifyDBInstance`).

---

## Coverage checklist

- [ ] Every UoC item in §1 is taught.
- [ ] Each of C1–C3 has teaching content (AWS reliability pillar and/or bespoke).
- [ ] The design enhances reliability with security/scalability/cost jointly considered.
- [ ] The Multi-AZ-database cost-benefit rejection is designed and argued.
- [ ] Depth stays at design — no implementation/build.
- [ ] A student leaving this Topic could attempt the reliability half of the Solution Design.
