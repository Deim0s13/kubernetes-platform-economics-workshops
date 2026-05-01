# 90-Day Plan

**Organisation:** [ORGANISATION]
**Facilitator:** [FACILITATOR]
**Version:** [VERSION]
**Last updated:** [DATE]
**Recommended scenario:** [CARRY FORWARD FROM scenario-comparison.md]

---

## Version history

| Version | Date | What changed |
|---------|------|-------------|
| v1.0 | [DATE] | Plan agreed — Workshop 5 |

---

## What this document is

This is the 90-day plan agreed upon in Workshop 5. It translates the recommended scenario into a practical, actionable set of next steps that leadership can approve and the team can execute.

It is structured across three tracks so that actions, decisions, and investigations are kept clearly separate, and nothing starts before it should..

> This document was agreed upon in Workshop 5. It cannot be completed without > the scenario comparison and recommendation.
>
> See: workshop-5-scenarios/attendee-materials.md, Section 4
> See: templates/working-documents/scenario-comparison.md

---

## How to use this plan

**Track 1 — No-regrets actions** can start immediately. They make sense regardless of which scenario is chosen and do not require additional leadership approval beyond sign-off on this plan.

**Track 2 — Decisions required** must be escalated to leadership before the recommended scenario can be fully committed to. These are not actions; they are questions that need answers.

**Track 3 — Pilots and spikes** are time-boxed investigations that validate key assumptions before committing to structural change. They have a defined scope, clear success criteria, and a named owner.

---

## Track 1 — No-Regrets Actions

> Start these now. Every action needs a named owner and a realistic > completion date within 90 days.

| Action | Why it matters | Owner | Start date | Target date | Expected outcome | Status |
|--------|---------------|-------|-----------|------------|-----------------|--------|
| | | | | | | Not started |
| | | | | | | Not started |
| | | | | | | Not started |
| | | | | | | Not started |
| | | | | | | Not started |

**Common no-regrets actions to consider:**

- Rightsize oversized node pools and enforce resource requests and limits.
- Retire or merge clearly redundant non-production clusters.
- Improve tagging and labelling to close allocation gaps.
- Consolidate duplicated tooling where the case is unambiguous.
- Establish or enforce autoscaling policies across clusters.
- Document justified exceptions from the workload placement matrix.

---

## Track 2 — Decisions Required

> These must go to leadership. Be explicit about the options and > what is at stake. Do not bury these in the appendix of the brief.

| Decision | What is being decided | Who decides | Options | By when | Escalated? |
|----------|--------------------|-------------|---------|---------|------------|
| | | | | | Y / N |
| | | | | | Y / N |
| | | | | | Y / N |

**Common decisions that need leadership input:**

- Commercial or procurement approach, renew, restructure, or phase. Organisational commitment to a preferred platform model
- Resourcing for migration or consolidation work
- Risk appetite for migration sequencing
- Governance model for a hybrid portfolio (if Scenario D)

---

## Track 3 — Pilots and Spikes

> Time-boxed. Defined scope. Clear success criteria. Named owner.
> A pilot or spike that runs indefinitely is not a pilot or spike.

| Pilot or spike | What we are testing | Scope | Success criteria | Duration | Owner | Start date |
|----------------|-------------------|-------|-----------------|----------|-------|-----------|
| | | | | | | |
| | | | | | | |
| | | | | | | |

**Common pilots and spikes to consider:**

- Managed Kubernetes viability spike, stood up a landing zone and migrated one or two consolidation candidates to validate the operational model, cost, and migration approach.
- Consolidation pilot, migrate a small set of workloads to validate the placement matrix findings and the migration approach at low risk.
- Tagging and allocation spike, implement the agreed tagging standard across one platform and validate the showback view improvement.

---

## Progress tracking

> Review this plan monthly. Update status, note blockers, and flag
> any decisions that are stalling.

| Review date | Track 1 progress | Track 2 progress | Track 3 progress | Blockers | Notes |
|-------------|-----------------|-----------------|-----------------|----------|-------|
| [DATE + 30 days] | | | | | |
| [DATE + 60 days] | | | | | |
| [DATE + 90 days] | | | | | |

---

## What success looks like at 90 days

> Agree on these in Workshop 5 alongside the plan.

| Measure | Current baseline | 90-day target | How we will verify |
|---------|----------------|--------------|-------------------|
| | [CARRY FORWARD FROM unit-metrics-definition.md] | | |
| | [CARRY FORWARD FROM value-risk-scorecard.md] | | |
| | | | |

---

## Owners and accountabilities

| Role | Name | Accountable for |
|------|------|----------------|
| Executive sponsor | | Decisions required — Track 2 |
| Plan owner | | Overall plan progress and reporting |
| Track 1 lead | | No-regrets actions delivery |
| Track 3 lead | | Pilots and spikes execution |
| Reporting cadence | | Monthly progress review |
