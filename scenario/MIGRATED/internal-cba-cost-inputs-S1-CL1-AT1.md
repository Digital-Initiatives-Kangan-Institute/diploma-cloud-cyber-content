# ICT Cost Baseline — Learning Management System (FY26)

**Relevant to:** S1-CL1 AT1

**UoC references this document supports:** Provides YAT-internal cost and operational planning data drawn on by consultants and YAT staff. Supports student evidencing of [ICTICT517 PC 3.1] (action-plan development with cost grounding), [ICTICT517 KE 1] (action-plan knowledge requirements), and [ICTICT517 FS Numeracy] (numerical interpretation + financial-implication analysis) via the AT1 CBA work. The document itself is reference data, not an action plan.

**Source status:** 🟢 Reframed 2026-05-26 from the prior `internal-cba-cost-inputs-S1-CL1-AT1.md` (which addressed the consultant directly with "what this pack provides / does not provide" framing) into an in-world YAT-internal cost baseline document per the `scenario/website.md` §2.1 in-world-only principle. All dollar figures preserved verbatim from the prior version — they remain Claude-proposed plausible values for the YAT scenario, **not** real YAT figures. **TBD** confirm or replace with real planning figures before live delivery. File rename from `internal-cba-cost-inputs-S1-CL1-AT1.md` → `internal-ict-cost-baseline-S1-CL1-AT1.md` is **TBD-confirm**.

---

## Document control

| | |
|---|---|
| Document title | ICT Cost Baseline — Learning Management System (FY26) |
| Document owner | YAT ICT Manager (Sam Walker, TBD-confirm) |
| Prepared by | YAT ICT in conjunction with YAT Finance |
| Effective from | FY26 commencement |
| Review cycle | Annual, or on material change to LMS operating model |
| Classification | Internal — ICT, Finance, and engaged consultants on signed MSA |
| Currency | Australian Dollars (AUD), exclusive of GST, at 2026 price levels |

---

## 1. Purpose

This document sets out the cost baseline for YAT's current on-premises Learning Management System (LMS) and the common planning assumptions used by ICT when evaluating changes to the LMS operating model. It draws together cost lines from the FY26 ICT operating budget, facilities allocations, software licensing records, and YAT's existing external support contracts.

The document is referenced when ICT reviews, change proposals, or external engagements (such as the in-flight LMS Cloud Migration project) need a consistent, current view of what the LMS costs YAT today.

## 2. Common planning assumptions

| Assumption | Value | Source |
|---|---|---:|
| LMS user population | ~800 students + ~60 staff | `public-org-structure.md` |
| Concurrent users (typical / peak) | 200–300 / 500–700 | `internal-lms-application-spec-S1-CL1-AT1.md` |
| Annual student growth | +15% per year | YAT Business Objectives — affects capacity-planning assumptions in out-years |
| Current measured LMS availability | 99.2% | `internal-lms-migration-role-brief-S1-CL1-AT1.md` |
| Target LMS availability | 99.9% | YAT ICT Strategic Plan |
| Indicative cost of downtime to YAT | $750 per hour during teaching hours, $0 outside teaching hours | TBD — YAT-estimated; reflects student impact, staff productivity, reputational risk |
| Fully-loaded ICT FTE cost | $115,000 per FTE / year | TBD — reflects salary + superannuation + on-costs |
| ICT planning horizon for LMS | 5 years | YAT ICT Strategic Plan |
| Productive hours per FTE per year | ~1,820 | YAT Finance convention |

## 3. Current on-premises LMS — cost baseline

### 3.1 Recurring operating costs (per year)

These are the actual costs YAT incurs today to operate the LMS on-premises.

| Category | Item | Annual cost |
|---|---|---:|
| Software licensing | Windows Server Standard (per-server) | $1,500 |
| | Antivirus / EDR (server) | $300 |
| | Monitoring and management tooling | $2,000 |
| Power and facilities | Electricity for LMS server + cooling allocation | $1,200 |
| | LMS share of server-room rent / cooling allocation | $5,000 |
| | UPS battery replacement (amortised annually) | $500 |
| Backup | Tape media (annual consumption) | $1,500 |
| | Offsite tape storage service contract | $2,400 |
| | Backup software maintenance | $1,500 |
| Staff time (YAT ICT) | LMS administration, patching, monitoring (~0.20 FTE) | (apply $115k FTE rate) |
| | Incident response (~0.05 FTE) | (apply $115k FTE rate) |
| External support | Current MTS application support contract (existing engagement, ongoing) | $30,000 |

