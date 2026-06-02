# AWS recorded demos — catalogue (CL1)

**Purpose.** The AWS Academy decks ship **recorded demonstrations** (and a few educator-led demo slides). These are the ready-made **"demonstrate" step** for the `teach → demonstrate → practice` flow on AWS practicals — per the delivery principle *"a demonstration may be a recorded video where one is available"* rather than a live in-class demo. This catalogue itemises every demo found, mapped to the CL1 topic that can leverage it.

**Source / licence.** All demos live inside `original-materials/AWS-Instructor Presentations/…` — the AWS Academy decks are **instructor-facing, do-not-distribute-to-students**. Use them as the demo a trainer plays/screens in class; don't republish to students. (The bespoke ICTCLD502 decks contain no recorded demos — AT3's demos come from ACA M10 / M06.)

**How to use in a deck.** On a `[DEMO]` slide for an AWS practical, prefer the recorded demo below; cue it (deck · slide) in the slide + speaker notes, and fall back to a live instructor demo only where no recorded demo fits.

---

## By topic (the build sequence)

### Topic 6 — Build foundations *(IAM, shared responsibility)*
| Demo | Source · slide | Use |
|---|---|---|
| **Recorded demo: IAM** | ACF M04 · S31 | C2 IAM build (create users/groups/roles/MFA) — the demonstrate step |
| *Educator-Led Demo: AWS Global Infrastructure* | ACF M03 · S06 | conceptual (Regions/AZs) — mostly Topic 1; optional context |

*No recorded demo fits the C1 account/Region/evidence workspace setup → that demo stays live/bespoke.*

### Topic 7 — Network & security base *(VPC, security groups, DNS)*
| Demo | Source · slide | Use |
|---|---|---|
| **Recorded Amazon VPC demonstration** | ACF M05 · S30 | VPC + subnets build |
| **Demo: Creating an Amazon VPC in the Console** (VPC + security groups + Elastic IP) | ACA M07 · S30 | deeper VPC + SG build — strong fit |
| **Demo: Route 53 — Failover Routing** | ACA M10 · S52 | DNS (failover relevant later in AT3; simple DNS here) |
| *Demo: Route 53 — Simple / Geolocation Routing* | ACA M10 · S51 / S53 | simple routing useful; geolocation out of YAT scope |

### Topic 8 — The workload tier *(EC2/EBS, ALB+ASG, RDS, S3)*
| Demo | Source · slide | Use |
|---|---|---|
| **Recorded Amazon EC2 demonstration** | ACF M06 · S35 | EC2 launch/config |
| **Demo: Configuring an EC2 Instance with User Data** | ACA M05 · S59 | EC2 bootstrapping |
| *Demo: Reviewing the Spot Instance History* | ACA M05 · S65 | Spot — out of YAT baseline scope |
| **Recorded demo: Amazon Elastic Block Store (EBS)** | ACF M07 · S15 | EBS volumes |
| **Recorded demo: Amazon S3** | ACF M07 · S35 | S3 buckets |
| **Recorded demo: Amazon S3 Glacier** | ACF M07 · S55 | Glacier (7-yr retention — esp. the Accounting practice) |
| **Demo: Managing Lifecycles in Amazon S3** | ACA M04 · S36 | S3 lifecycle → Glacier (retention) |
| **Demo: Amazon S3 Versioning** | ACA M04 · S43 | S3 versioning |
| *Demo: S3 Transfer Acceleration* | ACA M04 · S26 | out of YAT scope |
| *Recorded demo: Amazon EFS* | ACF M07 · S43 | EFS not in the YAT design |
| **Recorded demo: Amazon RDS console** | ACF M08 · S22 | RDS provisioning |
| **Demo: Amazon RDS Automated Backup & Read Replicas** | ACA M06 · S37 | RDS backups (RPO) + read replicas → Multi-AZ readiness (AT3) |
| *Recorded demo: Amazon DynamoDB console* | ACF M08 · S37–38 | DynamoDB (NoSQL) — not used (YAT is MySQL / SQL Server) |
| **Demo: Creating Scaling Policies for EC2 Auto Scaling** | ACA M10 · S26 | ASG scaling policy |

### Topic 9 — Operability & justification *(CloudWatch, testing)*
*Drawn from ACA M10 monitoring content; no standalone recorded demo isolated specifically for CloudWatch — confirm when Topic 9 is built.*

### AT3 — High Availability *(Topics 11–14)*
| Demo | Source · slide | Use |
|---|---|---|
| **Demo: Creating a Highly Available Application** | ACA M10 · S44 | the core HA build demo |
| **Demo: Route 53 — Failover Routing** | ACA M10 · S52 | DNS failover for HA |
| **Demo: Amazon RDS Automated Backup & Read Replicas** | ACA M06 · S37 | Multi-AZ / replica readiness |
| **Demo: Creating Scaling Policies for EC2 Auto Scaling** | ACA M10 · S26 | autoscaling for availability |

### Topic 1 — Cloud literacy *(already built — for reference)*
| Demo | Source · slide |
|---|---|
| Recorded demo: Amazon Billing dashboard | ACF M02 · S46–47 |
| Educator-Led Demo: AWS Global Infrastructure | ACF M03 · S06 |

---

## Notes

- **Relevance flags** (*italic* rows above) mark demos that exist but fall outside the YAT/Accounting scope (DynamoDB, EFS, Spot, S3 Transfer Acceleration, geolocation routing) — skip unless scope changes.
- Slide numbers are from the canonical (non-duplicated) copies of the decks; verify against the deck when isolating.
- This complements `aws-deck-catalogue-draft.md` (deck→topic mapping); this file is specifically the **demo→demonstrate-step** mapping.
