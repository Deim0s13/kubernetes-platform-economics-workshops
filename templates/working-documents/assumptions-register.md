# Assumptions Register

**Organisation:** [ORGANISATION]
**Facilitator:** [FACILITATOR]
**Version:** [VERSION]
**Last updated:** [DATE]
**Status:** Active

---

## Version history

| Version | Date | Changed by | What changed |
|---------|------|------------|-------------|
| v0.1 | [DATE] | [FACILITATOR] | Document created — Workshop 0 |
| v1.0 | [DATE] | [FACILITATOR] | Scope and rules agreed — Workshop 1 |

---

## What this document is

The Assumptions Register is the single source of truth for every decision made about scope, cost treatment, allocation, and data confidence throughout the platform economics assessment.

Every time a decision is made in a workshop, what to include, how to treat a shared cost, and which proxy to use, it is recorded here. This is what makes the final output defensible. When Finance or Procurement asks “why did you include that?” or “how did you treat shared tooling costs?” the answer is in this document, with a date and a version number.

> This document is started in Workshop 0 and updated after every > subsequent workshop. It is never complete until the decision brief > has been finalised and reviewed.
>
> See: workshop-0-setup/attendee-materials.md

---

## Section 1 — Scope

> Agreed in Workshop 1 — Scope, Glossary, and Rules of the Game
> See: workshop-1-scope/attendee-materials.md

### Platforms in scope

| Platform | Role in assessment | Confirmed in scope? | Notes |
|----------|--------------------|--------------------|----|
| [PLATFORM A] | Baseline | | |
| [PLATFORM B] | Baseline | | |
| [PLATFORM C] | Baseline | | |
| [PLATFORM D] | Scenario only | | |
| [PLATFORM E] | Scenario only | | |

### Environments

| Environment | In scope? | Treatment | Notes |
|-------------|-----------|-----------|-------|
| Production | | | |
| Non-production | | Separate / combined | |

### Time window

| Field | Value |
|-------|-------|
| Start date | |
| End date | |
| Reason for this window | |

### Cost types in scope

| Cost type | In scope? | Confidence | Notes |
|-----------|-----------|------------|-------|
| Cloud compute | | H / M / L | |
| Cloud storage | | H / M / L | |
| Cloud network and egress | | H / M / L | |
| Managed service fees | | H / M / L | |
| Platform tooling | | H / M / L | |
| Subscriptions | | H / M / L | |
| Operating effort | | H / M / L | |
| Shared services | | H / M / L | |

### Explicit exclusions

| Item excluded | Reason | Impact on completeness |
|---------------|--------|----------------------|
| | | |

---

## Section 2 — Cost Treatment Rules

> Agreed in Workshop 1 — Scope, Glossary, and Rules of the Game
> See: workshop-1-scope/attendee-materials.md

### Rule 1 — Shared platform costs

| Field | Decision |
|-------|---------|
| Method agreed | Proportional / Equal / Unallocated bucket |
| Reason | |
| Agreed in | Workshop 1 |
| Version recorded | |

### Rule 2 — Non-production environments

| Field | Decision |
|-------|---------|
| Method agreed | Separate line / Combined / Excluded from unit economics |
| Reason | |
| Agreed in | Workshop 1 |
| Version recorded | |

### Rule 3 — Operating effort

| Field | Decision |
|-------|---------|
| Method agreed | Time split / Hours per activity / Excluded |
| Basis for estimate | |
| Confidence | H / M / L |
| Agreed in | Workshop 1 |
| Version recorded | |

### Rule 4 — Tooling duplication

| Field | Decision |
|-------|---------|
| Method agreed | Separate line / Included in tooling / Not modelled |
| Reason | |
| Agreed in | Workshop 1 |
| Version recorded | |

---

## Section 3 — Allocation Rules

> Agreed in Workshop 3 — Allocation Rules and Unit Economics
> See: workshop-3-unit-economics/attendee-materials.md

### Shared platform cost allocation

| Field | Decision |
|-------|---------|
| Method | |
| Applied to | |
| Confidence | H / M / L |
| Agreed in | Workshop 3 |
| Version recorded | |

### Platform tooling allocation

| Field | Decision |
|-------|---------|
| Method | |
| Applied to | |
| Confidence | H / M / L |
| Agreed in | Workshop 3 |
| Version recorded | |

### Operating effort allocation

| Field | Decision |
|-------|---------|
| Method | |
| Applied to | |
| Confidence | H / M / L |
| Agreed in | Workshop 3 |
| Version recorded | |

### Minimum tagging standard

| Tag or label | What it identifies | Coverage | Gap? |
|-------------|-------------------|----------|------|
| | | | |
| | | | |

---

## Section 4 — Unit Metrics

> Agreed in Workshops 1 and 3
> See: workshop-1-scope/attendee-materials.md
> See: workshop-3-unit-economics/attendee-materials.md

| Metric | Numerator | Denominator | Data source | Confidence | Agreed in |
|--------|-----------|-------------|-------------|------------|-----------|
| | | | | H / M / L | |
| | | | | H / M / L | |
| | | | | H / M / L | |
| | | | | H / M / L | |
| | | | | H / M / L | |

---

## Section 5 — Data Sources

> Populated across Workshops 1 and 2
> See: workshop-1-scope/attendee-materials.md
> See: workshop-2-cost-baseline/attendee-materials.md

| Data item | Source | Owner | Date received | Confidence | Notes |
|-----------|--------|-------|--------------|------------|-------|
| Cloud billing exports | | | | H / M / L | |
| Cluster inventory | | | | H / M / L | |
| Platform subscription | | | | H / M / L | |
| Tooling list and costs | | | | H / M / L | |
| Operating effort estimate | | | | H / M / L | |
| Production app list | | | | H / M / L | |
| Namespace or team mapping | | | | H / M / L | |
| Utilisation data | | | | H / M / L | |

---

## Section 6 — Known Gaps and Mitigations

> Updated across all workshops
> Any gap that affects confidence in the final output must be noted here.

| Gap | Impact on output | Mitigation agreed | Owner | Status |
|-----|----------------|------------------|-------|--------|
| | High / Medium / Low | Estimate / Exclude / Defer | | Open / Closed |
| | High / Medium / Low | Estimate / Exclude / Defer | | Open / Closed |
| | High / Medium / Low | Estimate / Exclude / Defer | | Open / Closed |

---

## Section 7 — Decisions Requiring Revision

> If any assumption changes after it has been agreed, record the change
> here, bump the document version, and note the impact on downstream outputs.

| Original decision | Changed to | Reason | Version changed | Impact on outputs |
|------------------|------------|--------|-----------------|-------------------|
| | | | | |

---

## Confidence rating guide

| Rating | What it means |
|--------|--------------|
| High | Based on actual measured data from a reliable source |
| Medium | Based on an estimate with a reasonable basis — directionally sound |
| Low | Based on a rough guess or proxy — treat as indicative only |

---

## Sign-off

| Role | Name | Date | Notes |
|------|------|------|-------|
| Facilitator | | | |
| Product Owner | | | |
| Platform Lead | | | |
