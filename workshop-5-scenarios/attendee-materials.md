# Workshop 5 — Attendee Materials
## Scenarios, Recommendation, and 90-Day Plan

**Version:** 1.0
**Session date:** [DATE]
**Facilitator:** [FACILITATOR]

---

## What this document is

This is your reference and working sheet for Workshop 5. Bring it to the
session — either printed or open on your device. This is the most
substantive attendee document in the series — it covers the workload
placement matrix, scenario comparison, recommendation, and 90-day plan.

---

## What we are doing today

Workshop 5 is the final session. Everything we have built across four
workshops comes together here and becomes a decision and a plan.

By the end of this session we will have:

- A workload placement matrix — which workloads belong where and why
- A scenario comparison — four options evaluated on cost, value, risk,
and time to value
- A recommendation — evidence-based, with trade-offs clearly stated
- A 90-day plan — no-regrets actions, decisions required, and pilots
- A decision brief outline ready to populate for the exec audience

---

## The full picture — a reminder

Before we build scenarios, confirm these outputs from previous workshops:

| Output | Headline finding | Confidence |
|--------|----------------|------------|
| Total platform cost | | |
| Key unit metric | | |
| Highest cost driver | | |
| Biggest value finding | | |
| Biggest risk signal | | |

---

## Section 1 — Workload Placement Matrix

Score ten to twenty meaningful workloads against six criteria.

**Scoring:** H = High | M = Medium | L = Low

| Workload | Compliance intensity | Cloud coupling | Ops burden | Portability need | Migration complexity | Data gravity |
|----------|---------------------|---------------|------------|-----------------|---------------------|-------------|
| [WL 1] | | | | | | |
| [WL 2] | | | | | | |
| [WL 3] | | | | | | |
| [WL 4] | | | | | | |
| [WL 5] | | | | | | |
| [WL 6] | | | | | | |
| [WL 7] | | | | | | |
| [WL 8] | | | | | | |
| [WL 9] | | | | | | |
| [WL 10] | | | | | | |
| [WL 11] | | | | | | |
| [WL 12] | | | | | | |

**Criteria quick reference:**

| Criterion | High means... | Low means... |
|-----------|--------------|-------------|
| Compliance intensity | Heavy policy, frequent audits | Light touch, minimal evidence needed |
| Cloud coupling | Deeply integrated with provider services | Portable, minimal provider dependencies |
| Ops burden | High toil, complex day-two operations | Low maintenance, runs itself well |
| Portability need | Needs to move or might move | Stable, no foreseeable need to move |
| Migration complexity | Risky, complex, many dependencies | Straightforward, low risk |
| Data gravity | Hard latency or residency constraints | No meaningful location constraints |

**Placement outcomes:**

Consolidation candidates (low coupling + high burden or high compliance + low complexity):

```
Workloads:
```

Justified exceptions (high coupling or high complexity or hard constraints):

```
Workloads and reasons:
```

Managed platform candidates (high burden + low coupling):

```
Workloads:
```

Spike candidates (ambiguous — needs further investigation):

```
Workloads:
```

---

## Section 2 — Scenario Comparison

Complete together during the session.

### How we assess cost impact

| Type | What it means |
|------|--------------|
| Hard savings | Actual reduction in spend |
| Cost avoidance | Future growth that does not happen |
| Capacity release | Using what you already pay for more efficiently |
| Toil reduction | Operational time returned to higher-value work |

---

### Scenario A — Optimise the current estate

What changes: Utilisation improvement, cluster sprawl reduction, resource
rightsizing, autoscaling, tooling consolidation. No structural change.

| Dimension | Assessment | Notes |
|-----------|-----------|-------|
| Hard savings | | |
| Cost avoidance | | |
| Capacity release | | |
| Toil reduction | | |
| Delivery performance impact | | |
| Reliability impact | | |
| Security and compliance impact | | |
| Developer experience impact | | |
| Time to value | 4-12 weeks (optimisations) | |
| Risk | Low | |
| Key dependencies | Governance + tooling | |

---

### Scenario B — Consolidate workloads across platforms

What changes: Consolidation candidates migrate to a preferred platform.
Tooling, policy, and operational duplication is reduced.

| Dimension | Assessment | Notes |
|-----------|-----------|-------|
| Hard savings | | |
| Cost avoidance | | |
| Capacity release | | |
| Toil reduction | | |
| Delivery performance impact | | |
| Reliability impact | | |
| Security and compliance impact | | |
| Developer experience impact | | |
| Time to value | 1-4 quarters | |
| Risk | Medium | |
| Key dependencies | Placement rules + migration plan | |

---

### Scenario C — Move to managed Kubernetes

What changes: Selected clusters move to managed Kubernetes. Control
plane and upgrade burden shifts to the managed service.

