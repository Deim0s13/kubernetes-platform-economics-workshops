# Scenario Comparison

**Organisation:** [ORGANISATION]
**Facilitator:** [FACILITATOR]
**Version:** [VERSION]
**Last updated:** [DATE]

---

## Version history

| Version | Date | What changed |
|---------|------|-------------|
| v1.0 | [DATE] | Scenarios evaluated and compared — Workshop 5 |

---

## What this document is

This is the scenario comparison for the platform economics assessment.
It evaluates four scenarios across cost, value and risk, time to value,
and dependencies — and forms the evidence base for the recommendation
in the decision brief.

> This document is built in Workshop 5. It requires all working documents
> from Workshops 1 through 4 to be complete before the scenario evaluation
> can be done with confidence.
>
> See: workshop-5-scenarios/attendee-materials.md — Section 2
> See: templates/working-documents/workload-placement-matrix.md
> See: templates/working-documents/cost-taxonomy-baseline.md
> See: templates/working-documents/unit-metrics-definition.md
> See: templates/working-documents/value-risk-scorecard.md

---

## Cost impact types

We distinguish between four types of cost impact throughout this document.

| Type | What it means |
|------|--------------|
| Hard savings | Actual reduction in spend — money that leaves the budget |
| Cost avoidance | Future spend growth that does not happen |
| Capacity release | Using what you already pay for more efficiently |
| Toil reduction | Operational time returned to higher-value work |

---

## Scenario A — Optimise the Current Estate

**What changes:** The current platform estate stays broadly as-is. Focus
on utilisation improvement, cluster sprawl reduction, resource rightsizing,
autoscaling, and tooling consolidation where duplication exists. No
structural change to the platform model.

### Cost impact

| Type | Estimated value | Basis | Confidence |
|------|----------------|-------|------------|
| Hard savings | | | H / M / L |
| Cost avoidance | | | H / M / L |
| Capacity release | | [From unit-metrics-definition.md — utilisation gap] | H / M / L |
| Toil reduction | | | H / M / L |
| **Total estimated impact** | | | |

### Value and risk impact

> Score against the value scorecard — does this scenario improve or worsen each category?
> Carry forward categories from value-risk-scorecard.md

| Scorecard category | Impact | Notes |
|-------------------|--------|-------|
| Delivery performance | Improves / Neutral / Worsens | |
| Reliability | Improves / Neutral / Worsens | |
| Security and compliance effort | Improves / Neutral / Worsens | |
| Developer experience | Improves / Neutral / Worsens | |

### Time to value

| Action type | Timeframe |
|-------------|-----------|
| No-regrets optimisations | 4 to 12 weeks |
| Cluster consolidation | 1 to 2 quarters |

### Risk

| Field | Assessment |
|-------|-----------|
| Overall risk rating | Low |
| Primary risks | |
| Mitigations | |

### Key dependencies

```
Notes:
```

---

## Scenario B — Consolidate Workloads Across Platforms

**What changes:** Workloads identified as consolidation candidates in the
placement matrix migrate to a preferred platform. Tooling, policy, and
operational duplication is reduced. The estate becomes more intentional.

### Cost impact

| Type | Estimated value | Basis | Confidence |
|------|----------------|-------|------------|
| Hard savings | | [From cost-taxonomy-baseline.md — tooling duplication] | H / M / L |
| Cost avoidance | | | H / M / L |
| Capacity release | | | H / M / L |
| Toil reduction | | [From cost-taxonomy-baseline.md — ops effort] | H / M / L |
| **Total estimated impact** | | | |

### Value and risk impact

| Scorecard category | Impact | Notes |
|-------------------|--------|-------|
| Delivery performance | Improves / Neutral / Worsens | |
| Reliability | Improves / Neutral / Worsens | |
| Security and compliance effort | Improves / Neutral / Worsens | |
| Developer experience | Improves / Neutral / Worsens | |

### Time to value

| Action type | Timeframe |
|-------------|-----------|
| Tooling consolidation | 1 to 2 quarters |
| Workload migration | 2 to 4 quarters |

### Risk

| Field | Assessment |
|-------|-----------|
| Overall risk rating | Medium |
| Primary risks | Migration introduces short-term delivery and reliability risk |
| Mitigations | Sequence consolidation candidates first. Spike candidates require investigation before migration. |

