# Workshop 2 — Attendee Materials
## Cost Taxonomy and Baseline Model

**Version:** 1.0
**Session date:** [DATE]
**Facilitator:** [FACILITATOR]

---

## What this document is

This is your reference and working sheet for Workshop 2. Bring it to the
session — either printed or open on your device.

Some sections have space to capture decisions and findings as we work
through them in the room. Nothing needs to be completed in advance.

---

## What we are doing today

Workshop 2 is where we start building the cost model. We are going to:

- Agree a cost taxonomy — a structured way of grouping spend
- Map known spend into the taxonomy
- Identify what is fixed versus variable
- Review data gaps and confirm owners and dates

By the end of this session we will have a baseline model skeleton that
is ready to populate as the remaining data comes in.

---

## The cost taxonomy — six buckets

Every cost in scope sits in one of these six buckets.

| Bucket | What it covers |
|--------|---------------|
| Cloud infrastructure | Compute, storage, and network costs |
| Managed service fees | Cloud provider charges for managed Kubernetes services |
| Platform tooling | Observability, security, CI/CD, backup, and DR |
| Subscriptions | Platform licences and support agreements |
| Operating effort | Platform team time — the largest hidden cost |
| Shared services | IAM, shared network, shared logging |

---

## Section 1 — Mapping Spend

Work through each bucket in the session. Use this section to capture
what is agreed.

### Bucket 1 — Cloud Infrastructure

| Cost item | Platform | Source | Monthly amount | Confidence | Fixed or variable |
|-----------|----------|--------|---------------|------------|-------------------|
| Compute | | | | | |
| Storage | | | | | |
| Network / egress | | | | | |
| Other | | | | | |

Confidence ratings: **H** = measured | **M** = estimated | **L** = rough guess

Notes and findings:

```
Notes:
```

---

### Bucket 2 — Managed Service Fees

| Cost item | Platform | Source | Monthly amount | Confidence | Fixed or variable |
|-----------|----------|--------|---------------|------------|-------------------|
| Managed K8s fees | | | | | |
| Other | | | | | |

Notes and findings:

```
Notes:
```

---

### Bucket 3 — Platform Tooling

| Cost item | Platform(s) | Source | Monthly amount | Confidence | Fixed or variable |
|-----------|-------------|--------|---------------|------------|-------------------|
| Observability | | | | | |
| Security | | | | | |
| CI/CD | | | | | |
| Backup and DR | | | | | |
| Other | | | | | |

Duplication identified (same capability across multiple platforms):

```
Notes:
```

---

### Bucket 4 — Subscriptions

| Cost item | Renewal date | Source | Monthly amount | Confidence | Fixed or variable |
|-----------|-------------|--------|---------------|------------|-------------------|
| [SUBSCRIPTION] | | | | | |
| [SUBSCRIPTION] | | | | | |
| Other | | | | | |

Notes and findings:

```
Notes:
```

---

### Bucket 5 — Operating Effort

Rough time split across activities — use percentages or hours per month.

| Activity | Estimated time split | Notes |
|----------|---------------------|-------|
| Upgrades and patching | | |
| Incident response and on-call | | |
| Onboarding new teams and workloads | | |
| Building and maintaining standards | | |
| Other | | |

Estimated platform team size: [FTE]
Estimated blended cost per FTE per month: [AMOUNT OR RANGE]

Notes:

```
Notes:
```

---

### Bucket 6 — Shared Services

| Cost item | Source | Monthly amount | Confidence | Fixed or variable |
|-----------|--------|---------------|------------|-------------------|
| IAM | | | | |
| Shared network | | | | |
| Shared logging | | | | |
| Other | | | | |

Notes and findings:

```
Notes:
```

---

## Section 2 — Baseline Summary

Complete this together at the end of the mapping exercise.

### Total spend by bucket (first pass)

| Bucket | Monthly amount | Confidence | Notes |
|--------|---------------|------------|-------|
| Cloud infrastructure | | | |
| Managed service fees | | | |
| Platform tooling | | | |
| Subscriptions | | | |
| Operating effort | | | |
| Shared services | | | |
| **Total** | | | |

### Fixed versus variable split

| | Amount | Percentage |
|-|--------|------------|
| Fixed costs | | |
| Variable costs | | |
| **Total** | | |

---

## Section 3 — Data Gaps

For each gap agree an approach, confirm the owner, and set a date.

| Data item | Approach | Owner | Date | Notes |
|-----------|----------|-------|------|-------|
| | Estimate / Wait / Exclude | | | |
| | Estimate / Wait / Exclude | | | |
| | Estimate / Wait / Exclude | | | |
| | Estimate / Wait / Exclude | | | |

---

## Section 4 — Key Findings So Far

Use this space to note anything that stood out during the session —
numbers that surprised the group, patterns worth investigating, or
early signals about where the levers are.

```
Findings:
```

---

## Section 5 — Questions and Notes

```
Notes:
```

---

## After this session

Within 24 hours you will receive a recap email covering:

- Decisions made in the session
- The updated baseline model — saved, versioned, and shared
- Outstanding data items — please action these as soon as possible
- Workshop 3 confirmed — date, time, and what to expect

The model will be updated as new data comes in before Workshop 3.
A revised version will be shared before the next session.

---

## Glossary

| Term | Plain English |
|------|---------------|
| Cost taxonomy | A structured way of grouping technology costs into consistent categories |
| TBM | Technology Business Management — a standard cost classification framework |
| Fixed cost | A cost that does not change with usage in the short term |
| Variable cost | A cost that scales with usage |
| Baseline | The current state — what things cost today before any changes |
| Confidence rating | H = measured, M = estimated, L = rough guess |
| Operating effort | The time a platform team spends running and maintaining the platforms |
| Shared services | Costs that serve multiple platforms or teams without clean attribution |
| Data egress | The cost of moving data out of a cloud provider |
| Managed service fee | A charge for a managed Kubernetes service above and beyond compute cost |
| Tooling duplication | The same capability running separately across multiple platforms |
| Assumptions Register | A versioned log of every scope and cost treatment decision |
