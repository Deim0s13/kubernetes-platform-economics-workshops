# Kubernetes Platform Economics — Decision Brief

**Organisation:** [ORGANISATION]
**Prepared by:** [FACILITATOR]
**Version:** [VERSION]
**Date:** [DATE]
**Status:** Draft for review / Final

---

## Version history

| Version | Date | Status | Notes |
|---------|------|--------|-------|
| v0.1 | [DATE] | Draft | Shared with platform team for review |
| v1.0 | [DATE] | Final | Approved for leadership presentation |

---

## Document purpose

This brief presents the findings and recommendation from a five-workshop
platform economics assessment of [ORGANISATION]'s Kubernetes estate.

It is prepared for: [CIO] | [GM TECHNOLOGY AND OPERATIONS] | [FINANCE] |
[PROCUREMENT]

It covers what the platform estate costs today, what value it delivers,
what the realistic options are for improving cost per outcome, and what
the recommended next steps are.

The assessment used FinOps, TBM, DORA, and SPACE as reference frameworks.
Every number carries a confidence rating — High, Medium, or Low — based
on whether it is measured, estimated, or proxied. Those ratings are part
of the output, not a caveat to it.

> This document is produced after Workshop 5 and reviewed with the
> platform team before going to the leadership audience.
>
> All figures are carried forward from the working documents produced
> across Workshops 1 through 5. Do not summarise from memory — follow
> the carry-forward pointers in each section.

---

---

# Section 1 — Executive Summary

> Write this section last. It summarises what is in the sections that
> follow — not what you expect to find before writing them.
> Target length: 1 to 2 pages.

## What we assessed

> State the scope clearly and briefly.

[ORGANISATION]'s Kubernetes estate was assessed across [TIME WINDOW].
The platforms in scope for the baseline were [PLATFORMS]. [PLATFORMS]
were assessed as scenario options.

The assessment covered cloud infrastructure, managed service fees,
platform tooling, subscriptions, operating effort, and shared services.

> Carry forward from: assumptions-register.md — Section 1

## Key findings

> Five findings maximum. Lead with the most important.
> Each finding should be a statement, not a question.

1. [FINDING 1]
2. [FINDING 2]
3. [FINDING 3]
4. [FINDING 4]
5. [FINDING 5]

## Recommended path

> One paragraph. What, why, and immediate next step.

> Carry forward from: scenario-comparison.md — Recommendation section

[RECOMMENDED SCENARIO AND RATIONALE]

## Decisions required from leadership

> Surface these explicitly — not buried later in the document.

1. [DECISION 1]
2. [DECISION 2]
3. [DECISION 3]

## Immediate next steps

> Three to five actions that start regardless of leadership decisions.

1. [ACTION 1]
2. [ACTION 2]
3. [ACTION 3]

---

---

# Section 2 — Methodology

> Target length: 1 page.
> This section builds trust. Finance and Procurement will read it first.

## How we structured costs

Platform costs were organised using a TBM-aligned taxonomy — an industry
standard for classifying technology costs that Finance and IT can both
work from. Six cost buckets were used:

1. Cloud infrastructure
2. Managed service fees
3. Platform tooling
4. Subscriptions
5. Operating effort
6. Shared services

> Carry forward from: cost-taxonomy-baseline.md — Taxonomy structure

## How we allocated costs

Shared costs were allocated using FinOps allocation principles — a
standard operating model for cloud and platform cost management. The
specific rules agreed for this assessment are documented in the
Assumptions Register (see Appendix A).

The approach used showback — making costs visible to teams and products
without implementing chargeback. This is appropriate for a first-pass
assessment.

> Carry forward from: assumptions-register.md — Section 3

## How we measured value

Platform value was assessed using DORA and SPACE as reference frameworks:

- **DORA** — four metrics for software delivery performance: deployment
frequency, lead time, change failure rate, and time to restore service
- **SPACE** — developer productivity across satisfaction, performance,
activity, communication, and efficiency

Both frameworks are industry standards and are not vendor-specific.

> Carry forward from: value-risk-scorecard.md

## Confidence ratings

Every figure in this brief carries a confidence rating:

| Rating | What it means |
|--------|--------------|
| High | Based on measured data from a reliable source |
| Medium | Based on an estimate with a reasonable basis |
| Low | Based on a proxy or rough estimate — treat as indicative |

Where data was not available, the approach taken — estimate, proxy,
or exclusion — is documented in the Assumptions Register (Appendix A).

---

---

# Section 3 — Cost Baseline

> Target length: 2 to 3 pages.
> Carry all figures forward from cost-taxonomy-baseline.md.
> Do not write numbers from memory.

## Total platform cost

> Carry forward from: cost-taxonomy-baseline.md — Baseline Summary

| Time period | Monthly cost | Annual cost | Confidence |
|-------------|-------------|------------|------------|
| [TIME WINDOW] | | | H / M / L |

## Cost by bucket

> Carry forward from: cost-taxonomy-baseline.md — Baseline Summary

