# Topic 1 — Analysing the baseline architecture · Coverage

**Topic 1 of 8** · **AT1 content Topic** (Design — Solution Design, analysis strand: review & set goals) · teaching source: AWS well-architected review (reliability/performance/cost/security pillars) + bespoke for the Ledgerline baseline framing · *DRAFT 2026-07-02*.

This file is the **coverage spec** for the Topic.

**Depth ceiling: ANALYSIS.** Review and evaluate the *existing* Ledgerline architecture and set the improvement goals + metrics — the analysis that the reliability/scalability design (Topics 2–3) then acts on. Diagnose and justify; do not design the changes yet, and do not implement.

---

## What this Topic must cover

The analysis half that opens the Solution Design: review Ledgerline's current single-AZ cloud architecture, evaluate the business impact of its design decisions, weigh cloud/architectural options against the business model, confirm the design decisions to carry forward, and set the security / reliability / high-performance / cost goals and the performance metrics the improvement will be measured against. Three components:

- **C1 — Reviewing the baseline.** Identify and review Ledgerline's current cloud architecture design; evaluate it and the business impact of its design decisions; the industry technology standards, standard hardware/software products, and the methods and impacts of cloud adoption that frame the review.
- **C2 — Options & fit against the business model.** Identify the design patterns and architectural options available; assess the benefits and differences of cloud computing and architectural design against Ledgerline's current business model and needs; confirm the system design decisions to carry forward.
- **C3 — Goals & metrics.** Set the business goals for security, reliability, high-performance and cost efficiency; evaluate and confirm the performance metrics the improved application will be measured against.

---

## 1. UoC mapping

| UoC item | Descriptor | Component |
|---|---|---|
| [ICTCLD504 PC 1.1] | Identify and review business's cloud architecture design | C1 |
| [ICTCLD504 PC 1.2] | Evaluate cloud architecture and identify business impact of design decisions | C1 |
| [ICTCLD504 PC 1.3] | Identify design patterns and architectural options | C2 |
| [ICTCLD504 PC 1.4] | Determine and assess benefits and differences of cloud computing and architectural design against current business model and needs | C2 |
| [ICTCLD504 PC 1.5] | Confirm system design decisions according to business needs | C2 |
| [ICTCLD504 PC 1.6] | Set business goals as they relate to security, reliability, high-performance and cost efficiencies of cloud architecture according to business requirements and needs | C3 |
| [ICTCLD504 PC 2.1] | Evaluate and confirm performance metrics for business applications according to business needs | C3 |
| [ICTCLD504 PE 3] | determine performance metrics and business goals | C3 |
| [ICTCLD504 KE 1] | industry technology standards used in cloud computing solutions and services | C1 |
| [ICTCLD504 KE 2] | industry standard hardware and software products, their general features, capabilities and application | C1 |
| [ICTCLD504 KE 3] | methods and impacts of cloud adoption as they relate to IT system changes | C1 |

> Taught here; formally **evidenced** in AT1 (Solution Design — baseline analysis, goals & metrics sections) + the Part A KE appendix.

---

## 2. AT alignment

| AT1 element | How Topic 1 aligns |
|---|---|
| **Design — element 1 (analyse architecture)** | Direct — review the supplied Ledgerline baseline, evaluate business impact, weigh options against the business model, confirm decisions (C1, C2). |
| **Design — goals & metrics (bridge to element 2)** | Set the security/reliability/performance/cost goals and confirm the metrics the improvement design and the AT3 build are measured against (C3). |

**Practice-activity alignment:** run the same baseline review on the **practice vehicle (the website)** — review the current architecture, evaluate business impact, and draft the goals + metrics — before analysing Ledgerline for the assessment.

---

## Out of scope for this Topic (covered elsewhere)

- **Designing the reliability improvements** (Multi-AZ app tier, DB backup/restore, cross-Region DR) → Topic 2.
- **Designing scalability & selecting the four components** → Topic 3.
- **Documenting, presenting and obtaining sign-off** → Topic 4.
- **Leading the team build** → AT2 (Topics 5–6); **deploying/testing** → AT3 (Topics 7–8).

---

## Coverage checklist

- [ ] Every UoC item in §1 is taught.
- [ ] Each of C1–C3 has teaching content (AWS well-architected review and/or bespoke).
- [ ] The exercise reviews a baseline architecture, evaluates business impact, and sets goals + metrics on the practice vehicle.
- [ ] Depth stays at analysis — no design of the changes, no implementation.
- [ ] A student leaving this Topic could attempt the analysis half of the Solution Design.
