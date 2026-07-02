# Topic 05 Leading and planning the team build — Slide plan
> **Covers:** Topic 05 — see coverage.md
> **STATUS: DRAFT** (authored 2026-07-02).

## Depth ceiling
LEADERSHIP / team-planning — plan the team and set it up to build (BSBXTW401 el 1–2): objectives, performance plans, accountability, contingencies, and allocating the four IaC components. Not technical design/build — the CloudFormation write itself is Topic 6 / AT3 and is NOT 504-assessed here.

## Teaching source
Bespoke throughout, drawn from BSBXTW401 leadership content (team planning, task allocation, facilitation) applied to the four-component IaC allocation. In-world team = YAT ICT staff improving Ledgerline.

## AWS pin table
None — leadership (BSBXTW401) topic; bespoke.

## Slides

### Opener
- [BESPOKE] Leading the build team
  - Topic 5 opens AT2: the approved design is written as CloudFormation by a **team of four**, one IaC component each — network, compute, database, storage.
  - Dividing the write is the leadership vehicle: you plan the team, set expectations, and allocate the work — the write itself is a 504 concern, not assessed here.
  - This Topic is the set-up half of AT2 (plan and stand up the team); leading them *through* the write is Topic 6.
  - In-world, the team is YAT ICT staff improving Ledgerline.
  image: gen flat vector hero illustration of a team leader assigning four workstreams to four team members around a table, blue and gold accents, minimal, no text

### C1 — Objectives, performance plans & accountability
- Teaches: [BSBXTW401 PC 1.1] · [BSBXTW401 PC 1.2] · [BSBXTW401 PC 1.3] · [BSBXTW401 KE 1] · [BSBXTW401 KE 2]
- Kicker: know the goal, set expectations, hold the line
- [PRIMER] Team objectives, responsibilities & outcomes
  - Start by naming the common objective: deliver the approved Ledgerline design as working, deployed IaC.
  - Break it into responsibilities and required outcomes — what the team must produce, and to what standard.
  - Shared, explicit objectives are what let four separate component-writers pull in one direction.
  image: none
- [BESPOKE] Performance plans set expectations
  - A performance plan sets each member's expected outcomes, goals and behaviours for their component.
  - Align each plan to the team objective and to relevant policies — a plan is not a wish-list, it is measurable.
  - Example: "network component templates valid, peer-reviewed and deployed to us-east-1 by the milestone; collaborates on shared parameters."
  image: none
- [BESPOKE] Accountability, grounded in organisational & legislative requirements
  - Choose accountability strategies: clear ownership per component, review checkpoints, a shared definition of done.
  - Ground them in **organisational requirements** — workplace policies, codes of conduct, and YAT's reputation and culture (KE 1).
  - Respect the **legislative requirements** relevant to the workplace (work health & safety, privacy, anti-discrimination) (KE 2) — accountability operates inside those rules.
  image: none

### C2 — Contingency planning
- Teaches: [BSBXTW401 PC 1.4] · [BSBXTW401 KE 9]
- Kicker: plan for the things that go wrong
- [BESPOKE] Typical team contingencies
  - Plan for contingencies that could impact the team before they happen — don't improvise under pressure.
  - The typical workplace ones: unplanned leave or absence of a component owner; re-allocation of work tasks when load shifts; succession planning for important roles (KE 9).
  - For the build team: if the database-component owner is absent, who picks it up, and how is the handover documented?
  - A contingency is a named trigger plus a pre-agreed response — write it into the team plan.
  image: none

### C3 — Communicating & allocating the component work
- Teaches: [BSBXTW401 PC 2.1] · [BSBXTW401 PC 2.2] · [BSBXTW401 PE 1]
- Kicker: communicate the goal, then hand out the work
- [BESPOKE] Communicate the objectives & responsibilities
  - Communicate the common objectives and each member's responsibilities so everyone shares the same picture of "done".
  - Confirm understanding — a kick-off where the team restates the goal and how the four components integrate.
  - Clear communication up front is what prevents four components that don't fit together.
  image: none
- [BESPOKE] Allocate the four components
  - Allocate the four IaC components — **network, compute, database, storage** — one per member, by expertise or development potential (PC 2.2).
  - Give appropriate instruction with each allocation: scope of the component, the interfaces it must expose, and any required contingencies (PE 1).
  - The four allocations integrate into one design — allocate the seams (shared parameters, dependencies), not just the boxes.
  image: diagram component-allocation
- [EX] Plan & allocate the practice build team
  - For the practice engagement, draft the **team plan**: common objective, per-member performance plans, accountability strategies and contingencies.
  - **Allocate the four components** to four members with clear instruction and any required contingencies.
  - Produce the artefact you'll produce for the assessed Ledgerline team — this is the practice run.
  timer: ~30 min
  image: none

### C4 — Facilitating collaboration
- Teaches: [BSBXTW401 PC 2.3] · [BSBXTW401 PC 2.4] · [BSBXTW401 KE 3] · [BSBXTW401 KE 6] · [BSBXTW401 KE 7]
- Kicker: keep the team open, respectful and connected
- [PRIMER] Facilitation & communication styles
  - Facilitate open and respectful communication and collaboration between members (PC 2.3).
  - Use facilitation techniques that build cohesion and effectiveness — stand-ups, shared review, ground rules (KE 3).
  - Match the method and style of communication to the message and the person (KE 6) — synchronous for decisions, written for the record.
  image: none
- [BESPOKE] Diverse teams & cross-collaboration
  - Consider the needs of members from diverse backgrounds: apply cross-cultural communication principles and accommodate special needs or disabilities (KE 7, PC 2.3).
  - Identify opportunities for cross-collaboration with internal and external teams — the DBA team, the security reviewers, an external CloudFormation SME (PC 2.4).
  - Respectful, inclusive facilitation is what makes a four-person split behave as one team.
  image: none
- [TAKEAWAYS] Topic 5 · Key takeaways
  - Name the common objective, set per-member performance plans, and choose accountability strategies grounded in policy and law.
  - Plan for the typical contingencies — absence, re-allocation, succession — before the build starts.
  - Communicate the objective, then allocate the four components one per member with clear instruction.
  - Facilitate open, respectful, inclusive collaboration and connect with internal/external teams.
  image: none

### Close
- [BESPOKE] Next: Topic 6 — lead the team through the build
  - You've planned the team and allocated the four components; next you lead, support and monitor them as they write the IaC.
  - Bring the team plan and allocations — Topic 6 runs the build against them.
  image: none

## Build notes
~13 slides. Bespoke leadership topic (no AWS pins). Exercise = draft the team/performance plan and allocate the four components for the practice engagement. One generated diagram (`diagram component-allocation` — four members mapped to the four components integrating into one design); one decorative `gen` image (opener hero).

## Changelog
- 2026-07-02 — authored to full content.
