# Topic 03 Designing for scalability and the four components — Slide plan
> **Covers:** Topic 03 — see coverage.md
> **Subtitle:** Design the scalability improvements by selecting and improving the four resource tiers
> **STATUS: DRAFT** (authored 2026-07-02).

## Depth ceiling
DESIGN — design the scalability improvements on paper and select/improve the four resource tiers to Ledgerline's business needs; the build is AT3. Scalability = elastic capacity-on-demand, demonstrable by test — not a load forecast. Justify each choice; do not implement, and do not over-provision.

## Teaching source
AWS performance/scalability pillar (elastic capacity, auto scaling, resource selection); bespoke for the four-component allocation framing and the object-storage-in-context contrast.

## AWS pin table
TBD — AWS scalability/architecture modules to be pinned.

## Slides

### Opener
- [BESPOKE] The scalability half of the design
  - Topic 3 continues AT1: you design the scalability improvements for Ledgerline (single-AZ cloud).
  - Structure the design by four resource components — network, compute, database, storage — the same four units the AT2 team later divides the IaC write by.
  - Scalability here means elastic capacity-on-demand, demonstrable by test at AT3 — not a forecast, and not over-provisioning.
  - Design only, to the business needs — the build is AT3.
  image: gen flat vector hero illustration of four cloud resource tiers network compute database storage scaling elastically, blue and gold accents, minimal, no text

### C1 — The four resource components
- Teaches: [ICTCLD504 PC 2.2]
- Kicker: select and improve each tier to the business needs
- [PRIMER] Scalability = elastic capacity-on-demand
  - Elastic capacity: add resources as load rises, release them as load falls — pay for what you use.
  - The test of a scalable design is a demonstration: it scales on demand (proven at AT3), not a load forecast on paper.
  - Over-provisioning fixed spare capacity is not scalability — it is gold-plating; right-size instead.
  image: none
- [BESPOKE] The four resource components
  - Split the design across four tiers: network, compute, database, storage.
  - Compute and storage are the tiers that scale elastically on demand; network and database are selected and configured to support that scale.
  - These are the same four units the AT2 team later divides the IaC write by — a clean seam from design to build.
  image: diagram four-components
- [BESPOKE] Selecting and improving each tier
  - Network: right-size the path and load-spreading so the tier below can scale out behind it.
  - Compute: move from fixed capacity to a pool that grows and shrinks on demand (auto scaling).
  - Database: select a managed data service that scales reads without a rebuild; keep Ledgerline's accounting data consistent.
  - Storage: select storage that grows on demand rather than a fixed-size volume.
  image: none
- [BESPOKE] Justify against the business needs
  - Tie every resource choice to a stated Ledgerline business need — why this tier, why this size.
  - Choose the simplest option that meets the need; note where capacity scales elastically and how it would be demonstrated by test.
  - Do not over-engineer: no tier scaled beyond what a need justifies.
  image: none
- [EX] Design the four tiers for the practice engagement
  - For the practice-vehicle engagement, select and improve the network, compute, database and storage tiers to its business needs.
  - Mark where capacity scales elastically, and justify each choice against a named need.
  timer: ~30 min
  image: none

### C2 — Object storage in context
- Teaches: [ICTCLD504 KE 6]
- Kicker: contrast a stateful system with an object-storage-dependent one
- [PRIMER] Object storage for static web sites
  - Object storage holds whole objects (files) addressed by key — it scales storage on demand and serves static assets directly.
  - It is the natural home for a static web site's content: HTML, images, downloads served without a server.
  - Contextual knowledge here — not a Ledgerline requirement, but the contrast that sharpens what Ledgerline's storage actually needs.
  image: none
- [BESPOKE] Ledgerline vs a static-website workload
  - Ledgerline is a stateful accounting system: transactional, consistent, database-backed — object storage is not its primary store.
  - An object-storage-dependent static-website workload is the opposite: its content lives in object storage and scales with it.
  - Be able to explain how you would provision object storage for such a workload if the need arose.
  image: none
- [EX] Answer the object-storage-in-context question
  - Contrast Ledgerline's storage needs with an object-storage-dependent website workload.
  - Explain how you would provision object storage for the website workload if it were needed.
  timer: ~15 min
  image: none
- [TAKEAWAYS] Topic 3 · Key takeaways
  - Scalability = elastic capacity-on-demand, demonstrable by test — not a forecast, not over-provisioning.
  - Design across four resource components: network, compute, database, storage — the AT2 IaC seam.
  - Justify each tier against a Ledgerline business need; right-size, choose the simplest that fits.
  - Object storage suits static-website workloads; Ledgerline is stateful and database-backed — know the contrast.
  image: none

### Close
- [BESPOKE] Next: Topic 4 — document, present & sign-off
  - You've designed the scalability half across the four components; next you document and present the Solution Design for sign-off.
  - Bring these resource selections and their justifications — they are the core of the design.
  image: none

## Build notes
~11 slides. Exercises run on the practice-vehicle engagement (design only). One generated diagram (`diagram four-components` — the four tiers network/compute/database/storage with elastic-scaling indicators on compute and storage); one decorative `gen` image (opener hero).

## Changelog
- 2026-07-02 — authored to full content from coverage.md.
