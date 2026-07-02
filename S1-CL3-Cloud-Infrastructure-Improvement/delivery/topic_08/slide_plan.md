# Topic 08 Testing, refining and documenting the whole system; final sign-off — Slide plan
> **Covers:** Topic 08 — see coverage.md
> **Subtitle:** Document the as-deployed system against the approved design, describe the long-term strategy, and obtain the final sign-off
> **STATUS: DRAFT** (authored 2026-07-02).

## Depth ceiling
BUILD / FINALISE — the closing AT3 topic. The deploy, monitoring and testing happened in Topic 7; here the deployed-and-tested improvement is written up as-built, the long-term improvement strategy is described, and the final sign-off is obtained. No new build — this closes out AT3 and the cluster.

## Teaching source
Bespoke — as-deployed documentation to the YAT templates, the long-term-improvement narrative, and the final review / sign-off discipline; grounded in the Ledgerline improvement, rehearsed on the website practice vehicle.

## AWS pin table
None — bespoke topic.

## Slides

### Opener
- [BESPOKE] Closing AT3 — document, refine, sign off
  - Topic 7 deployed, monitored and tested the improvement; Topic 8 writes it up and closes the cluster.
  - Three moves: document the as-deployed system against the approved design, describe the long-term improvement strategy, and obtain the final sign-off.
  - The deliverable is the **Deployment Report** — the whole system across all four concerns: security, reliability, scalability, cost.
  - No new build — the report is assembled from what you captured live during the Topic 7 deploy and test.
  image: gen flat vector hero illustration of an engineer finalising a deployment report and obtaining sign-off, checklist and signature, blue and gold accents, minimal, no text

### C1 — Document as-deployed + test results
- Teaches: [ICTCLD504 PC 4.1] · [ICTCLD504 PE 5]
- Kicker: record what you actually deployed, and prove it works
- [PRIMER] The as-deployed record & the Deployment Report
  - An as-deployed record documents the system as it was actually deployed — not the design on paper, the resources actually running.
  - The Deployment Report assembles it: the as-deployed architecture, the test results, the changes from the approved design, and the deployment/testing steps.
  - It is complete and readable by someone who wasn't in the room — a reviewer can follow it end to end.
  image: none
- [BESPOKE] As-deployed vs the approved design — highlight the changes
  - Document the as-deployed architecture and test results, and **highlight the changes and improvements from the approved design** (PC 4.1).
  - Every difference is named and justified — e.g. the DB-tier DR stayed at design level because the lab couldn't modify the database; the app-tier Multi-AZ was built and evidenced.
  - Test results cover all four concerns — security, reliability, scalability, cost — each against the goals set in Topic 1.
  image: none
- [BESPOKE] Document the deployment & testing steps
  - Create the documentation of the deployment and testing steps (PE 5) — the step-by-step record of how the improvement was deployed and tested.
  - Written so a reader could repeat it: the stacks/changes applied, in order, and each test run with its outcome.
  - Assembled from the screenshots, exports and logs you captured as you went in Topic 7 — you can't reconstruct it after the fact.
  image: none
- [TABLE] Deployment Report structure
  | Section | What it contains |
  | As-deployed architecture | The system as actually deployed to us-east-1 — diagrams and resource inventory across all four concerns |
  | Changes from approved design | Where the as-deployed differs from the approved design, and why (e.g. DB-tier DR left at design level) |
  | Test results | The tests run against the deployment and their outcomes — security, reliability, scalability, cost |
  | Deployment & testing steps | The step-by-step record of how it was deployed and tested (PE 5) — repeatable by a reader |
  | Long-term improvement strategy | The next-iteration improvements and their benefits (C2) |
  | Final sign-off record | The approval accepting the deployed system — who, on what, when |
  note: The four concerns run across the as-deployed record and test results; the sign-off record closes the document.
  image: none

### C2 — Long-term improvement strategies
- Teaches: [ICTCLD504 PC 4.2]
- Kicker: what the next iteration would improve, and why
- [BESPOKE] Describe the long-term improvement strategy
  - Describe long-term improvement strategies and their benefits **as applied to the deployed resources** (PC 4.2) — what a next iteration would improve and the benefit it buys.
  - This is where the DB-tier DR lives: built at design level here, it is the headline long-term strategy — cross-Region database resilience and the availability benefit it delivers.
  - Include other future improvements across the four concerns — tighter cost controls, further scalability headroom, security hardening — each tied to a benefit, not a wish-list.
  image: none

### C3 — Final sign-off
- Teaches: [ICTCLD504 PC 4.3]
- Kicker: get the deployed system accepted
- [BESPOKE] Obtain the final sign-off
  - Obtain final sign-off from the required personnel (PC 4.3) — the formal acceptance of the deployed and tested improvement.
  - Walk the Deployment Report: the as-deployed system, the test results against the goals, and the long-term strategy — confirm requirements met for the audience, not in jargon.
  - Record it — who approved, on what, when — as the closing section of the report.
  image: none
- [BESPOKE] Two approval moments — don't confuse them
  - This is the cluster's **second** approval: the final sign-off at AT3, on the deployed and tested improvement.
  - The **first** was the AT1 deploy sign-off — the approval to proceed to deployment, on the design (Topic 4).
  - The first gate authorised the build; this gate accepts the result and closes the cluster.
  image: none
- [EX] Write the report section & rehearse the final sign-off
  - For the practice engagement (the website vehicle), write the as-deployed / test-results section of the Deployment Report — highlight the changes from the approved design.
  - Rehearse the final sign-off conversation to a mock panel: walk the report, confirm the goals met, and obtain acceptance.
  - Produce it before finalising the assessed Ledgerline report — this is the practice run.
  timer: ~30 min
  image: none
- [TAKEAWAYS] Topic 8 · Key takeaways
  - Document the as-deployed architecture and test results, highlighting the changes and improvements from the approved design.
  - Create the deployment and testing step documentation from your live-captured evidence — repeatable by a reader.
  - Describe the long-term improvement strategy and its benefits — the DB-tier DR and other next-iteration improvements.
  - Obtain and record the final sign-off — the AT3 gate that accepts the deployed system, distinct from the AT1 deploy sign-off.
  image: none

### Close
- [BESPOKE] Cluster complete
  - AT3 is documented, refined and signed off — the deployed improvement is accepted against the approved design.
  - You analysed the baseline (AT1), designed and got the design approved (AT1), led the build (AT2), deployed and tested it (AT3), and closed it with the final sign-off.
  image: none

## Build notes
~11 slides. No new build — documentation, long-term strategy and final sign-off on the Topic 7 deployment. One `[EX]` writes the as-deployed report section and rehearses the final sign-off on the website practice vehicle. One `[TABLE]` gives the Deployment Report structure (as-deployed vs approved design, test results, long-term strategy, sign-off record). One decorative `gen` image (opener hero); no technical diagram. The DB-tier DR (design-level here) is the headline long-term-strategy item.

## Changelog
- 2026-07-02 — authored to full content.