### 3.2 Capital required if YAT continues on-premises

The current LMS server is approaching end-of-life; continuing the on-prem operating model requires a one-off hardware and ancillary refresh:

| Item | Cost |
|---|---:|
| Replacement LMS server (mid-range enterprise, dual PSU, RAID-10 SSDs, 5-year warranty) | $25,000 |
| Backup tape library refresh + drive | $8,000 |
| UPS upgrade (server-room rack UPS) | $3,000 |
| Migration labour to move LMS to new server (one-off, in-house) | $15,000 |

These figures are the cost basis against which any alternative operating model (managed hosting, cloud migration) is compared.

## 4. Cost categorisation framework for change proposals

When changes to the LMS operating model are evaluated, the cost lines fall into three cost-bearer categories. Any change proposal — internal or by an engaged consultant — must address all three to give YAT leadership a complete view:

1. **External consultant-priced costs** — fees payable to any engaged consultancy (e.g. MTS) for design, build, and ongoing infrastructure support work delivered under a Master Services Agreement.
2. **Direct vendor / cloud-platform costs** — fees payable directly to platform vendors (e.g. AWS service charges, Microsoft licensing not bundled into existing agreements).
3. **YAT-internal costs** — work YAT in-house IT undertakes itself. For the LMS this typically includes:
   - Project oversight + acceptance — ICT staff time during any external delivery (requirements coordination, milestone meetings, acceptance testing). Indicative: ~0.30 FTE × 6 months for a project of LMS-migration scale
   - Application deployment — installing the DOODLE LMS application onto whatever infrastructure is provided. Indicative: ~80–120 hours
   - Data migration — extract, transform, and load of the MySQL database, including post-migration verification. Indicative: ~60–100 hours
   - Cutover — parallel running of old + new environments during transition (~1–2 months of dual-running cost), DNS switch, user redirection, post-cutover incident response ramp. Indicative effort: ~40–60 hours plus the parallel-running infrastructure cost
   - Organisational change management — Change Advisory Board process per `internal-change-management-procedure.md`, end-user communications (staff + students), training collateral preparation and delivery, post-cutover support ramp. Indicative: ~80–120 hours of ICT + Administrative staff time
   - Decommissioning of any displaced infrastructure — hardware retirement, secure data destruction per `internal-privacy-policy.md` and records management obligations, facility reclamation. Indicative: ~$2,500 in materials + ~16 hours of ICT time

Apply the FTE / hours figures in §2 to convert effort estimates to dollars (1 FTE-year ≈ 1,820 productive hours).

## 5. Operational considerations and ICT priorities

In addition to direct cost comparison, the following operational factors are material to any LMS operating-model decision and are weighted by YAT leadership in change reviews:

- **Avoided downtime.** Lifting LMS availability from the current 99.2% to the target 99.9% reduces unplanned downtime by ~61 hours per year. Applying the $750/hour figure from §2 yields an indicative avoided-cost range — actual figure depends on what fraction of that downtime would have fallen during teaching hours.
- **Capacity for student growth.** The 15% annual growth trajectory requires capacity headroom across all options; capacity planning is a standing consideration in any operating-model decision.
- **Capacity for assessment-week peaks.** The LMS sees approximately 3× concurrent load during the two-week assessment submission windows each term. Any operating model must handle these peaks without degradation.
- **Staff capability development.** YAT ICT staff currently have limited cloud-operations experience. Any move to a cloud operating model has implications for staff upskilling and the residual external support requirement.
- **Vendor dependency, sustainability, cyber security maturity, disaster recovery (whole-campus loss), data residency.** Each is captured in YAT's broader ICT strategic-plan considerations and surfaces in any material change decision.

## 6. References

- `public-about-mission-vision.md` — YAT strategic context
- `internal-ict-strategic-plan-detail.md` — ICT five-year direction, target availability, growth assumptions
- `internal-lms-application-spec-S1-CL1-AT1.md` — LMS workload + concurrency profile
- `internal-lms-migration-role-brief-S1-CL1-AT1.md` — current engagement context
- `internal-change-management-procedure.md` — change governance referenced in §4 / §5
- `internal-privacy-policy.md` — data residency and secure-destruction obligations
