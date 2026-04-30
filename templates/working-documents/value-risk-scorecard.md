# Value and Risk Scorecard

**Organisation:** [ORGANISATION]
**Facilitator:** [FACILITATOR]
**Version:** [VERSION]
**Last updated:** [DATE]

---

## Version history

| Version | Date | What changed |
|---------|------|-------------|
| v1.0 | [DATE] | Scorecard built and baselined — Workshop 4 |

---

## What this document is

This is the value and risk scorecard for the platform economics assessment.
It captures what the platform enables and what it protects — ensuring that
cost decisions in Workshop 5 are made with a complete picture, not a
cost-only view.

> This document is built entirely in Workshop 4. It cannot be meaningfully
> completed before that session because the measures, proxies, and baselines
> must be agreed in the room by the people who own the data.
>
> See: workshop-4-value-scorecard/attendee-materials.md

---

## Why this scorecard exists

Cost without value is an incomplete picture. A platform that looks expensive
may be delivering significant returns in delivery speed, reliability, security
posture, and developer productivity. The scorecard makes those returns visible
so decisions in Workshop 5 are balanced — not just cost-optimised.

The scorecard uses DORA and SPACE as reference frameworks. Both are
industry standards, not vendor constructs.

---

## Confidence rating guide

| Rating | What it means |
|--------|--------------|
| High | Based on actual measured data from a reliable source |
| Medium | Based on an estimate with a reasonable basis |
| Low | Based on a proxy or rough estimate — treat as indicative |

---

## Category 1 — Delivery Performance

> Agreed and baselined in Workshop 4
> Reference framework: DORA

| Measure | Definition | Data source or proxy | Baseline value | Confidence | Target direction | Notes |
|---------|-----------|---------------------|---------------|------------|-----------------|-------|
| Deployment frequency | How often code is successfully deployed to production | | | H / M / L | Increase / Maintain | |
| Lead time for changes | Time from code commit to running in production | | | H / M / L | Decrease / Maintain | |
| Change failure rate | Percentage of deployments that cause a production failure | | | H / M / L | Decrease / Maintain | |

**Proxy used (if applicable):**

| Measure | Proxy agreed | Reason |
|---------|-------------|--------|
| | | |

**Key findings — delivery performance:**

```
Notes:
```

---

## Category 2 — Reliability

> Agreed and baselined in Workshop 4
> Reference framework: DORA

| Measure | Definition | Data source or proxy | Baseline value | Confidence | Target direction | Notes |
|---------|-----------|---------------------|---------------|------------|-----------------|-------|
| Incident volume | Number of production incidents per quarter | | | H / M / L | Decrease / Maintain | |
| Time to restore service (MTTR) | Average time to recover from a production incident | | | H / M / L | Decrease / Maintain | |
| Platform availability | Uptime percentage | | | H / M / L | Increase / Maintain | |

**Proxy used (if applicable):**

| Measure | Proxy agreed | Reason |
|---------|-------------|--------|
| | | |

**Key findings — reliability:**

```
Notes:
```

---

## Category 3 — Security and Compliance Effort

> Agreed and baselined in Workshop 4

| Measure | Definition | Data source or proxy | Baseline value | Confidence | Target direction | Notes |
|---------|-----------|---------------------|---------------|------------|-----------------|-------|
| Time to patch critical vulnerabilities | From disclosure to patched across the estate | | | H / M / L | Decrease / Maintain | |
| Policy coverage | Percentage of workloads governed by automated policy controls | | | H / M / L | Increase / Maintain | |
| Audit evidence effort | Time spent generating evidence per audit cycle (days) | | | H / M / L | Decrease / Maintain | |

**Proxy used (if applicable):**

| Measure | Proxy agreed | Reason |
|---------|-------------|--------|
| | | |

**Key findings — security and compliance:**

```
Notes:
```

---

## Category 4 — Developer Experience

> Agreed and baselined in Workshop 4
> Reference framework: SPACE

| Measure | Definition | Data source or proxy | Baseline value | Confidence | Target direction | Notes |
|---------|-----------|---------------------|---------------|------------|-----------------|-------|
| Onboarding time | Time for a new service or team to reach first deployment | | | H / M / L | Decrease / Maintain | |
| Time to first deployment | From zero to production for a new workload | | | H / M / L | Decrease / Maintain | |
| Ticket and toil volume | Support tickets or manual steps per month | | | H / M / L | Decrease / Maintain | |

**Proxy used (if applicable):**

| Measure | Proxy agreed | Reason |
|---------|-------------|--------|
| | | |

**Key findings — developer experience:**

```
Notes:
```

---

## Scorecard Summary

> Carry forward from the four category sections above

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

## The value narrative

> Complete after all four categories are baselined.
> This narrative goes directly into the decision brief.

**What the platform is enabling well:**

```
Notes:
```

**Where there is room to improve:**

```
Notes:
```

**What would be at risk if cost were optimised without considering
this scorecard:**

```
Notes:
```