| Bucket | Monthly | Annual | % of total | Confidence |
|--------|---------|--------|------------|------------|
| Cloud infrastructure | | | | H / M / L |
| Managed service fees | | | | H / M / L |
| Platform tooling | | | | H / M / L |
| Subscriptions | | | | H / M / L |
| Operating effort | | | | H / M / L |
| Shared services | | | | H / M / L |
| **Total** | | | 100% | |

## Fixed versus variable split

> Carry forward from: cost-taxonomy-baseline.md — Baseline Summary

| | Monthly | % of total |
|-|---------|------------|
| Fixed | | |
| Variable | | |

## Cost by platform

> Carry forward from: cost-taxonomy-baseline.md — Total by platform

| Platform | Monthly | Annual | % of total | Confidence |
|----------|---------|--------|------------|------------|
| [PLATFORM A] | | | | H / M / L |
| [PLATFORM B] | | | | H / M / L |
| [PLATFORM C] | | | | H / M / L |
| Shared | | | | |
| **Total** | | | 100% | |

## Key cost drivers

> Summarise the two or three biggest drivers of cost.
> Carry forward from: cost-taxonomy-baseline.md — Key findings

1. [DRIVER 1]
2. [DRIVER 2]
3. [DRIVER 3]

## Tooling duplication

> If duplication was identified in Workshop 2, summarise it here.
> Carry forward from: cost-taxonomy-baseline.md — Tooling duplication

[DUPLICATION SUMMARY AND ESTIMATED COST]

---

---

# Section 4 — Unit Economics

> Target length: 1 to 2 pages.
> Carry all figures forward from unit-metrics-definition.md.

## What unit economics shows us

Total spend is a number. Unit economics is what that number means.
Instead of "we spend X on Kubernetes" this section answers: what does
the platform cost per useful outcome?

## Agreed unit metrics and baseline values

> Carry forward from: unit-metrics-definition.md — Unit economics summary

| Metric | Baseline value | Confidence | What it tells us |
|--------|---------------|------------|-----------------|
| [METRIC 1] | | H / M / L | |
| [METRIC 2] | | H / M / L | |
| [METRIC 3] | | H / M / L | |
| [METRIC 4] | | H / M / L | |
| [METRIC 5] | | H / M / L | |

## The unit economics narrative

> Carry forward from: unit-metrics-definition.md — Unit economics narrative

[NARRATIVE — what do these numbers tell us about the cost efficiency
of the platform estate?]

## Showback summary

> Summarise the showback view from Workshop 3.
> Carry forward from: showback-view.md — Key findings

[SHOWBACK SUMMARY — which teams or namespaces carry the highest cost,
and what does that tell us?]

---

---

# Section 5 — Value and Risk

> Target length: 1 to 2 pages.
> Carry all figures forward from value-risk-scorecard.md.
> This section must sit alongside cost — not after it as an afterthought.

## Why value alongside cost

Cost without value is an incomplete picture. A platform that looks
expensive may be delivering significant returns in delivery speed,
reliability, security posture, and developer productivity. This section
ensures platform decisions are made with a complete view.

## Value and risk scorecard

> Carry forward from: value-risk-scorecard.md — Scorecard Summary

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

## The value narrative

> Carry forward from: value-risk-scorecard.md — The value narrative

**What the platform is enabling well:**
[NARRATIVE]

**Where there is room to improve:**
[NARRATIVE]

**What would be at risk if cost were optimised without considering
this scorecard:**
[NARRATIVE]

---

---

# Section 6 — Scenario Comparison

> Target length: 2 to 3 pages.
> Carry all figures forward from scenario-comparison.md.

## How scenarios were developed

Four scenarios were evaluated against the cost baseline, unit economics,
value scorecard, and workload placement matrix from the previous sections.
The workload placement matrix (see Appendix B) identified consolidation
candidates, justified exceptions, and managed platform candidates —
providing the evidence base for each scenario.

## Scenario summary

> Carry forward from: scenario-comparison.md — Scenario Summary

| | Scenario A | Scenario B | Scenario C | Scenario D |
|-|------------|------------|------------|------------|
| **What changes** | Optimise current estate | Consolidate workloads | Move to managed K8s | Hybrid portfolio |
| **Total cost impact** | | | | |
| **Delivery performance** | | | | |
| **Reliability** | | | | |
| **Security and compliance** | | | | |
| **Developer experience** | | | | |
| **Time to value** | | | | |
| **Risk** | | | | |
| **Key dependency** | | | | |

## Scenario detail

### Scenario A — Optimise the current estate

> Carry forward from: scenario-comparison.md — Scenario A

**Cost impact:** [SUMMARY]
**Value and risk impact:** [SUMMARY]
**Time to value:** 4 to 12 weeks (optimisations) — 1 to 2 quarters (consolidation)
**Risk:** Low
**Key dependency:** [DEPENDENCY]

### Scenario B — Consolidate workloads across platforms

> Carry forward from: scenario-comparison.md — Scenario B

