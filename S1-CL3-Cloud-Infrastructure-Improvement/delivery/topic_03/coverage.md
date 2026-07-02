# Topic 3 — Designing for scalability & the four components · Coverage

**Topic 3 of 8** · **AT1 content Topic** (Design — Solution Design, scalability strand) · teaching source: AWS performance/scalability pillar (elastic capacity, auto scaling, resource selection) + bespoke for the four-component allocation framing · *DRAFT 2026-07-02*.

This file is the **coverage spec** for the Topic.

**Depth ceiling: DESIGN.** Design the scalability improvements on paper and select/improve the four resource tiers to the business needs — the build is AT3. Justify each resource choice; do not implement, and do not over-engineer.

---

## What this Topic must cover

The scalability half of the Solution Design, structured by the **four resource components — network / compute / database / storage** (the same four units the AT2 team divides the IaC write by). Select and improve each tier to the business needs so capacity is elastic-on-demand and demonstrable by test, and place object storage in context — Ledgerline (a stateful accounting system) contrasted with an object-storage-dependent static-website workload. Two components:

- **C1 — The four resource components.** Select and improve compute, storage, database and network resources to Ledgerline's business needs — the network/compute/database/storage tiers, elastic capacity-on-demand, and how each choice serves scalability (demonstrable by test at AT3).
- **C2 — Object storage in context.** The use of object storage for static web sites — the contextual knowledge that lets a student contrast Ledgerline's storage needs with an object-storage-dependent website workload and explain how they would provision that storage if needed.

---

## 1. UoC mapping

| UoC item | Descriptor | Component |
|---|---|---|
| [ICTCLD504 PC 2.2] | Select and improve compute, storage, database and network resources according to business needs | C1 |
| [ICTCLD504 KE 6] | use of object storage for static web sites | C2 |

> Taught here; formally **evidenced** in AT1 (Solution Design — resource-selection sections) + the Part A KE appendix (object-storage-in-context question).

---

## 2. AT alignment

| AT1 element | How Topic 3 aligns |
|---|---|
| **Design — element 2 (improve architecture: resources)** | Direct — select and improve the network/compute/database/storage tiers for scalability against the business needs (C1). |
| **Design — KE appendix** | The object-storage-for-static-sites contextual question (Ledgerline contrasted with a website) (C2). |

**Practice-activity alignment:** select and improve the four resource tiers for the **practice vehicle**, showing where capacity scales elastically, and answer the object-storage-in-context question.

---

## Out of scope for this Topic (covered elsewhere)

- **Baseline review, goals & metrics** → Topic 1.
- **Reliability design (Multi-AZ, DR, backup/restore)** → Topic 2.
- **Documenting, presenting & sign-off** → Topic 4.
- **Allocating the four components to team members and writing the IaC** → AT2 (Topics 5–6).
- **Deploying & demonstrating scalability by test** → AT3 (Topics 7–8).

---

## Coverage checklist

- [ ] Every UoC item in §1 is taught.
- [ ] Each of C1–C2 has teaching content (AWS scalability pillar and/or bespoke).
- [ ] The design selects/improves all four resource tiers (network/compute/database/storage) to the business needs.
- [ ] The object-storage-in-context contrast is taught.
- [ ] Depth stays at design — no implementation/build.
- [ ] A student leaving this Topic could attempt the scalability half of the Solution Design.