### Key dependencies

```
Notes:
```

---

## Scenario C — Move to Managed Kubernetes

**What changes:** Selected clusters or workloads move to a managed
Kubernetes offering. Control plane management, upgrades, and infrastructure
reliability shift to the managed service. Platform team capacity is
redirected to higher-value work.

### Cost impact

| Type | Estimated value | Basis | Confidence |
|------|----------------|-------|------------|
| Hard savings | | | H / M / L |
| Cost avoidance | | | H / M / L |
| Capacity release | | | H / M / L |
| Toil reduction | | [From cost-taxonomy-baseline.md — upgrade and patching effort] | H / M / L |
| **Total estimated impact** | | | |

**Infrastructure cost comparison:**

| | Self-managed (current) | Managed (estimated) | Difference |
|-|----------------------|--------------------|-|
| Monthly infrastructure cost | | | |
| Monthly operating effort cost | | | |
| **Total monthly cost** | | | |

### Value and risk impact

| Scorecard category | Impact | Notes |
|-------------------|--------|-------|
| Delivery performance | Improves / Neutral / Worsens | |
| Reliability | Improves / Neutral / Worsens | |
| Security and compliance effort | Improves / Neutral / Worsens | |
| Developer experience | Improves / Neutral / Worsens | |

### Time to value

| Action type | Timeframe |
|-------------|-----------|
| Landing zone and pilot | 1 quarter |
| Broader migration | 2 to 4 quarters |

### Risk

| Field | Assessment |
|-------|-----------|
| Overall risk rating | Low to Medium |
| Primary risks | Migration period. Non-standard workload requirements. |
| Mitigations | Pilot with consolidation candidates first. Validate landing zone requirements before committing. |

### Key dependencies

```
Notes:
```

---

## Scenario D — Hybrid Portfolio

**What changes:** The estate is structured deliberately. Justified exceptions
stay where they are with documented reasons from the placement matrix.
Consolidation candidates migrate. The estate is intentional — not sprawling.

### Cost impact

| Type | Estimated value | Basis | Confidence |
|------|----------------|-------|------------|
| Hard savings | | | H / M / L |
| Cost avoidance | | | H / M / L |
| Capacity release | | | H / M / L |
| Toil reduction | | | H / M / L |
| **Total estimated impact** | | | |

### Value and risk impact

| Scorecard category | Impact | Notes |
|-------------------|--------|-------|
| Delivery performance | Improves / Neutral / Worsens | |
| Reliability | Improves / Neutral / Worsens | |
| Security and compliance effort | Improves / Neutral / Worsens | |
| Developer experience | Improves / Neutral / Worsens | |

### Time to value

| Action type | Timeframe |
|-------------|-----------|
| Governance model | 1 quarter |
| Consolidation of non-exceptions | 2 to 4 quarters |

### Risk

| Field | Assessment |
|-------|-----------|
| Overall risk rating | Medium |
| Primary risks | Governance overhead. Risk of hybrid model expanding without discipline. |
| Mitigations | Strong placement rules. Regular review of justified exceptions. Document all exceptions with a review date. |

### Key dependencies

```
Notes:
```

---

## Scenario Summary

> Complete after all four scenarios are evaluated

| | Scenario A | Scenario B | Scenario C | Scenario D |
|-|------------|------------|------------|------------|
| **Total cost impact** | | | | |
| **Delivery performance** | | | | |
| **Reliability** | | | | |
| **Security and compliance** | | | | |
| **Developer experience** | | | | |
| **Time to value** | 4-12 weeks | 1-4 quarters | 1-4 quarters | 1-4 quarters |
| **Risk** | Low | Medium | Low-Medium | Medium |
| **Key dependency** | | | | |

---

## Recommendation

> Agreed in Workshop 5 — carry forward to decision-brief-template.md

**Recommended path:**

```
Notes:
```

**Why this path — grounded in the evidence:**

```
Notes:
```

**Trade-offs we are accepting:**

```
Notes:
```

**Key assumptions the recommendation depends on:**

```
Notes:
```

**Dissenting views (if any):**

```
Notes:
```
