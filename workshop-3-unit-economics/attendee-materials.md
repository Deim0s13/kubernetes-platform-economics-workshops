# Workshop 3 — Attendee Materials
## Allocation Rules and Unit Economics

**Version:** 1.0
**Session date:** [DATE]
**Facilitator:** [FACILITATOR]

---

## What this document is

This is your reference and working sheet for Workshop 3. Bring it to the
session — either printed or open on your device.

Some sections have space to capture decisions and values as we work through
them in the room. Nothing needs to be completed in advance.

---

## What we are doing today

Workshop 3 is where the cost model becomes useful to leadership. We are
moving from total cost to unit economics — cost per useful outcome.

By the end of this session we will have:

- Agreed allocation rules for shared costs
- Baseline values for our three to five unit metrics
- A first-pass showback view mapping cost to teams or namespaces
- A clear narrative connecting platform cost to business outcomes

---

## A reminder of why this matters

Total spend is a number. Unit economics is what that number means.

Instead of "we spend X on Kubernetes" we want to be able to say:

- "A production application costs Y per month."
- "Each tenant costs Z per quarter."
- "We pay for capacity but only use A% of it effectively."

Those are the numbers leadership and Finance can act on.

---

## Section 1 — Allocation Rules

We will agree these together in the session. Record what is decided below.

### Shared platform costs

| Option | Description | Selected? |
|--------|-------------|-----------|
| A | Proportional by usage | |
| B | Equal split across platforms | |
| C | Shared unallocated bucket | |

```
Decision:

Reason:
```

### Platform tooling allocation

| Option | Description | Selected? |
|--------|-------------|-----------|
| A | Allocate by cluster or node count per platform | |
| B | Allocate equally across platforms | |
| C | Hold as shared — do not allocate | |

```
Decision:

Reason:
```

### Operating effort allocation

| Option | Description | Selected? |
|--------|-------------|-----------|
| A | Allocate by estimated time per platform | |
| B | Allocate equally across platforms | |
| C | Hold as platform-level cost — do not allocate to workloads | |

```
Decision:

Reason:
```

### Minimum tagging standard

Current tags and labels in use:

| Tag / label | What it identifies | Coverage |
|-------------|-------------------|----------|
| | | |
| | | |
| | | |

Minimum standard agreed for this work:

```
Notes:
```

Gaps to close:

```
Notes:
```

---

## Section 2 — Unit Metrics

Our shortlist from Workshop 1:

- [ ] Cost per production app per month
- [ ] Cost per tenant or namespace per month
- [ ] Cost per environment (prod vs non-prod)
- [ ] Effective cost per vCPU-hour used
- [ ] Ops cost per cluster per month
- [ ] Other: _______________

---

### Metric 1: [METRIC NAME]

| Field | Value |
|-------|-------|
| Numerator (costs included) | |
| Denominator (what we divide by) | |
| Data sources | |
| Baseline value | |
| Confidence rating | H / M / L |

```
What this number means:

What it enables:

Notes:
```

---

### Metric 2: [METRIC NAME]

| Field | Value |
|-------|-------|
| Numerator (costs included) | |
| Denominator (what we divide by) | |
| Data sources | |
| Baseline value | |
| Confidence rating | H / M / L |

```
What this number means:

What it enables:

Notes:
```

---

### Metric 3: [METRIC NAME]

| Field | Value |
|-------|-------|
| Numerator (costs included) | |
| Denominator (what we divide by) | |
| Data sources | |
| Baseline value | |
| Confidence rating | H / M / L |

```
What this number means:

What it enables:

Notes:
```

---

### Metric 4: [METRIC NAME]

| Field | Value |
|-------|-------|
| Numerator (costs included) | |
| Denominator (what we divide by) | |
| Data sources | |
| Baseline value | |
| Confidence rating | H / M / L |

```
What this number means:

What it enables:

Notes:
```

---

### Metric 5: [METRIC NAME]

| Field | Value |
|-------|-------|
| Numerator (costs included) | |
| Denominator (what we divide by) | |
| Data sources | |
| Baseline value | |
| Confidence rating | H / M / L |

```
What this number means:

What it enables:

Notes:
```

---

## Section 3 — Unit Economics Summary

Complete this together at the end of the metric-building exercise.

| Metric | Baseline value | Confidence | Key finding |
|--------|---------------|------------|-------------|
| [METRIC 1] | | H / M / L | |
| [METRIC 2] | | H / M / L | |
| [METRIC 3] | | H / M / L | |
| [METRIC 4] | | H / M / L | |
| [METRIC 5] | | H / M / L | |

---

## Section 4 — Showback View

First-pass cost mapped to teams, products, or namespaces.

| Team / namespace | Compute | Tooling | Ops effort | Total | % of total |
|-----------------|---------|---------|------------|-------|------------|
| | | | | | |
| | | | | | |
| | | | | | |
| | | | | | |
| Shared / unallocated | | | | | |
| **Total** | | | | | |

```
Key findings from the showback view:
```

---

## Section 5 — Key Findings

Use this space to capture findings that emerged during the session —
numbers that surprised the group, patterns worth investigating, or
early signals about where the levers are.

```
Findings:
```

---

## Section 6 — Questions and Notes

```
Notes:
```

---

## After this session

Within 24 hours you will receive a recap email covering:

- Decisions made in the session
- The unit economics model — saved, versioned, and shared
- The showback view — saved, versioned, and shared
- Workshop 4 confirmed — date, time, and what to expect

Workshop 4 looks at the other side of the equation — not just what
the platform costs, but what it enables. We will build a value and
risk scorecard so cost is not the only lens leadership is looking
through.

---

## Glossary

| Term | Plain English |
|------|---------------|
| Unit economics | Cost per useful outcome — e.g. cost per app per month |
| Allocation rules | The agreed method for distributing shared costs |
| Showback | Making costs visible to teams without billing them |
| Chargeback | Billing teams directly for their platform usage |
| Numerator | The cost included in a unit metric calculation |
| Denominator | What you divide by — app count, tenant count, vCPU hours |
| Utilisation gap | The difference between capacity purchased and capacity used |
| Namespace | A Kubernetes construct for grouping and isolating workloads |
| Tenant | A team or product that uses a shared platform |
| Confidence rating | H = measured, M = estimated, L = rough guess |
| Assumptions Register | A versioned log of every scope and cost treatment decision |
| Tagging / labelling | Metadata applied to cloud resources to enable cost allocation |
| vCPU-hour | One virtual CPU running for one hour — the unit of compute measurement |
