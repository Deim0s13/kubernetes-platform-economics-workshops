# Workshop 1 — Attendee Materials
## Scope, Glossary, and Rules of the Game

**Version:** 1.0  
**Session date:** [DATE]  
**Facilitator:** [FACILITATOR]  

---

## What this document is

This is your reference and working sheet for Workshop 1. Bring it to the
session — either printed or open on your device.

Some sections have space to capture decisions as we agree them in the room.
Nothing needs to be completed in advance.

---

## What we are doing today

Workshop 1 is where the assessment begins in earnest. We are going to agree:

- Which platforms, environments, and cost types are in scope
- How we will treat shared and complex costs
- Which unit metrics we will use to report cost per outcome
- Who owns which data inputs and when we need them by

Everything we agree today goes into the Assumptions Register — a versioned
record that makes the final output defensible with leadership, Finance,
and Procurement.

---

## Section 1 — Scope

### Platforms

*Confirm in the session. Record what is agreed below.*

| Platform | Role | In scope? | Notes |
|----------|------|-----------|-------|
| [PLATFORM A] | Baseline | | |
| [PLATFORM B] | Baseline | | |
| [PLATFORM C] | Baseline | | |
| [PLATFORM D] | Scenario only | | |
| [PLATFORM E] | Scenario only | | |

Anything missing from this list?

```
Notes:
```

### Environments

*Confirm in the session.*

- [ ] Production only
- [ ] Non-production only
- [ ] Both — separated
- [ ] Both — combined
- [ ] Other: _______________

### Time window

*Confirm in the session.*

- [ ] Last full quarter — [QUARTER / DATES]
- [ ] Last three months — [START DATE] to [END DATE]
- [ ] Other: _______________

### Cost types

*Work through this table in the session. Confirm in or out for each item.*

| Cost type | Examples | In scope? | Confidence | Notes |
|-----------|---------|-----------|------------|-------|
| Cloud compute | EC2, VMs, node pools | | | |
| Cloud storage | Block and object storage | | | |
| Cloud network | Load balancers, NAT, egress | | | |
| Managed service fees | EKS fees, AKS fees | | | |
| Platform tooling | Observability, security, CI/CD | | | |
| Subscriptions | Platform licences, support | | | |
| Operating effort | Platform team time | | | |
| Shared services | IAM, shared logging | | | |

Confidence ratings: **H** = High | **M** = Medium | **L** = Low

---

## Section 2 — Cost Treatment Rules

*We will agree each rule in the session. Record the decision and reason below.*

### Rule 1 — Shared platform costs

Options discussed:

- A — Allocate proportionally by usage
- B — Allocate equally across platforms
- C — Hold in a shared unallocated bucket (recommended for v1)

```
Decision:

Reason:
```

### Rule 2 — Non-production environments

Options discussed:

- A — Include in total as a separate line item
- B — Include in total without separating
- C — Exclude from unit economics but include in total

```
Decision:

Reason:
```

### Rule 3 — Operating effort

Options discussed:

- A — Percentage split of team time across activities
- B — Rough hours per activity per month
- C — Exclude and note as a gap

```
Decision:

Reason:

If Option A or B — rough split or estimate agreed:
```

### Rule 4 — Tooling duplication

Options discussed:

- A — Model as a separate line to surface consolidation opportunity
- B — Include in platform tooling without separating

```
Decision:

Reason:
```

---

## Section 3 — Unit Metrics Shortlist

*We will shortlist three to five metrics in the session. Circle or tick
the ones agreed, and note any data dependencies.*

| Unit metric | Selected? | Data needed |
|-------------|-----------|-------------|
| Cost per production app per month | | |
| Cost per tenant or namespace per month | | |
| Cost per environment (prod vs non-prod) | | |
| Effective cost per vCPU-hour used | | |
| Ops cost per cluster per month | | |
| Cost per deployment or release | | |

```
Notes:
```

---

## Section 4 — Data Request and Owners

*We will confirm owners and due dates together in the session.*

| Data needed | Why we need it | Owner | Due date | Confidence |
|-------------|----------------|-------|----------|------------|
| Cluster inventory | Defines scope | | | |
| Cloud billing exports (AWS CUR / Azure) | Source of truth for spend | | | |
| Platform subscription details | Fixed vs variable cost | | | |
| Tooling list and costs | Duplication and consolidation | | | |
| Ops effort estimate | Cost not on invoices | | | |
| Production app list or top 20 | Unit economics foundation | | | |
| Namespace or team mapping | Allocation rules | | | |
| Utilisation data (CPU / memory) | Effective cost per vCPU | | | |

Confidence ratings: **H** = High | **M** = Medium | **L** = Low

---

## Section 5 — Assumptions Register (v1 summary)

*A full Assumptions Register is maintained in the shared workspace.
Use this space to capture key decisions during the session.*

| Decision | What was agreed | Reason | Confidence |
|----------|----------------|--------|------------|
| Platforms in scope | | | |
| Environments | | | |
| Time window | | | |
| Shared cost treatment | | | |
| Non-prod treatment | | | |
| Operating effort | | | |
| Tooling duplication | | | |

---

## Section 6 — Questions and Notes

*Use this space during the session for anything you want to capture.*

```
Notes:
```

---

## After this session

Within 24 hours you will receive a recap email covering:

- Decisions made in the session
- The Assumptions Register v1 — saved, versioned, and shared
- The data request list with your name and due date confirmed
- Workshop 2 confirmed — date, time, and what to expect

**Action for data owners:** please action your data request items
as soon as possible after this session. The sooner the data comes in,
the stronger the baseline will be in Workshop 2.

---

## Glossary

| Term | Plain English |
|------|---------------|
| Scope | What is included in the assessment and what is not |
| Cost allocation | Distributing shared costs across teams or products |
| Showback | Making costs visible to teams without billing them |
| Chargeback | Billing teams directly for their platform usage |
| Unit economics | Cost per useful outcome — e.g. cost per app per month |
| Assumptions Register | A versioned log of every scope and cost treatment decision |
| Confidence rating | High, Medium, or Low — how certain we are about a figure |
| Baseline | The current state — what things cost today before any changes |
| Unit metric | A single agreed measure of cost per outcome |
| FinOps | A way for engineering and finance to manage platform costs together |
| TBM | A standard cost classification structure for technology spend |
| DORA | Four metrics for measuring software delivery performance |
| SPACE | A framework for measuring developer productivity |
| Cost pool | A grouping of similar costs — e.g. cloud compute, people effort |
| Fixed cost | A cost that does not change with usage — e.g. a subscription fee |
| Variable cost | A cost that changes with usage — e.g. compute consumption |
