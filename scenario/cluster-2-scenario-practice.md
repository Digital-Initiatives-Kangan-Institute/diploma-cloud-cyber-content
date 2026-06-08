# Cluster 2 — Scenario (Practice)

> **Role:** Practice · **Vehicle:** LMS · per `scenario-flow.md`.
>
> Lean cluster-and-role delta — see `scenario-flow.md`, `cluster-2-scenario-assessment.md`, and the LMS ICT records. Meta/design doc.

## 1. Engagement

Students rehearse the CL2 skills — DR planning, web-scale design, the audit microservice, and IaC — on the **LMS**: the system they already know from CL1, and which is already cloud-hosted and highly available. The LMS is a credible **web-scale** practice vehicle because it plausibly carries a large student user base.

## 2. Scenario deltas

- **Web-scale-credible:** the LMS plausibly carries a large, peaky user base (assessment-window spikes), so global-serving / scale-out practice is realistic on it.
- **Already cloud + HA:** practice starts from a known, hardened architecture, so effort goes into the CL2 skills (DR, web-scale, microservice, IaC) rather than learning the system.
- **Practice ↔ assessment contrast — [TBD].** The LMS (practice) and the website (assessment) are both web / log systems, so a deliberate distinction is needed for students to transfer the skill rather than pattern-match a practised answer onto the assessment. Candidate axes: authenticated-cohort (LMS) vs anonymous-public-traffic (website) web-scale; or a distinct residency framing per system. **To settle with Tim.**

## 3. Vehicle state

The LMS in its **Multi-AZ HA** cloud state — held in `lms-application-spec-cloud.md`, the LMS Infrastructure Specifications, and the HA-hardened ICT records.

## 4. Practised focus

Rehearses the CL2 assessment units **ICTCLD501 / 503 / 505** on the LMS, ahead of assessment on the website.

## 5. References

- `scenario-flow.md`; `cluster-2-scenario-assessment.md` — the website assessment
- Intranet: the LMS cloud + HA-hardened ICT records
