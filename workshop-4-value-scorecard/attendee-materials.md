# Workshop 4 — Attendee Materials
## Value and Risk Scorecard

**Version:** 1.0
**Session date:** [DATE]
**Facilitator:** [FACILITATOR]

---

## What this document is

This is your reference and working sheet for Workshop 4. Bring it to the
session — either printed or open on your device.

Some sections have space to capture measures, baselines, and target
directions as we agree them in the room. Nothing needs to be completed
in advance.

---

## What we are doing today

Workshop 4 looks at the other side of the equation. We have built a cost
model and a unit economics picture. Today we build a value and risk
scorecard — what the platform enables, what it protects, and what would
be at risk if cost decisions were made without considering it.

By the end of this session we will have:

- A value and risk scorecard — eight to twelve agreed measures
- Baseline values with confidence ratings
- Target directions for each measure
- A narrative connecting platform cost to platform value

---

## Why this matters

Cost without value is an incomplete picture.

When leadership only sees cost, they optimise in one dimension — and
often shift cost somewhere less visible, into incidents, audit failures,
or developer friction.

The scorecard gives leadership a balanced view and gives the platform
team something they often lack: a way to articulate value in terms
leadership recognises.

---

## The four scorecard categories

| Category | What it measures |
|----------|----------------|
| Delivery performance | How effectively the platform enables teams to ship changes safely and quickly |
| Reliability | How stable the platform is and how quickly it recovers when things go wrong |
| Security and compliance effort | How much effort the platform requires and reduces for security and compliance |
| Developer experience | How much friction developers experience when building and deploying |

---

## A note on proxies

Not every organisation tracks these measures formally. That is fine.

For each measure where direct data is not available, we agree a proxy —
an imperfect but directionally useful substitute. A proxy with a Low
confidence rating is more useful than no baseline at all.

---

## Section 1 — Delivery Performance

*Agree measures, data sources, baselines, and confidence ratings in the session.*

| Measure | Data source or proxy | Baseline value | Confidence | Target direction |
|---------|---------------------|---------------|------------|-----------------|
| Deployment frequency | | | H / M / L | |
| Lead time for changes | | | H / M / L | |
| Change failure rate | | | H / M / L | |

Proxy options if not tracked:

| Measure | Proxy |
|---------|-------|
| Deployment frequency | Release cadence per team per month |
| Lead time | Estimated time from code review to production |
| Change failure rate | Proportion of deployments followed by a hotfix or rollback |

```
Key findings from this category:
```

---

## Section 2 — Reliability

*Agree measures, data sources, baselines, and confidence ratings in the session.*

| Measure | Data source or proxy | Baseline value | Confidence | Target direction |
|---------|---------------------|---------------|------------|-----------------|
| Incident volume (per quarter) | | | H / M / L | |
| Time to restore service (MTTR) | | | H / M / L | |
| Platform availability | | | H / M / L | |

Proxy options if not tracked:

| Measure | Proxy |
|---------|-------|
| Incident volume | On-call escalations per quarter |
| MTTR | Average incident duration from on-call logs |
| Availability | Rough uptime estimate from the platform team |

```
Key findings from this category:
```

---

## Section 3 — Security and Compliance Effort

*Agree measures, data sources, baselines, and confidence ratings in the session.*

| Measure | Data source or proxy | Baseline value | Confidence | Target direction |
|---------|---------------------|---------------|------------|-----------------|
| Time to patch critical vulnerabilities | | | H / M / L | |
| Policy coverage (% of workloads) | | | H / M / L | |
| Audit evidence effort (days per cycle) | | | H / M / L | |

Proxy options if not tracked:

| Measure | Proxy |
|---------|-------|
| Time to patch | Estimated average from recent CVE responses |
| Policy coverage | Rough percentage of workloads with enforced controls |
| Audit evidence effort | Estimated person-days per audit cycle |

```
Key findings from this category:
```

---

## Section 4 — Developer Experience

*Agree measures, data sources, baselines, and confidence ratings in the session.*

| Measure | Data source or proxy | Baseline value | Confidence | Target direction |
|---------|---------------------|---------------|------------|-----------------|
| Onboarding time (new service or team) | | | H / M / L | |
| Time to first deployment | | | H / M / L | |
| Ticket and toil volume (per month) | | | H / M / L | |

Proxy options if not tracked:

| Measure | Proxy |
|---------|-------|
| Onboarding time | Estimated from recent team onboarding experiences |
| Time to first deployment | Estimated from platform team experience |
| Ticket and toil volume | Support ticket count per month or per deployment |

```
Key findings from this category:
```

---

## Section 5 — Scorecard Summary

Complete this together once all four categories are built.

| Category | Measure | Baseline | Confidence | Target direction |
|----------|---------|----------|------------|-----------------|
| Delivery performance | Deployment frequency | | H / M / L | |
| | Lead time for changes | | H / M / L | |
| | Change failure rate | | H / M / L | |
| Reliability | Incident volume | | H / M / L | |
| | MTTR | | H / M / L | |
| | Availability | | H / M / L | |
| Security and compliance | Time to patch | | H / M / L | |
| | Policy coverage | | H / M / L | |
| | Audit evidence effort | | H / M / L | |
| Developer experience | Onboarding time | | H / M / L | |
| | Time to first deployment | | H / M / L | |
| | Ticket and toil volume | | H / M / L | |

---

## Section 6 — The Value Narrative

Capture the narrative that emerges from the scorecard.

**What the platform is enabling well:**

```
Notes:
```

**Where there is room to improve:**

```
Notes:
```

**What would be at risk if cost were optimised without considering value:**

```
Notes:
```

---

## Section 7 — Questions and Notes

```
Notes:
```

---

## After this session

Within 24 hours you will receive a recap email covering:

- Decisions made in the session
- The value and risk scorecard — saved, versioned, and shared
- Workshop 5 confirmed — date, time, and what to expect

Workshop 5 is the final session. We bring everything together — cost
model, unit economics, showback view, and value scorecard — and turn
it into a decision and a plan.

---

## Glossary

| Term | Plain English |
|------|---------------|
| DORA | DevOps Research and Assessment — four metrics for software delivery performance |
| SPACE | A framework for developer productivity across five dimensions |
| Deployment frequency | How often code is successfully deployed to production |
| Lead time for changes | Time from code commit to running in production |
| Change failure rate | Percentage of deployments that cause a production failure |
| MTTR | Mean Time to Restore — average recovery time from incidents |
| Proxy | An imperfect but directionally useful substitute for a direct measurement |
| Policy coverage | The percentage of workloads governed by automated policy controls |
| Toil | Repetitive, manual, automatable work that does not add long-term value |
| Onboarding time | Time for a new service or team to reach first deployment |
| Confidence rating | H = measured, M = estimated, L = rough guess |
| Scorecard | A structured set of agreed measures with baseline and target values |
| Target direction | Whether a measure should increase, decrease, or stay the same |
