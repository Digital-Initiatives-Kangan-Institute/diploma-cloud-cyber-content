# Topic 7 — Deploying the baseline & applying the improvement as a change-set · Coverage

**Topic 7 of 8** · **AT3 content Topic** (Implement — deploy, monitor & test; 504 el 3) · teaching source: AWS CloudFormation deploy/change-sets + CloudWatch monitoring + bespoke (apply-as-update discipline) · *DRAFT 2026-07-02*.

This file is the **coverage spec** for the Topic.

**Depth ceiling: BUILD.** First hands-on Topic of AT3. Deploy the approved architecture to the Learner Lab, measure it against the metrics, test and demonstrate the improvements, and refine — every improvement applied as an **in-place/additive change-set** over the deployed baseline. Per the process, AWS practicals run `teach → demo → practice`.

---

## What this Topic must cover

The deploy-and-prove half of AT3: stand up the Ledgerline baseline, then apply the approved improvement **as an update (change-set)**, monitor and measure against the metrics and business goals, test and demonstrate the security/reliability/scalability/cost improvements, and apply short-term refinements from the test results — using the console, SDKs or CLI. Four components:

- **C1 — Deploy the approved architecture.** Deploy the approved improved architecture on the cloud platform as an apply-as-update change-set over the baseline; use cloud management consoles, SDKs or command-line tools to do it.
- **C2 — Monitor & measure.** Monitor and measure the architecture against the performance metrics and business goals set at AT1 — using the industry-standard metrics, methods and monitoring techniques for cloud resources.
- **C3 — Test & demonstrate.** Test and demonstrate the security, reliability, scalability and cost optimisation of the deployed resources — using testing/debugging techniques, including techniques to avoid single points of failure.
- **C4 — Short-term refinements.** Apply short-term refinements to the deployed resources according to the test results.

---

## 1. UoC mapping

| UoC item | Descriptor | Component |
|---|---|---|
| [ICTCLD504 PC 3.1] | Deploy approved architecture on cloud platform | C1 |
| [ICTCLD504 PE 4] | use cloud management consoles, software development kits or command line tools | C1 |
| [ICTCLD504 PC 3.2] | Monitor and measure architecture against performance metrics and business goals | C2 |
| [ICTCLD504 KE 10] | techniques, methods and industry standard metrics and business goals used to monitor performance of cloud resources | C2 |
| [ICTCLD504 PC 3.3] | Test and demonstrate security, reliability, scalability and cost optimisation of deployed resources | C3 |
| [ICTCLD504 PE 2] | deploy, test and measure at least one architecture design, against architecture principles, metrics and business goals | C3 |
| [ICTCLD504 KE 7] | testing and debugging techniques, including techniques to avoid single point failures | C3 |
| [ICTCLD504 PC 3.4] | Apply short-term refinements to deployed resources according to test results | C4 |

> Taught here; formally **evidenced** in AT3 (Implementation — the deploy, monitoring evidence, test results and refinements) + the AT3 documentation.

---

## 2. AT alignment

| AT3 element | How Topic 7 aligns |
|---|---|
| **Implement — element 3 (deploy, monitor, test)** | Direct — deploy the approved architecture as a change-set, monitor/measure against metrics, test and demonstrate the improvements, refine (C1–C4). |

**Practice-activity alignment:** `teach → demo → practice` — deploy a baseline, apply an improvement as a change-set, monitor and test it in the lab on the **practice vehicle**, before the assessed Ledgerline deploy.

**Learner Lab note:** the improvement applies as an in-place/additive change-set. The **database tier is not modified** (the lab role denies `rds:ModifyDBInstance`), so DB-tier DR stays design-level (per AT1); app-tier Multi-AZ, scalability and monitoring improvements are built and evidenced.

---

## Out of scope for this Topic (covered elsewhere)

- **The design being deployed** → AT1 (Topics 1–4).
- **Leading the team that wrote the IaC** → AT2 (Topics 5–6).
- **Documenting the as-deployed system, long-term strategy and final sign-off** → Topic 8.

---

## Coverage checklist

- [ ] Every UoC item in §1 is taught.
- [ ] Each of C1–C4 has teaching content (AWS deploy/monitor and/or bespoke).
- [ ] A `[DEMO]` precedes the practice (deploy + apply-as-update change-set).
- [ ] The improvement is applied as an in-place/additive change-set, DB tier untouched.
- [ ] The deploy is monitored and tested against the AT1 metrics/goals.
- [ ] A student leaving this Topic could attempt the deploy/test half of AT3.
