# Cost Taxonomy and Baseline Model

**Organisation:** [ORGANISATION]
**Facilitator:** [FACILITATOR]
**Version:** [VERSION]
**Last updated:** [DATE]
**Time window:** [START DATE] to [END DATE]

---

## Version history

| Version | Date | What changed |
|---------|------|-------------|
| v1.0 | [DATE] | Taxonomy agreed and skeleton created — Workshop 2 |

---

## What this document is

This is the cost taxonomy and baseline model for the platform economics
assessment. It organises all in-scope platform costs into six agreed
buckets and provides a structured view of where spend goes across the
Kubernetes estate.

> This document is created and populated in Workshop 2. The taxonomy
> structure is agreed in the session. Costs are mapped into it using
> data from the Data Request List.
>
> It cannot be completed without the scope and cost treatment rules
> agreed in Workshop 1 and the data gathered before Workshop 2.
>
> See: workshop-2-cost-baseline/attendee-materials.md
> See: templates/working-documents/assumptions-register.md — Section 2
> See: templates/working-documents/data-request-list.md

---

## Taxonomy structure — the six buckets

All in-scope costs sit in one of these six buckets. If a cost does not
fit, it goes into an Other bucket and is noted in the Assumptions Register.

| Bucket | What it covers |
|--------|---------------|
| 1. Cloud infrastructure | Compute, storage, and network costs |
| 2. Managed service fees | Cloud provider charges for managed Kubernetes services |
| 3. Platform tooling | Observability, security, CI/CD, backup, and DR |
| 4. Subscriptions | Platform licences and support agreements |
| 5. Operating effort | Platform team time |
| 6. Shared services | IAM, shared network, shared logging |

---

## Bucket 1 — Cloud Infrastructure

> Populated in Workshop 2 using cloud billing exports
> See: templates/working-documents/data-request-list.md

| Cost item | Platform | Source | Monthly amount | Annual amount | Fixed or variable | Confidence | Notes |
|-----------|----------|--------|---------------|--------------|-------------------|------------|-------|
| Compute — node pools | | AWS CUR / Azure | | | Variable | H / M / L | |
| Compute — reserved instances | | AWS CUR / Azure | | | Fixed | H / M / L | |
| Compute — spot usage | | AWS CUR / Azure | | | Variable | H / M / L | |
| Storage — block | | AWS CUR / Azure | | | Variable | H / M / L | |
| Storage — object | | AWS CUR / Azure | | | Variable | H / M / L | |
| Network — load balancers | | AWS CUR / Azure | | | Variable | H / M / L | |
| Network — NAT gateways | | AWS CUR / Azure | | | Variable | H / M / L | |
| Network — data egress | | AWS CUR / Azure | | | Variable | H / M / L | |
| Other | | | | | | H / M / L | |
| **Subtotal** | | | | | | | |

---

## Bucket 2 — Managed Service Fees

> Populated in Workshop 2 using cloud billing exports
> See: templates/working-documents/data-request-list.md

| Cost item | Platform | Source | Monthly amount | Annual amount | Fixed or variable | Confidence | Notes |
|-----------|----------|--------|---------------|--------------|-------------------|------------|-------|
| Managed K8s cluster fees | | AWS CUR / Azure | | | Variable | H / M / L | |
| Other managed service fees | | | | | | H / M / L | |
| **Subtotal** | | | | | | | |

---

## Bucket 3 — Platform Tooling

> Populated in Workshop 2 using tooling list and invoices
> Note duplication — same capability across multiple platforms
> See: templates/working-documents/data-request-list.md

| Cost item | Platform(s) | Source | Monthly amount | Annual amount | Fixed or variable | Duplicated? | Confidence | Notes |
|-----------|-------------|--------|---------------|--------------|-------------------|-------------|------------|-------|
| Observability — monitoring | | Invoice / cloud | | | | Y / N | H / M / L | |
| Observability — logging | | Invoice / cloud | | | | Y / N | H / M / L | |
| Security — scanning | | Invoice / cloud | | | | Y / N | H / M / L | |
| Security — policy enforcement | | Invoice / cloud | | | | Y / N | H / M / L | |
| CI/CD tooling | | Invoice / cloud | | | | Y / N | H / M / L | |
| Backup and DR | | Invoice / cloud | | | | Y / N | H / M / L | |
| Other tooling | | | | | | Y / N | H / M / L | |
| **Subtotal** | | | | | | | | |