**Cost impact:** [SUMMARY]
**Value and risk impact:** [SUMMARY]
**Time to value:** 1 to 4 quarters
**Risk:** Medium — migration introduces short-term risk
**Key dependency:** [DEPENDENCY]

### Scenario C — Move to managed Kubernetes

> Carry forward from: scenario-comparison.md — Scenario C

**Cost impact:** [SUMMARY]
**Value and risk impact:** [SUMMARY]
**Time to value:** 1 quarter (pilot) — 2 to 4 quarters (broader)
**Risk:** Low to Medium
**Key dependency:** [DEPENDENCY]

### Scenario D — Hybrid portfolio

> Carry forward from: scenario-comparison.md — Scenario D

**Cost impact:** [SUMMARY]
**Value and risk impact:** [SUMMARY]
**Time to value:** 1 quarter (governance) — 2 to 4 quarters (consolidation)
**Risk:** Medium — governance overhead required
**Key dependency:** [DEPENDENCY]

---

---

# Section 7 — Recommendation and 90-Day Plan

> Target length: 2 pages.
> Carry forward from: scenario-comparison.md and 90-day-plan-template.md.

## Recommendation

> Carry forward from: scenario-comparison.md — Recommendation

**Recommended path:**
[RECOMMENDED SCENARIO]

**Why this path:**
[RATIONALE GROUNDED IN THE EVIDENCE]

**Trade-offs we are accepting:**
[TRADE-OFFS]

**What would change this recommendation:**
[KEY ASSUMPTIONS]

## 90-day plan

### Track 1 — No-regrets actions

> Carry forward from: 90-day-plan-template.md — Track 1

| Action | Owner | Target date |
|--------|-------|------------|
| | | |
| | | |
| | | |
| | | |

### Track 2 — Decisions required

> Carry forward from: 90-day-plan-template.md — Track 2

| Decision | Who decides | By when |
|----------|-------------|---------|
| | | |
| | | |
| | | |

### Track 3 — Pilots and spikes

> Carry forward from: 90-day-plan-template.md — Track 3

| Pilot or spike | Scope | Owner | Duration |
|----------------|-------|-------|----------|
| | | | |
| | | | |

## What success looks like at 90 days

> Carry forward from: 90-day-plan-template.md — What success looks like

| Measure | Current baseline | 90-day target |
|---------|----------------|--------------|
| | | |
| | | |
| | | |

---

---

# Appendix A — Assumptions Register Summary

> Include a summary of the key decisions from the full Assumptions Register.
> The full register is at: templates/working-documents/assumptions-register.md

| Decision area | Decision made | Confidence | Version |
|---------------|--------------|------------|---------|
| Platforms in scope | | | |
| Time window | | | |
| Non-production treatment | | | |
| Shared cost allocation | | | |
| Operating effort method | | | |
| Tooling duplication treatment | | | |
| Allocation rules | | | |

---

# Appendix B — Workload Placement Matrix Summary

> Summarise the placement matrix findings.
> Full matrix at: templates/working-documents/workload-placement-matrix.md

| Category | Count | Key workloads |
|----------|-------|--------------|
| Consolidation candidates | | |
| Justified exceptions | | |
| Managed platform candidates | | |
| Spike candidates | | |

---

# Appendix C — Data Sources

> List every data source used in the assessment.
> Full list at: templates/working-documents/data-request-list.md

| Data item | Source | Date received | Confidence |
|-----------|--------|--------------|------------|
| | | | H / M / L |
| | | | H / M / L |
| | | | H / M / L |

---

# Appendix D — Glossary

| Term | Plain English |
|------|---------------|
| FinOps | A way for engineering and finance to manage platform costs together |
| TBM | Technology Business Management — a standard cost classification framework |
| DORA | Four metrics for software delivery performance |
| SPACE | A framework for developer productivity across five dimensions |
| Unit economics | Cost per useful outcome — e.g. cost per app per month |
| Showback | Making costs visible to teams without billing them |
| Allocation rules | The agreed method for distributing shared costs |
| Baseline | The current state — what things cost today before any changes |
| Confidence rating | H = measured, M = estimated, L = rough guess |
| Workload placement matrix | A structured view of which workloads belong on which platform |
| Hard savings | Actual reduction in spend |
| Cost avoidance | Future spend growth that does not happen |
| Capacity release | Using what you already pay for more efficiently |
| Toil reduction | Operational time returned to higher-value work |
| No-regrets actions | Improvements that make sense regardless of which scenario is chosen |
| Spike | A short, time-boxed investigation to validate a key assumption |
| Managed Kubernetes | A Kubernetes offering where the provider manages the control plane |

---

# Appendix E — Sensitivity Notes

> Note anything that would materially change the recommendation
> if the underlying assumptions turned out to be wrong.

| Assumption | If wrong — impact on recommendation | Likelihood |
|------------|-------------------------------------|------------|
| | High / Medium / Low | High / Medium / Low |
| | High / Medium / Low | High / Medium / Low |
| | High / Medium / Low | High / Medium / Low |
