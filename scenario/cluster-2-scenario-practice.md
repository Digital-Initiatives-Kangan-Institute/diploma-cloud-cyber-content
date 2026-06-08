# Cluster 2 — Scenario (Practice)

> **Role:** Practice · **Vehicle:** LMS · per `scenario-flow.md`.
>
> Lean cluster-and-role delta — see `scenario-flow.md`, `cluster-2-scenario-assessment.md`, and the LMS ICT records. Meta/design doc.

## 1. Engagement

Students rehearse the CL2 skills — DR planning, web-scale design, the audit microservice, and IaC — on the **LMS**: the system they already know from CL1, and which is already cloud-hosted and highly available. The LMS is a credible **web-scale** practice vehicle because it plausibly carries a large **authenticated** student user base.

## 2. Scenario deltas

- **Web-scale-credible:** the LMS plausibly carries a large, peaky user base (assessment-window spikes), so global-serving / scale-out practice is realistic on it.
- **Already cloud + HA:** practice starts from a known, hardened architecture, so effort goes into the CL2 skills (DR, web-scale, microservice, IaC) rather than learning the system.
- **Practice ↔ assessment contrast — authenticated vs anonymous.** The one deliberate distinction between practice and assessment: the LMS (practice) serves an **authenticated student cohort**, whereas the website (assessment) serves **anonymous public traffic** (prospective students worldwide). This difference is real and free, and it naturally pulls different web-scale concerns into the website design — CDN / edge caching, WAF and bot/DDoS mitigation, and SEO — that the logged-in LMS does not need. Students should let that shape the website answer rather than transposing the LMS one. **Beyond this natural axis the two engagements are deliberately kept similar — no other contrived differentiation.**

## 3. Vehicle state

The LMS in its **Multi-AZ HA** cloud state — held in `lms-application-spec-cloud.md`, the LMS Infrastructure Specifications, and the HA-hardened ICT records.

## 4. Practised focus

Rehearses the CL2 assessment units **ICTCLD501 / 503 / 505** on the LMS, ahead of assessment on the website.

## 5. References

- `scenario-flow.md`; `cluster-2-scenario-assessment.md` — the website assessment
- Intranet: the LMS cloud + HA-hardened ICT records
