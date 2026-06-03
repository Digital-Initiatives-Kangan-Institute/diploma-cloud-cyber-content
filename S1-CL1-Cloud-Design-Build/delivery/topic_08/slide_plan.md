# Topic 8 — The workload tier · Slide plan

Build sheet for the two decks → `Topic_08a_Slides.pptx` (C1 Compute + C2 Elasticity) and `Topic_08b_Slides.pptx` (C3 Database + C4 Storage). Satisfies `coverage.md`. **Disposable scaffold** — delete once both decks are built.

**Markers.** `[PRIMER]` vendor-neutral fundamentals · `[AWS Mx Sy]` author from the pinned AWS slide (reuse-first) · `[BESPOKE]` author from inline brief (gap) · `[DEMO]` recorded AWS demo (live only if none fits) · `[EX]` lab activity. Per-concept: `[PRIMER] → [AWS] teach → [DEMO] → [EX]`. Accents reuse A1/A2/A3 (= MAGENTA/SKY/GREEN); topic-level slides GOLD.

## AWS slides to draw from + paste images (exact refs — decks read 2026-06-03)

| Pin | Deck · slide(s) | Used on |
|---|---|---|
| EC2 overview / VM | **ACF M06** · S9–S10 | 8a C1 teach |
| Launch choices (AMI, type, network, role, user-data, storage, tags, SG, key pair) | **ACF M06** · S11–S26 | 8a C1 teach |
| Instance types (family.gen.size; CPU/RAM/storage/network) | **ACF M06** · S14–S16 | 8a C1 teach |
| EBS = durable block storage (vs instance store) | **ACF M06** · S22 · **ACF M07** · S15 (EBS demo) | 8a C1 teach |
| **Recorded demo: EC2** | **ACF M06** · **S35** | 8a C1 demo |
| Elasticity; vertical vs horizontal scaling | **ACA M10** · S19 | 8a C2 primer |
| EC2 Auto Scaling (ASG, launch template, min/desired/max, policies) | **ACA M10** · S20–S24 | 8a C2 teach |
| Load balancer + target group + health check | **ACA M07** (Topic 7 context) · **ACA M10** load-balancer section | 8a C2 teach |
| **Recorded demo: Auto Scaling policies** | **ACA M10** · **S26** | 8a C2 demo |
| Relational DB; self-hosted vs managed (EC2 vs RDS) | **ACF M06** · S44 (activity) · **ACF M08** · early | 8b C3 primer |
| Amazon RDS (engines, instance class, storage, backups, encryption, Multi-AZ named) | **ACF M08** · RDS slides · **ACA M06** | 8b C3 teach |
| **Recorded demo: RDS console** | **ACF M08** · **S22** | 8b C3 demo |
| RDS automated backups (RPO) | **ACA M06** · **S37** (demo) | 8b C3 demo/teach |
| Storage types (block/object/archive); S3 | **ACF M07** · S35 (S3), S55 (Glacier) | 8b C4 primer + teach |
| S3 lifecycle → Glacier (retention) | **ACA M04** · **S36** (demo) | 8b C4 demo |
| S3 versioning | **ACA M04** · **S43** (demo) | 8b C4 demo |
| **Recorded demos: S3 / Glacier** | **ACF M07** · **S35**, **S55** | 8b C4 demo |

---

## Deck 8a — Compute & elasticity (~21 slides)

1. **title_slide** "08a · The workload tier — compute & elasticity" / "Launch the application server, give it storage, put it behind a load balancer that scales."
2. **content_slide** opener — Topic 7 built the network; now the workload moves in. 8a = compute + elasticity; 8b = database + storage. Still building the design + evidencing; watch the demo then do it.

### C1 — Compute (EC2 + EBS) · A1
3. **divider** "01" · "Compute — the application server" · "EC2 + EBS"
4. **content** `[PRIMER]` "What a server is — and a virtual one" — a server runs the app; CPU/RAM/disk/network are its dimensions; a VM is a software-defined server you size to the workload.
5. **content** `[AWS ACF M06 S10]` "Amazon EC2" — resizable VMs, full OS control (Win/Linux), launch from an AMI into a subnet in minutes, control traffic via SGs.
6. **content** `[AWS ACF M06 S11–S26]` "Launching an instance — the key choices" — AMI · instance type (family.gen.size = CPU/RAM/storage/network) · network (VPC/subnet) · IAM role (instance profile) · user data · storage (root+data) · tags · security group · key pair.
7. **content** `[PRIMER + AWS ACF M06 S22]` "Storage on the instance — EBS (block)" — block storage = a virtual disk attached to one instance; EBS durable (survives stop/start) vs instance store ephemeral; gp3 SSD; resize without downtime.
8. **content** `[BESPOKE — design]` "The compute you'll build" — EC2 Win Server 2016 (m6i.large*, C1) in private-app-a, no public IP; instance role for RDS/S3/CloudWatch; sg-app; EBS gp3 root 80 GB + data volume (footprint+growth+headroom).
9. **demo** `[DEMO recorded]` "Launch an EC2 instance" — `source="ACF M06 · EC2 (S35)"`.
10. **activity** `[EX]` "Launch the Ledgerline server" (~25 min) — launch per design (AMI, type, private-app-a, role, sg-app, tags) + add the gp3 data volume; capture evidence (instance, volumes, Region).
11. **takeaways** "Section 1 · Compute".

