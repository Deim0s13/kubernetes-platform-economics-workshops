# Workload Placement Matrix

**Organisation:** [ORGANISATION]
**Facilitator:** [FACILITATOR]
**Version:** [VERSION]
**Last updated:** [DATE]

---

## Version history

| Version | Date | What changed |
|---------|------|-------------|
| v1.0 | [DATE] | Matrix built and agreed — Workshop 5 |

---

## What this document is

This is the workload placement matrix for the platform economics assessment.
It provides a structured view of which workloads belong on which platform
and why — based on agreed criteria rather than habit or history.

> This document is built in Workshop 5. It cannot be completed without the
> cost baseline, unit economics, and value scorecard from previous workshops
> — because the placement decision requires understanding both the cost and
> the operational characteristics of each workload.
>
> See: workshop-5-scenarios/attendee-materials.md — Section 1

---

## Why this matrix matters

Without a placement matrix, the scenario comparison in Workshop 5 becomes
a platform debate. With it, the conversation is grounded in workload
characteristics rather than preference. That is what makes the final
recommendation credible with Finance and Procurement.

The matrix is also what distinguishes a justified exception from an
unjustified one. Any workload that stays on its current platform after
this assessment should have a documented reason in this matrix.

---

## Scoring criteria

Score each workload against six criteria using High, Medium, or Low.

| Criterion | High means | Low means |
|-----------|-----------|----------|
| Compliance intensity | Heavy policy enforcement, frequent audits, significant evidence generation | Light touch, minimal compliance obligations |
| Cloud-native coupling | Deeply integrated with provider-specific managed services | Portable, minimal provider dependencies |
| Operational burden | High day-two toil, complex operations, frequent intervention | Low maintenance, largely self-managing |
| Portability need | Needs or may need to move between platforms or clouds | Stable, no foreseeable need to move |
| Migration complexity | Risky, many dependencies, long migration timeline | Straightforward, low risk, short timeline |
| Data gravity | Hard latency or data residency constraints pinning the workload | No meaningful location constraints |

---

## The matrix

> Score each workload during Workshop 5. Two to three minutes per workload.
> The pattern across workloads matters more than precision on any single one.

**Scoring:** H = High | M = Medium | L = Low

| Workload | Compliance intensity | Cloud coupling | Ops burden | Portability need | Migration complexity | Data gravity | Provisional placement |
|----------|---------------------|---------------|------------|-----------------|---------------------|-------------|----------------------|
| [WL 01] | | | | | | | |
| [WL 02] | | | | | | | |
| [WL 03] | | | | | | | |
| [WL 04] | | | | | | | |
| [WL 05] | | | | | | | |
| [WL 06] | | | | | | | |
| [WL 07] | | | | | | | |
| [WL 08] | | | | | | | |
| [WL 09] | | | | | | | |
| [WL 10] | | | | | | | |
| [WL 11] | | | | | | | |
| [WL 12] | | | | | | | |
| [WL 13] | | | | | | | |
| [WL 14] | | | | | | | |
| [WL 15] | | | | | | | |
| [WL 16] | | | | | | | |
| [WL 17] | | | | | | | |
| [WL 18] | | | | | | | |
| [WL 19] | | | | | | | |
| [WL 20] | | | | | | | |

---

## Placement outcomes

> Populate after scoring all workloads in the matrix above

### Consolidation candidates

Low cloud coupling + high operational burden or high compliance intensity
+ low migration complexity

| Workload | Primary reason | Preferred destination | Notes |
|----------|---------------|----------------------|-------|
| | | | |
| | | | |

---

### Justified exceptions — with documented reasons

> Every workload in this section must have a clear, documented reason.
> "We have always run it here" is not a justified exception.

| Workload | Stays on | Documented reason | Review date |
|----------|----------|-------------------|-------------|
| | | | |
| | | | |

---

### Managed platform candidates

High operational burden + low cloud coupling — good candidates for
a managed Kubernetes offering

| Workload | Primary reason | Notes |
|----------|---------------|-------|
| | | |
| | | |

---

### Spike candidates

Ambiguous scoring — needs further investigation before a placement
decision can be made

| Workload | What is ambiguous | Recommended spike | Owner |
|----------|-------------------|------------------|-------|
| | | | |
| | | | |

---

## Placement summary

| Category | Count | % of workloads assessed |
|----------|-------|------------------------|
| Consolidation candidates | | |
| Justified exceptions | | |
| Managed platform candidates | | |
| Spike candidates | | |
| **Total assessed** | | 100% |

---

## Key findings from the matrix

**Most common reason for consolidation candidacy:**

```
Notes:
```

**Most common reason for justified exception:**

```
Notes:
```

**Implications for scenario modelling:**

```
How does the placement matrix shape the scenario comparison?
Which scenarios become more or less viable based on these results?
```
