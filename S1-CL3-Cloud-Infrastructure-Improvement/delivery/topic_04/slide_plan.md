# Topic 04 Documenting and presenting the Solution Design — Slide plan
> **Covers:** Topic 04 — see coverage.md
> **Subtitle:** Assemble the whole Solution Design, present it for review, and obtain sign-off to proceed
> **STATUS: DRAFT** (authored 2026-07-02).

## Depth ceiling
DESIGN → sign-off — assemble the four design concerns (Topics 2–3) plus the baseline analysis (Topic 1) into one reviewable Solution Design, present it to the required personnel, and obtain the sign-off to proceed to deployment. No build — this Topic closes the AT1 design phase and gates the AT2/AT3 work.

## Teaching source
Bespoke — technical documentation of a proposed architecture and the review / sign-off discipline; grounded in the Ledgerline improvement scenario, rehearsed on the website practice vehicle.

## AWS pin table
None — bespoke topic.

## Slides

### Opener
- [BESPOKE] Closing AT1 — from design to sign-off
  - Topics 1–3 produced the design; Topic 4 turns it into one reviewable Solution Design and gets it approved.
  - Two moves: document and present the proposed architecture, then obtain the sign-off to proceed to deployment.
  - The cost-benefit reasoning rides inside the Solution Design — there is no separate business case.
  - Design only — this is the AT1 deliverable and its approval gate; the build is AT2/AT3.
  image: gen flat vector hero illustration of a presenter showing a cloud architecture proposal to stakeholders for sign-off, blue and gold accents, minimal, no text

### C1 — Documenting & presenting
- Teaches: [ICTCLD504 PC 2.4]
- Kicker: assemble it, then walk them through it
- [PRIMER] What a Solution Design document is
  - A Solution Design is a professional artefact: the proposed architecture, the rationale, and the trade-offs — complete and readable by a reviewer who wasn't in the room.
  - It documents the improved architecture with clear diagrams, decision rationale, and the metrics behind each call.
  - Pitched for a review audience: the required personnel who decide whether to proceed.
  image: none
- [BESPOKE] Assemble the whole design
  - Bring together the baseline analysis (Topic 1) and the four design concerns — reliability and scalability (Topics 2–3) — into one document.
  - Each proposed change traces back to a named requirement or gap; the diagrams, tables and prose agree.
  - Fold in the cost-benefit reasoning: what each change costs and the improvement it buys.
  image: none
- [TABLE] Solution Design document structure
  | Section | What it contains |
  | Baseline & gaps | Current Ledgerline architecture and the improvement needs (Topic 1) |
  | Proposed architecture | The improved design + diagrams (reliability + scalability, Topics 2–3) |
  | Decision rationale | Each change: the requirement met, the option chosen, why over alternatives |
  | Cost-benefit | The trade-offs — including why the database is not Multi-AZ |
  | Sign-off record | The approval to proceed to deployment |
  note: The cost-benefit is a section here, not a separate business case; the sign-off record closes the document.
  image: none
- [BESPOKE] Present it for review
  - Present the proposed architecture to the required personnel for review — walk the decisions that matter, not every line.
  - Be ready to defend the reliability cost-benefit call: why the database stays single-AZ rather than Multi-AZ.
  - Seek feedback and respond — accept, adjust, or defend with reasons; this is an observed individual oral in AT1 Part B.
  image: none
- [EX] Rehearse the design walkthrough
  - For the practice engagement (the website vehicle), present your assembled Solution Design to a mock review panel.
  - Walk the key decisions and defend the cost-benefit trade-offs; seek and respond to feedback.
  timer: ~25 min
  image: none

### C2 — Obtaining sign-off
- Teaches: [ICTCLD504 PC 2.5]
- Kicker: get the deploy authorised
- [BESPOKE] The deploy sign-off — the approval gate
  - Obtain sign-off to proceed to deployment from the required personnel — the formal authorisation to build.
  - Sign-off is the gate: no AT2/AT3 work starts until the design is approved.
  - Record it — who approved, on what, when — as part of the Solution Design.
  image: none
- [BESPOKE] Two approval moments — don't confuse them
  - This is the cluster's first approval: sign-off to proceed to deployment, on the design.
  - The second is the final sign-off at AT3, on the deployed and tested improvement.
  - This gate authorises the build; the AT3 gate accepts the result.
  image: none
- [TAKEAWAYS] Topic 4 · Key takeaways
  - Assemble the baseline analysis and the four design concerns into one reviewable Solution Design.
  - The cost-benefit rides inside the document — no separate business case; be ready to defend the no-Multi-AZ call.
  - Present the proposed architecture to the required personnel and respond to feedback.
  - Obtain and record the sign-off to proceed — the deploy gate, distinct from the AT3 final sign-off.
  image: none

### Close
- [BESPOKE] Next: Topic 5 — leading the AT2 build
  - AT1 is closed out: designed, documented, presented, signed off to proceed.
  - Next you switch from design to build — lead and plan the team that implements the approved design.
  image: none

## Build notes
~10 slides. One `[EX]` rehearses the design walkthrough + sign-off conversation on the website practice vehicle (design only, no build). One `[TABLE]` gives the Solution Design document structure. One decorative `gen` image (opener hero); no technical diagram.

## Changelog
- 2026-07-02 — authored to full content.