### C2 — Elasticity (ALB + Auto Scaling) · A2
12. **divider** "02" · "Elasticity — load balancing & scaling" · "ALB + Auto Scaling"
13. **content** `[PRIMER + AWS ACA M10 S19]` "Load balancing & scaling" — a load balancer spreads traffic + health-checks targets; elasticity = grow/shrink to demand; vertical (bigger) vs horizontal (more) scaling — the cloud way.
14. **visual** `[AWS ACA M10 / ACA M07]` "The Application Load Balancer" — listener (HTTPS:443) → target group → healthy targets only; internal vs internet-facing. *Placeholder: AWS — ALB + target group.*
15. **visual** `[AWS ACA M10 S20–S24]` "Auto Scaling groups" — ASG from a launch template; min/desired/max; replaces unhealthy; policies (scheduled / target-tracking / step); ALB health-check integration. *Placeholder: AWS — horizontal scaling with an ASG (ACA M10 S22).*
16. **content** `[BESPOKE — design]` "The elasticity you'll build" — internal ALB HTTPS:443 → target group = the ASG; ASG min1/desired1/max2, target-tracking CPU 70%, ELB+EC2 health checks, 300 s cooldown; baseline (HA adds cross-AZ in AT3).
17. **demo** `[DEMO recorded]` "Create an Auto Scaling policy" — `source="ACA M10 · Scaling policies (S26)"`.
18. **activity** `[EX]` "Behind the ALB + ASG; test scaling" (~25 min) — create internal ALB + target group + listener; launch template + ASG (min1/max2, target-tracking); **test scaling** (drive the metric; watch scale-out/in), fix errors; capture evidence. *(PC 3.1, 3.2.)*
19. **takeaways** "Section 2 · Elasticity".

### Close
20. **takeaways** "Topic 8a · Key takeaways" (GOLD).
21. **close_slide** "Next: Topic 8b — the data tier (RDS + S3)" (GOLD).

---

## Deck 8b — Database & storage (~19 slides)

1. **title_slide** "08b · The workload tier — data & storage" / "Provision the managed database and the object storage the application relies on."
2. **content_slide** opener — compute is built; now the data tier. 8b = managed database (RDS) + object/archive storage (S3 + Glacier). Build the design + evidence; watch the demo then do it.

### C3 — Managed database (RDS) · A1
3. **divider** "01" · "The managed database" · "Amazon RDS"
4. **content** `[PRIMER]` "Databases, and who runs them" — a relational database stores structured data (tables); someone must patch/back-up/secure it; **self-hosted** (you do it on EC2) vs **managed** (the cloud does it).
5. **content** `[AWS ACF M06 S44 / ACF M08]` "Self-hosted vs managed — EC2 vs RDS" — RDS handles provisioning, patching, automated backups, restore, monitoring; EC2 gives full control but all the work.
6. **content** `[AWS ACF M08 / ACA M06]` "Amazon RDS" — engines (incl. SQL Server); instance class; gp3 storage; automated backups + point-in-time restore; encryption at rest; Multi-AZ (named — **deferred to AT3**).
7. **content** `[BESPOKE — design]` "The database you'll build" — RDS for SQL Server Standard (db.m6i.large*, C2; licence model C3); gp3 ~22 GB + growth; private-data-a, not public; Multi-AZ off (baseline); automated backups RPO ≤ 1 h; KMS encryption; **MTS provisions an empty instance** (schema/data = YAT ICT).
8. **demo** `[DEMO recorded]` "Provision an RDS database" — `source="ACF M08 · RDS console (S22)"` (+ ACA M06 S37 for backups).
9. **activity** `[EX]` "Provision the Ledgerline database" (~20 min) — RDS for SQL Server per design (class, storage, private-data-a, sg-db, backups, encryption); **test app→db connectivity** (completes PC 2.6); capture evidence.
10. **takeaways** "Section 1 · Managed database".

### C4 — Object & archive storage (S3 + Glacier) · A2
11. **divider** "02" · "Object & archive storage" · "S3 + Glacier"
12. **content** `[PRIMER]` "Block vs object vs archive" — block (a disk on one instance: EBS) · object (files+metadata via API, virtually unlimited: S3) · archive (cheap, slow-retrieve, long-term: Glacier).
13. **content** `[AWS ACF M07 S35]` "Amazon S3" — buckets + objects; durable; block-public-access; encryption (SSE); versioning; access via IAM/endpoints.
14. **content** `[AWS ACF M07 S55 / ACA M04 S36]` "Lifecycle to Glacier — retention" — lifecycle rules transition objects to Glacier; Object Lock for write-once retention — the 7-year financial-records hold.
15. **content** `[BESPOKE — design]` "The storage you'll build" — Documents bucket (→ Glacier, 7-yr) + Backups bucket; both: block public access, SSE(-KMS), versioning, access logging; Object Lock considered for the financial hold.
16. **demo** `[DEMO recorded]` "S3 buckets, versioning & lifecycle" — `source="ACA M04 · S3 lifecycle (S36) + versioning (S43)"` (+ ACF M07 S35/S55).
17. **activity** `[EX]` "Create the buckets per the design" (~15 min) — Documents + Backups buckets; block public access; enable versioning + encryption; add the lifecycle rule to Glacier; capture evidence.
18. **takeaways** "Section 2 · Object & archive storage".

### Close
19. **takeaways** "Topic 8 · Key takeaways" (GOLD) — the whole workload tier (compute, elasticity, database, storage) now sits in the network; built to the design, tested, evidenced.
20. **close_slide** "Next: Topic 9 — operability & justification (CloudWatch, testing, justifying the build)" (GOLD).

---

## Notes
- **Reuse-first:** nearly every build step has a recorded AWS demo — use them; no live demos expected in Topic 8.
- **Depth ceiling:** single-AZ baseline, Multi-AZ **off**, ASG min1/max2 (elasticity intro, not HA). HA → AT3.
- **PC 3.2** (test scaling) lands in 8a C2; **PC 2.6** (app→db connectivity) completes in 8b C3.
- **Practice scenario:** Accounting/Ledgerline; assessed LMS is the same structure (public ALB; RDS MySQL).
