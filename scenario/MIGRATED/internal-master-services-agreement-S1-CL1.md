# Master Services Agreement — YAT College and MTS Consulting (S1-CL1)

**Relevant to:** S1-CL1 (cluster-stable across AT1, AT2, AT3)

**UoC references this document supports:**
- Provides the in-world contractual framing for the consultant engagement that AT1–AT3 sit within. No direct UoC evidencing — the document is supporting context.

**Source status:** 🟡 **PLACEHOLDER** (Claude, 2026-05-26). Section structure + authoring notes only. Full content TBD. This file replaces the previous `public-cluster-project-narrative.md` (which combined a public-homepage stub and a meta-narrative addressed to the student) — the homepage half of that file is now replaced by the marketing-style public homepage TBD content (per `scenario/website.md` §2.2), and the consultant-narrative half is replaced by this MSA reframe.

**Intranet mount point:** `/intranet/projects/lms-cloud-migration/master-services-agreement` (per `scenario/website.md` §2.3).

---

## Purpose of this document (when authored)

A standard-form Master Services Agreement between **YAT College** (client) and **MP Tech Solutions / MTS Consulting** (consultant), under which the LMS Cloud Migration engagement is performed. The MSA is the in-world contractual artefact the consultant would actually see on the YAT intranet under the project record — bounded scope, deliverables, governance, acceptance, change control, payment, IP, confidentiality, signatures.

The MSA carries the same scope-of-engagement information the previous narrative carried, but in contract form. The role brief (`internal-lms-migration-role-brief-S1-CL1-AT1.md`) remains as a separate **operational** working document and is referenced from the MSA but not absorbed into it.

---

## Section-by-section authoring notes

### 1. Parties

- **Client:** YAT College Pty Ltd, RTO based at 175 Cremorne Street, Cremorne VIC 3121 (per `public-locations-campus.md`).
- **Consultant:** MP Tech Solutions Pty Ltd, trading as MTS Consulting. *(Address + ABN — TBD placeholder.)*
- ABN + ACN values TBD (use plausible 11-digit ABN placeholders, not real-company numbers).

### 2. Recitals / Background

Three short recitals:

1. YAT operates a self-hosted on-prem LMS that is approaching end-of-life and no longer meets capacity, availability, and growth requirements set out in YAT's ICT strategic plan (ref `internal-ict-strategic-plan-detail.md`).
2. YAT has determined to undertake a phased cloud migration of the LMS, with cloud infrastructure work delivered by an external consultancy and application + cutover work retained in-house.
3. YAT has selected MTS to provide the cloud infrastructure services described in this Agreement.

### 3. Definitions

Light, only what the rest of the document depends on:

- *Services* / *Deliverables* / *Acceptance* / *Working Day* / *Business Hours* (with explicit teaching-hours definition referencing the indicative-cost-of-downtime figure)
- *Change-Management Procedure* — the YAT procedure at `/intranet/policies/change-management`, expressly incorporated by reference
- *Site* — the YAT Cremorne campus + YAT-controlled cloud environment

### 4. Services / Scope of work

The substantive scope. Three phases mapping to the three ATs:

| Phase | Description | Aligns to |
|---|---|---|
| Phase 1 — Analysis & Business Case | Strategic analysis, gap analysis, 5-year CBA, prioritised action plan, board-ready Business Case + presentation | S1-CL1 AT1 |
| Phase 2 — Cloud Foundation Build | Implement the approved cloud architecture per the action plan: IAM, network, compute, managed database, autoscaled multi-tier application, monitoring; smoke-test infrastructure; document and obtain sign-off | S1-CL1 AT2 |
| Phase 3 — High Availability Hardening | Review the (already-deployed) cloud environment for SPOFs / recovery gaps, design and implement HA architecture (Multi-AZ database, cross-AZ ASG, etc.), simulate failure + scaling, produce closure pack for sign-off via the Change-Management Procedure | S1-CL1 AT3 |

Cross-references to scenario documents: role brief, LMS application spec, migration requirements, HA database requirements, supplied cloud architecture design (AT2 baseline).

### 5. Out of scope

Explicit and material — this is the same scope-of-engagement clarification already documented in `internal-lms-migration-role-brief-S1-CL1-AT1.md` § *Scope of the MTS consulting engagement*. Lift verbatim or reference. Out of scope items:

- LMS application installation onto the new cloud infrastructure
- MySQL database extract, transform, load, and post-migration verification
- Production cutover from on-prem to cloud (DNS switch, dual-running, user redirection, ramp)
- Organisational change management (CAB process, user communications, training, post-cutover support ramp)
- Decommissioning of the on-prem LMS server hardware
- All routine end-user support and YAT-side operational ICT activities

These remain with YAT in-house IT.

### 6. Deliverables and milestones

A short table per phase with: deliverable name, format (document / running infrastructure / report + simulation evidence), required acceptance evidence, indicative milestone date. Use *Day N* numbering rather than calendar dates — the Agreement is a template used for the case-study scenario, not a real engagement plan with fixed dates.