**Tooling duplication identified:**

| Capability | Platforms it runs on | Estimated duplication cost | Notes |
|------------|---------------------|--------------------------|-------|
| | | | |

---

## Bucket 4 — Subscriptions

> Populated in Workshop 2 using subscription and licence details
> See: templates/working-documents/data-request-list.md

| Cost item | Renewal date | Source | Monthly amount | Annual amount | Fixed or variable | Confidence | Notes |
|-----------|-------------|--------|---------------|--------------|-------------------|------------|-------|
| [SUBSCRIPTION A] | | Invoice | | | Fixed | H / M / L | |
| [SUBSCRIPTION B] | | Invoice | | | Fixed | H / M / L | |
| Support agreement | | Invoice | | | Fixed | H / M / L | |
| Other | | | | | | H / M / L | |
| **Subtotal** | | | | | | | |

---

## Bucket 5 — Operating Effort

> Estimated in Workshop 2 using platform team input
> See: templates/working-documents/data-request-list.md
> See: templates/working-documents/assumptions-register.md — Rule 3

| Activity | % of team time | FTE equivalent | Monthly cost estimate | Annual cost estimate | Confidence | Notes |
|----------|---------------|---------------|----------------------|---------------------|------------|-------|
| Upgrades and patching | | | | | H / M / L | |
| Incident response and on-call | | | | | H / M / L | |
| Onboarding new teams and workloads | | | | | H / M / L | |
| Building and maintaining standards | | | | | H / M / L | |
| Other operational activities | | | | | H / M / L | |
| **Subtotal** | 100% | | | | | |

**Basis for estimate:**

| Field | Value |
|-------|-------|
| Total platform team size (FTE) | |
| Blended cost per FTE per month | |
| Source or basis for FTE cost | |

---

## Bucket 6 — Shared Services

> Populated in Workshop 2 — often the least complete bucket in first pass
> See: templates/working-documents/assumptions-register.md — Section 2

| Cost item | Source | Monthly amount | Annual amount | Fixed or variable | Allocated? | Confidence | Notes |
|-----------|--------|---------------|--------------|-------------------|------------|------------|-------|
| Identity and access management | | | | | Y / N | H / M / L | |
| Shared network infrastructure | | | | | Y / N | H / M / L | |
| Shared logging platform | | | | | Y / N | H / M / L | |
| Other shared services | | | | | Y / N | H / M / L | |
| **Subtotal** | | | | | | | |

---

## Baseline Summary

> Complete this section once all six buckets are populated

### Total by bucket

| Bucket | Monthly total | Annual total | % of total | Confidence |
|--------|--------------|-------------|------------|------------|
| 1. Cloud infrastructure | | | | H / M / L |
| 2. Managed service fees | | | | H / M / L |
| 3. Platform tooling | | | | H / M / L |
| 4. Subscriptions | | | | H / M / L |
| 5. Operating effort | | | | H / M / L |
| 6. Shared services | | | | H / M / L |
| **Total** | | | 100% | |

### Fixed versus variable split

| | Monthly amount | % of total |
|-|---------------|------------|
| Fixed costs | | |
| Variable costs | | |
| **Total** | | 100% |

### Total by platform

| Platform | Monthly total | Annual total | % of total | Notes |
|----------|--------------|-------------|------------|-------|
| [PLATFORM A] | | | | |
| [PLATFORM B] | | | | |
| [PLATFORM C] | | | | |
| Shared / unallocated | | | | |
| **Total** | | | 100% | |

---

## Key findings

> Populate after the baseline summary is complete

**Where spend concentrates:**

```
Notes:
```

**Fixed versus variable observations:**

```
Notes:
```

**Tooling duplication cost:**

```
Notes:
```

**Gaps still to close:**

```
Notes:
```