| Dimension | Assessment | Notes |
|-----------|-----------|-------|
| Hard savings | | |
| Cost avoidance | | |
| Capacity release | | |
| Toil reduction | | |
| Delivery performance impact | | |
| Reliability impact | | |
| Security and compliance impact | | |
| Developer experience impact | | |
| Time to value | 1 quarter (pilot) / 2-4 quarters (broader) | |
| Risk | Low to Medium | |
| Key dependencies | Landing zone readiness | |

---

### Scenario D — Hybrid portfolio

What changes: The estate is structured deliberately. Justified exceptions
stay. Consolidation candidates migrate.

| Dimension | Assessment | Notes |
|-----------|-----------|-------|
| Hard savings | | |
| Cost avoidance | | |
| Capacity release | | |
| Toil reduction | | |
| Delivery performance impact | | |
| Reliability impact | | |
| Security and compliance impact | | |
| Developer experience impact | | |
| Time to value | 1 quarter (governance) / 2-4 quarters (consolidation) | |
| Risk | Medium | |
| Key dependencies | Placement rules + governance model | |

---

### Scenario summary

| | Scenario A | Scenario B | Scenario C | Scenario D |
|-|------------|------------|------------|------------|
| Cost impact | | | | |
| Value and risk | | | | |
| Time to value | | | | |
| Risk | | | | |
| Key dependency | | | | |

---

## Section 3 — Recommendation

Complete together in the session.

**Recommended path:**

```
Notes:
```

**Why this path — evidence from the model:**

```
Notes:
```

**Trade-offs we are accepting:**

```
Notes:
```

**What would change this recommendation:**

```
Notes:
```

**Dissenting views (if any):**

```
Notes:
```

---

## Section 4 — 90-Day Plan

### Track 1 — No-regrets actions

Start these now — they make sense regardless of which scenario is chosen.

| Action | Owner | Timeframe | Expected outcome |
|--------|-------|-----------|-----------------|
| | | | |
| | | | |
| | | | |
| | | | |
| | | | |

### Track 2 — Decisions required

Leadership needs to make these decisions before the preferred scenario
can be fully committed to.

| Decision | Who decides | By when | Options |
|----------|-------------|---------|---------|
| | | | |
| | | | |
| | | | |

### Track 3 — Pilots and spikes

Time-boxed investigations to validate key assumptions before committing
to structural change.

| Pilot or spike | Scope | Success criteria | Timeframe | Owner |
|----------------|-------|-----------------|-----------|-------|
| | | | | |
| | | | | |
| | | | | |

---

## Section 5 — Decision Brief Outline

Confirm the structure and timeline before the session closes.

| Section | Content | Status |
|---------|---------|--------|
| Executive summary | What we assessed, findings, recommendation | To produce |
| Methodology | Frameworks, confidence levels, assumptions | To produce |
| Cost baseline | TBM-aligned baseline, fixed vs variable | From Workshop 2 |
| Unit economics | Three to five metrics with baselines | From Workshop 3 |
| Value scorecard | Eight to twelve measures with targets | From Workshop 4 |
| Scenario comparison | Four scenarios on four dimensions | From Workshop 5 |
| Recommendation | Recommended path, rationale, trade-offs | From Workshop 5 |
| 90-day plan | Actions, decisions, pilots | From Workshop 5 |
| Appendix | Assumptions register, sources, glossary | Ongoing |

**Decision brief audience:** [CIO] | [GM TECH AND OPS] | [FINANCE] | [PROCUREMENT]

**Draft by:** [DATE]

**Review session:** [DATE]

**Leadership presentation:** [DATE / TBC]

---

## Section 6 — Questions and Notes

```
Notes:
```

---

## After this session

Within 48 hours you will receive:

- A recap email — recommendation confirmed, 90-day plan summary,
decision brief timeline
- All session outputs saved and shared — scenario comparison,
placement matrix, 90-day plan
- The Assumptions Register — final version, fully versioned

The decision brief draft will follow by [DATE]. You will have the
opportunity to review it before it goes to the leadership audience.

**No-regrets actions start now.** Do not wait for the brief to be
finalised before beginning the work identified in Track 1.

---

## Glossary

| Term | Plain English |
|------|---------------|
| Scenario | A structured option for how the platform estate could be organised |
| Workload placement matrix | A structured view of which workloads belong on which platform and why |
| Hard savings | Actual reduction in spend |
| Cost avoidance | Future spend growth that does not happen |
| Capacity release | Using what you already pay for more efficiently |
| Toil reduction | Operational time returned to higher-value work |
| No-regrets actions | Improvements that make sense regardless of which scenario is chosen |
| Spike | A short, time-boxed investigation to validate a key assumption |
| Pilot | A small-scale implementation to test a scenario before committing |
| Decision brief | The exec-ready output for leadership, Finance, and Procurement |
| Cloud-native coupling | Tight dependency on services specific to one cloud provider |
| Data gravity | Performance or data residency constraints that pin workloads to a location |
| Managed Kubernetes | A Kubernetes offering where the provider manages the control plane |
| Justified exception | A workload with documented, quantified reasons to stay on its current platform |
| Governance model | The rules and processes that keep a hybrid estate from becoming unmanaged sprawl |
