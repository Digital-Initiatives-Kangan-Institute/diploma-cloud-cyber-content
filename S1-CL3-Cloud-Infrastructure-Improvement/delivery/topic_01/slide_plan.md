# Topic 01 Analysing the baseline architecture — Slide plan
> **Covers:** Topic 01 — see coverage.md
> **Subtitle:** Review and evaluate the existing Ledgerline cloud architecture, then set the improvement goals and metrics
> **STATUS: DRAFT** (authored 2026-07-02).

## Depth ceiling
ANALYSIS — review and evaluate the *existing* Ledgerline architecture and set the improvement goals + metrics. Diagnose and justify; do not design the changes (Topics 2–3) and do not implement (AT3).

## Teaching source
AWS well-architected review (reliability / performance / cost / security pillars) pinned at Step 4 (TBD); bespoke for the Ledgerline single-AZ baseline framing and the goals-and-metrics discipline.

## AWS pin table
TBD — AWS ICTCLD504/architecture modules to be pinned.

## Slides

### Opener
- [BESPOKE] From analysis to improvement
  - Topic 1 opens AT1: before you improve a cloud system you first understand the one you have.
  - This Topic is the analysis half of the Solution Design — review the baseline, evaluate it, set the goals. The design of the fix is Topics 2–4.
  - Vehicle: **Ledgerline**, YAT's Accounting system, runs single-AZ in the cloud — the system you analyse and improve.
  - Stay at analysis: diagnose and justify, don't design the changes yet.
  image: gen flat vector hero illustration of an analyst reviewing a cloud architecture diagram, magnifying glass over a data centre, blue and gold accents, minimal, no text

### C1 — Reviewing the baseline
- Teaches: [ICTCLD504 PC 1.1] · [ICTCLD504 PC 1.2] · [ICTCLD504 KE 1] · [ICTCLD504 KE 2] · [ICTCLD504 KE 3]
- Kicker: understand what you have before you change it
- [PRIMER] How to review a cloud architecture
  - A structured review reads an architecture against pillars: security, reliability, performance, cost.
  - Frame the review with industry technology standards used in cloud solutions (KE 1) and the standard hardware/software products the platform is built on — compute families, managed databases, object/block storage (KE 2).
  - Keep the method vendor-neutral here; you apply it to Ledgerline (a real AWS baseline) next.
  image: none
- [BESPOKE] Review the Ledgerline baseline
  - Identify and review Ledgerline's current cloud architecture: a VPC, one Availability Zone, an app tier and a single RDS database.
  - Read the topology top-down — network, compute, database, storage — and note how each resource is deployed today.
  - Cloud adoption changes the IT system: managed services, elasticity and shared responsibility reshape how you run and improve it (KE 3).
  image: diagram ledgerline-baseline
- [BESPOKE] Evaluate the design decisions & their business impact
  - Evaluate the baseline and name the business impact of its design decisions: single-AZ means single points of failure — one AZ outage takes Accounting down.
  - A seeded constraint surfaces here: the accounting product is **vendor-certified single-instance only → the database cannot go Multi-AZ**. Record it now — it is the reliability cost-benefit centrepiece in Topic 2.
  - Impact is a business statement, not a technical one: downtime, lost billing, risk to close-of-month — the language the goals in C3 answer.
  image: none
- [EX] Review the practice baseline
  - On the **practice engagement (the website)**, identify and review its current architecture the same way.
  - Evaluate it and name the business impact of its design decisions — where would an outage or a bottleneck hurt the business?
  timer: ~25 min
  image: none

### C2 — Options & fit against the business model
- Teaches: [ICTCLD504 PC 1.3] · [ICTCLD504 PC 1.4] · [ICTCLD504 PC 1.5]
- Kicker: what could change, and what fits the business
- [PRIMER] Design patterns & architectural options
  - Identify the options available to a cloud architecture: multi-AZ redundancy, horizontal scaling and load balancing, managed vs self-run data tiers, caching, decoupling.
  - Each option is a pattern with a cost and a benefit — there is no single right answer, only a fit.
  - The four improvement concerns to weigh against: security, reliability, scalability, cost.
  image: none
- [BESPOKE] Assess the options against Ledgerline & confirm decisions
  - Determine and assess the benefits and differences of cloud/architectural options **against Ledgerline's current business model and needs** — not in the abstract.
  - Weigh what fits: the single-instance DB constraint rules some reliability options out, which sharpens the ones that remain.
  - Confirm the system design decisions to carry forward according to business needs — the shortlist Topics 2–3 will actually design.
  image: none
- [EX] Weigh options on the practice engagement
  - For the practice engagement, list the architectural options open to it and assess each against its business model and needs.
  - Confirm the design decisions worth carrying forward — and note the ones you rule out and why.
  timer: ~25 min
  image: none

### C3 — Goals & metrics
- Teaches: [ICTCLD504 PC 1.6] · [ICTCLD504 PC 2.1] · [ICTCLD504 PE 3]
- Kicker: set the target the improvement is measured against
- [PRIMER] Goals across the four concerns
  - Set business goals across the four well-architected concerns: security, reliability, high-performance and cost efficiency (PC 1.6, PE 3).
  - A goal is directional and business-owned ("survive an AZ failure without data loss"); a metric makes it measurable.
  - Goals come from business requirements and needs, not from the technology you happen to like.
  image: none
- [BESPOKE] Set Ledgerline's goals & confirm the metrics
  - Set the security / reliability / high-performance / cost goals for Ledgerline from its business requirements.
  - Evaluate and confirm the performance metrics the improved application is measured against — availability %, RTO/RPO, response time, cost per period (PC 2.1).
  - These goals and metrics are the yardstick for the design (Topics 2–3) and the AT3 build — write them so a later Topic can test against them.
  image: none
- [EX] Draft goals & metrics for the practice engagement
  - For the practice engagement, set the goals across security, reliability, performance and cost.
  - Confirm the metrics each goal is measured by — you will design against them in the practice work that mirrors Topics 2–3.
  timer: ~25 min
  image: none
- [TAKEAWAYS] Topic 1 · Key takeaways
  - Review the baseline against the four pillars before changing anything; name the business impact of each design decision.
  - Ledgerline is single-AZ with a **vendor-certified single-instance DB that cannot go Multi-AZ** — carry that constraint into Topic 2.
  - Assess options against the business model, then confirm the decisions to carry forward.
  - Set goals across security, reliability, performance and cost, and confirm the metrics — that is the yardstick for the whole improvement.
  image: none

### Close
- [BESPOKE] Next: Topic 2 — designing the reliability improvements
  - You've reviewed the baseline, weighed the options and set the goals; next you design the reliability changes.
  - Bring the single-instance-DB constraint — it is the reliability cost-benefit centrepiece Topic 2 opens on.
  image: none

## Build notes
~13 slides. Depth ceiling ANALYSIS — no design of the fix. Worked examples use Ledgerline; the three `[EX]`s run the same analysis on the practice engagement (the website). One generated technical diagram (`diagram ledgerline-baseline` — single-AZ VPC, one AZ, app tier + single RDS, single points of failure); one decorative `gen` image (opener hero); every other slide `image: none`.

## Changelog
- 2026-07-02 — authored to full content from coverage.md (Step 4 artefact).
