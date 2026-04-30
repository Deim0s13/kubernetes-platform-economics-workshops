# Data Request List

**Organisation:** [ORGANISATION]
**Facilitator:** [FACILITATOR]
**Version:** [VERSION]
**Last updated:** [DATE]

---

## Version history

| Version | Date | What changed |
|---------|------|-------------|
| v1.0 | [DATE] | Initial list agreed — Workshop 1 |

---

## What this document is

This is the master list of data needed to complete the platform economics
assessment. Every item has a named owner, a due date, and a record of
whether it has been received.

> This list is created and agreed in Workshop 1 and updated in Workshop 2
> as gaps are identified. It is not complete until all items are either
> received or formally closed with an agreed alternative.
>
> See: workshop-1-scope/attendee-materials.md
> See: workshop-2-cost-baseline/attendee-materials.md

---

## How to use this list

For each item:

- **Owner** — the person responsible for providing the data. This does
not have to be the person who owns the data — it just needs to be
someone who can get it.
- **Due date** — a realistic date, not an ideal date.
- **Status** — Not started / In progress / Received / Closed (with note)
- **Confidence** — once received, rate the data: H = measured,
M = estimated, L = rough guess

If an item cannot be provided, agree one of three approaches in Workshop 2:
Estimate with a Low confidence rating, exclude with a note on the impact,
or defer to a later date with a firm commitment.

---

## Core data items

### Cloud billing

| Data item | Why we need it | Owner | Due date | Status | Confidence | Notes |
|-----------|---------------|-------|----------|--------|------------|-------|
| AWS Cost and Usage Report (CUR) | Source of truth for AWS spend by service, account, and tag | | | | H / M / L | |
| Azure cost export | Source of truth for Azure spend by service, subscription, and tag | | | | H / M / L | |
| Time period covered | Must match agreed time window | | | | | |

---

### Platform inventory

| Data item | Why we need it | Owner | Due date | Status | Confidence | Notes |
|-----------|---------------|-------|----------|--------|------------|-------|
| Cluster inventory | Defines scope — prevents gaps | | | | H / M / L | |
| Node counts per cluster | Grounds compute cost calculation | | | | H / M / L | |
| Instance types or VM sizes | Enables cost per node analysis | | | | H / M / L | |
| Cluster purpose | Prod, non-prod, dev, test, staging | | | | H / M / L | |
| Cluster version and upgrade history | Context for ops effort estimate | | | | H / M / L | |

---

### Subscriptions and licences

| Data item | Why we need it | Owner | Due date | Status | Confidence | Notes |
|-----------|---------------|-------|----------|--------|------------|-------|
| Platform subscription details | Separates fixed from variable cost | | | | H / M / L | |
| Renewal date and current terms | Relevant to scenario timing | | | | H / M / L | |
| Support agreement details | Part of subscription cost bucket | | | | H / M / L | |

---

### Platform tooling

| Data item | Why we need it | Owner | Due date | Status | Confidence | Notes |
|-----------|---------------|-------|----------|--------|------------|-------|
| Tooling list — observability | Identifies duplication across platforms | | | | H / M / L | |
| Tooling list — security | Identifies duplication across platforms | | | | H / M / L | |
| Tooling list — CI/CD | Identifies duplication across platforms | | | | H / M / L | |
| Tooling list — backup and DR | Identifies duplication across platforms | | | | H / M / L | |
| Tooling costs — invoices or estimates | Part of platform tooling cost bucket | | | | H / M / L | |

---

### Operating effort

| Data item | Why we need it | Owner | Due date | Status | Confidence | Notes |
|-----------|---------------|-------|----------|--------|------------|-------|
| Platform team size (FTE) | Basis for operating effort cost | | | | H / M / L | |
| Rough time split across activities | Captures cost not on invoices | | | | H / M / L | |
| On-call model and incident volume | Reliability and effort signal | | | | H / M / L | |
| Upgrade and patching cadence | Operating effort and risk signal | | | | H / M / L | |

---

### Workloads and allocation

| Data item | Why we need it | Owner | Due date | Status | Confidence | Notes |
|-----------|---------------|-------|----------|--------|------------|-------|
| Production application list or top 20 | Grounds unit economics in reality | | | | H / M / L | |
| Namespace or team mapping | Foundation for allocation rules | | | | H / M / L | |
| Utilisation data — CPU and memory | Effective cost per vCPU calculation | | | | H / M / L | |
| Existing showback or chargeback reports | Baseline for allocation rules | | | | H / M / L | |

---

## Items still outstanding

> Review this section at the start of Workshop 2 and again before Workshop 3.
> Every outstanding item needs a decision — estimate, exclude, or defer.

| Data item | Owner | Original due date | New due date or decision | Impact if not resolved |
|-----------|-------|------------------|------------------------|----------------------|
| | | | | High / Medium / Low |
| | | | | High / Medium / Low |
| | | | | High / Medium / Low |

---

## Closed items — with notes

> Record items that were formally closed without being received, along
> with the agreed mitigation. This is part of the audit trail.

| Data item | Closed date | Approach agreed | Impact on confidence |
|-----------|------------|----------------|---------------------|
| | | Estimate / Exclude / Defer | |