### 7. Term, suspension, termination

- Term commences on signature and continues until acceptance of the Phase 3 closure pack.
- Termination for convenience / for cause / for insolvency — boilerplate, brief.
- Effect of termination on partly-completed deliverables — payment for work completed to that point.

### 8. Acceptance

- Each deliverable submitted to the YAT ICT Manager for review.
- Review window (e.g. 5 Working Days) within which YAT either accepts or rejects with reasons.
- Re-submission cycle on rejection.
- Phase advance requires Phase-N acceptance — keeps the assessment cluster in proper sequence.

### 9. Change control

Substantive changes to scope, deliverables, or timing follow the YAT Change-Management Procedure incorporated by reference (see §3). Captures change requests in writing, approval via YAT's Change Advisory Board where the change crosses operational impact thresholds, and the change is then reflected in a signed variation to this Agreement.

### 10. Governance and key contacts

Light governance — the principals on each side, escalation path, meeting cadence, status reporting.

- **YAT side:** ICT Manager **Sam Walker** (project sponsor + acceptance authority); Sam reports operational status to the YAT Executive.
- **MTS side:** Senior Consultant **Pat Lin** (engagement lead); Pat reports to MTS Engagement Director (TBD name placeholder).
- The consultant working the day-to-day delivery reports to Pat; Pat liaises with Sam.

*(Names are placeholders — TBD confirm or replace before live delivery, consistent with `scenario/website.md` §9.)*

### 11. Fees and payment

Kept light — the scenario does not assess on commercial negotiation:

- Phase fees fixed-price, payable on acceptance.
- Travel + reasonable disbursements at cost, pre-approved.
- Payment terms 14 Working Days from invoice.
- All amounts in AUD exclusive of GST.
- Specific dollar amounts: TBD placeholders; should be plausible against the MTS-priced one-off cost line that appears in the AT1 CBA cost baseline (now `internal-ict-cost-baseline-S1-CL1-AT1.md` once reframed).

### 12. Confidentiality and data protection

- Confidential information protected; standard exceptions (publicly available, independently developed, etc.).
- Personal information handled per the Australian Privacy Act and YAT's `internal-privacy-policy.md`.
- Data residency: YAT data processed and stored in Australia (`ap-southeast-2`) per `internal-privacy-policy.md`.
- Data deletion / return on termination.

### 13. Intellectual property

- Pre-existing IP retained by each party.
- New IP created specifically for YAT under this Agreement assigned to YAT on payment.
- Background tooling, scripts, generic patterns the consultant uses across engagements remain MTS IP, licensed to YAT for use within the engagement scope.

### 14. Warranties, liability, insurance

Boilerplate but brief:

- Services performed with reasonable skill and care, by appropriately qualified personnel.
- Insurance — professional indemnity + public liability minimums (TBD placeholder figures).
- Liability cap — typically a multiple of fees paid; exclusions for confidentiality breach, IP infringement, wilful default.

### 15. General provisions

- Governing law: Victoria, Australia.
- Dispute resolution: good-faith discussion → mediation → courts of Victoria.
- Notices: in writing to the addresses in the signature block.
- Entire agreement, no waiver, severability, counterparts, assignment.

### 16. Signatures

Two signature blocks — YAT (signed by the appropriate authority — likely the CFO or COO given the materiality) and MTS (signed by the Engagement Director or Managing Director). Witnessed where required.

---

## TBD items (consolidated)

- Specific ABN / ACN placeholders for both parties
- Specific dollar amounts in §6 (deliverable milestone fees), §11 (payment terms), §14 (insurance minimums + liability cap)
- Specific milestone dates in §6 — proposed: Day-numbered rather than calendar
- Confirmation of named contacts (Pat Lin / Sam Walker) — consistent with the cross-document TBD on role-played names
- MTS legal entity full name + address — to date "MP Tech Solutions trading as MTS Consulting" with no registered address

## Authoring sources when content is drafted

| MSA section | Primary content sources |
|---|---|
| §2 Recitals | `internal-ict-strategic-plan-detail.md`, `public-about-mission-vision.md` |
| §4 Scope | `internal-lms-migration-role-brief-S1-CL1-AT1.md`, `internal-lms-cloud-migration-requirements-S1-CL1-AT1.md` |
| §5 Out of scope | `internal-lms-migration-role-brief-S1-CL1-AT1.md` § *Scope of the MTS consulting engagement* (already authored) |
| §6 Deliverables | The three AT assessment specs (S1-CL1-AT1 / AT2 / AT3 .docx) — translated from assessment-task language to deliverable-handover language |
| §9 Change control | `internal-change-management-procedure.md` (incorporated by reference) |
| §10 Governance | `public-org-structure.md` for YAT-side names + roles |
| §12 Privacy / data | `internal-privacy-policy.md` |
