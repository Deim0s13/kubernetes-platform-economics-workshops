# Workshop 3 — Facilitator Guide
## Allocation Rules and Unit Economics

**Version:** 1.0
**Duration:** 2 hours
**Audience:** Product Owner, Platform Lead, Platform Engineers and SREs
**Facilitator:** [FACILITATOR]

---

## Version history

| Version | Date | Changes |
|---------|------|---------|
| 1.0 | [DATE] | Initial version |

---

## Purpose

Workshop 3 is where the cost model becomes useful to leadership. The goal is to translate the baseline built in Workshop 2 into unit economics, cost per useful outcome, using agreed allocation rules.

By the end of this session, the group will have moved from "we spend X on Kubernetes" to "a production application costs Y per month." That is the shift that makes the output actionable for a CIO, a CFO, and a procurement
team.

By the end of this session, you will have:

- Agreed allocation rules and how shared costs are distributed are documented in the Assumptions Register.
- A unit economics model with baseline values for three to five metrics
- A showback view, cost mapped to teams, products, or namespaces
- A clear narrative connecting cost to platform outcomes
- A foundation for the scenario modelling in Workshop 5

---

## Before the session

### Update the baseline model

Before Workshop 3, update the baseline model with any data that has come in since Workshop 2. Share the updated version with attendees at least 24 hours before the session so they can review it and surface any concerns
early.

Note anything that has changed significantly since Workshop 2, unexpected numbers, new gaps, or anomalies that need addressing in the session.

### Prepare the unit economics template

Set up a unit economics template in the working model before the session. It should have a tab or section for each shortlisted metric with fields for:

- Metric name and definition
- Numerator, costs included
- Denominator, what we divide by
- Data sources
- Baseline value
- Confidence rating
- Notes and assumptions

### Review the unit metrics shortlist

Confirm the three to five metrics shortlisted in Workshop 1. Check whether any data constraints mean a metric needs to be swapped or deferred. Better to know this before the session than to discover it mid-exercise.

### Check namespace and team mapping

If namespace or team mapping data has come in, review it before the session. This is the foundation for the showback view and cost-per-tenant metrics. If it has not come in, agree on an approach before the session, estimate, defer, or use a proxy.

---

## Session agenda

| Time | Section | Duration |
|------|---------|----------|
| 0:00 | Welcome, recap, and outcomes | 10 minutes |
| 0:10 | Agree allocation rules | 25 minutes |
| 0:35 | Build unit economics — metric by metric | 50 minutes |
| 1:25 | Showback view | 15 minutes |
| 1:40 | Close and next steps | 10 minutes |

---

## Section-by-section guidance

---

### Welcome, recap, and outcomes (10 minutes)

**What you are doing**

Opening the session, recapping Workshop 2, acknowledging any data that has come in, and setting clear expectations for what this session will produce.

**Talk track**

*"Welcome back. In Workshop 2 we built the cost taxonomy and mapped known spend into the baseline model. Since then [DATA UPDATES IF ANY].*

*Today, we take that baseline and turn it into something leadership can act on. We are going to agree on how to allocate shared costs, build a unit economics model, and create a showback view that maps costs to teams and
products.*

*By the end of this session, we will have moved from 'we spend X on Kubernetes' to 'a production application costs Y per month.' That is the shift that makes this output useful to a CIO, a CFO, and a procurement team."*

Check in:

*"Anything from Workshop 2 that needs clearing up, or anything in the updated baseline that surprised you?"*

**Facilitation notes**

- If the updated baseline has surprises, acknowledge them and agree whether to investigate now or note and move on.
- If significant data gaps remain, be direct about the impact on confidence and the plan to close them.
- Keep this section to ten minutes. The allocation rules exercise is where the session earns its value.

---

### Agree allocation rules (25 minutes)

**What you are doing**

Agreeing on how shared costs are distributed across platforms, teams, and workloads, and documenting every decision in the Assumptions Register.

**Why this matters**

Unit economics cannot be calculated without allocation rules. If shared costs are not distributed, the unit metrics are incomplete. If they are distributed inconsistently, the metrics are not comparable.

This section is where the work gets political; someone will question why their team or platform is bearing a particular share of shared cost. Stay neutral, apply the rules consistently, and keep coming back to:

*"We are building showback, not chargeback. We are making costs visible, not billing anyone for them yet."*

**Talk track**

*"Before we can calculate unit metrics, we need to agree on how to handle shared costs, the costs that serve more than one platform or team and cannot be cleanly attributed to one place.*

*We agreed in Workshop 1 that we would use showback first, making costs visible before billing anyone. Today, we agree on the rules for distributing those shared costs in the model.*

*These rules will be applied consistently throughout. Every decision is recorded in the Assumptions Register. If we change a rule later, we version it."*

Work through these allocation decisions in order:

**Allocation method for shared platform costs**

*"We agreed in Workshop 1 to [RULE FROM WORKSHOP 1]. Does that still hold, or has anything changed now that we can see the actual numbers?"*

If still agreed, confirm and move on. If challenged, work through the options again:

- Proportional by usage, requires utilisation data or tag-based consumption
- Equal split across platforms, simpler, less precise
- Shared unallocated bucket, honest about uncertainty, refine later.

Record the decision and the reason.

**Allocation method for platform tooling**

*"For tooling that serves multiple platforms, observability, security, CI/CD, how do we want to allocate that cost across platforms?"*

Options:

- Allocate by number of clusters or nodes per platform.
- Allocate equally across platforms.
- Hold unallocated and note as a shared cost.

Record the decision. If tooling duplication was identified in Workshop 2, note the duplication cost as a separate line rather than allocating it.

**Allocation method for operating effort**

*"For operating effort — the platform team's time, how do we want to allocate that across platforms and workloads?"*

Options:

- Allocate by estimated time spent per platform.
- Allocate equally across platforms.
- Hold as a platform-level cost and not allocate to workloads.

Record the decision.

**Minimum tagging and labelling standard**

*"For costs to be allocated by namespace or team, we need a minimum tagging standard in place. What tags or labels exist today, and what is the minimum we need for the showback view to work?"*

Agree on a minimum viable tagging standard and note it in the Assumptions Register. Flag any gaps as an improvement in the output.

**Facilitation notes**

- If someone challenges an allocation rule, ask: *"What would you suggest instead, and can we apply it consistently across all platforms?"*
- Allocation debates can run long. Time-box each decision to five minutes. If agreement is not reached, default to the simpler option and note the reason.
- Watch for the person who wants to relitigate Workshop 1 decisions. Acknowledge the concern and park it: 
*"That is a valid point, let us note it as a sensitivity in the model and come back to it in Workshop 5 when we look at scenarios."*

---

### Build unit economics — metric by metric (50 minutes)

**What you are doing**

Working through each shortlisted metric and calculating a baseline value. This is the core exercise of Workshop 3, and the one that produces the most valuable output.

**How to run it**

Work through each metric in turn. For each one:

1. Confirm the definition — numerator, denominator, data sources
2. Apply the allocation rules agreed above
3. Calculate the baseline value — or agree an estimate with a confidence rating
4. Note what the number means and what it enables

Allow roughly ten minutes per metric. Keep pace steady, it is better to have three well-defined metrics than five poorly understood ones.

**Metric by metric guidance**

**Cost per production app per month**

Definition:
- Numerator: total platform cost allocated to production environments
- Denominator: number of production applications

*"This is the headline metric for most leadership conversations. It answers the question: 'what does it actually cost us to run one production application on this platform?'"*

What to look for:
- Is the number higher or lower than expected?
- Is there significant variation across platforms? Does an app cost more on one platform than another?
- What is driving the cost, compute, tooling, ops effort?

**Cost per tenant or namespace per month**

Definition:
- Numerator: total platform cost allocated to a team or namespace
- Denominator: number of active tenants or namespaces

*"This is the most useful metric if you run a multi-tenant platform. It tells you what it costs to serve one team or product."*

What to look for:
- Are costs distributed evenly, or are some tenants significantly more expensive to serve than others?
- Are there inactive namespaces consuming cost?
- Does the cost per tenant reflect the value each tenant gets from the platform?

**Cost per environment**

Definition:
- Numerator: total cost for production environments / total cost for non-production environments
- Denominator: not applicable, this is a split, not a unit cost.

*"This tells us how much of our total platform cost is serving production versus non-production. A high non-production share often signals cluster sprawl or over-provisioning in dev and test environments."*

What to look for:
- Is the non-production share higher than expected?
- Are there non-production clusters that are running continuously when they could be ephemeral?

**Effective cost per vCPU-hour used**

Definition:
- Numerator: total compute cost
- Denominator: actual vCPU hours consumed (not requested or purchased)

*"This is the utilisation metric. It tells us how efficiently we are using the capacity we pay for.*

*Most estates have a meaningful gap between what they purchase and what they actually use. That gap is often the most straightforward cost improvement available, because it does not require a structural change, just better utilisation."*

What to look for:
- What is the gap between purchased, requested, and used?
- Is the gap consistent across platforms or concentrated on specific clusters?
- Is the gap consistent across platforms, or is it concentrated in specific clusters?

**Ops cost per cluster per month**

Definition:
- Numerator: operating effort cost allocated to a cluster
- Denominator: number of clusters

*"This tells us the operational overhead of each cluster, the cost in people time to keep it running. It is one of the clearest signals for cluster consolidation."*

What to look for:
- Is the ops cost per cluster consistent or highly variable?
- Are some clusters disproportionately expensive to operate?
- What would the ops cost look like if cluster count were reduced?

**Facilitation notes**

- If data is missing for a metric, agree on an estimate with a confidence rating rather than skipping the metric entirely.
- If a calculated number surprises the group, note it and briefly explore it, but do not turn it into a full investigation. The finding belongs in the scenario modelling in Workshop 5.
- If the group struggles with a denominator, for example, “we do not have a reliable production app count”, agree on a proxy and note the confidence impact.
- Keep the model visible on screen and update it live. Seeing numbers appear in real time keeps people engaged and surfaces reactions quickly.

---

### Showback view (15 minutes)

**What you are doing**

Building a first-pass showback view, cost mapped to teams, products, or namespaces, using the allocation rules and unit metrics agreed today.

**Talk track**

*"Now that we have unit metrics and allocation rules in place, I want to build a first-pass showback view, a report that shows what each team or product is spending on the platform.*

*This is showback, not chargeback. We are making costs visible, not billing anyone. The value of this is that it creates accountability and surfaces conversations that would otherwise not happen.*

*What does your current namespace or team mapping look like? Let us use that to structure the view."*

Work through the showback structure:

- Rows: teams, products, or namespaces, whichever is most meaningful
- Columns: cost bucket breakdown, total cost, cost as a percentage of platform total, unit metric where applicable

If the namespace or team mapping is incomplete, agree on a proxy structure and note the confidence rating.

**Facilitation notes**

- If the showback view surfaces a team that is significantly more expensive than others, handle it carefully. The finding is valuable but can trigger defensiveness. Frame it as: *"This tells us something worth understanding, not something to assign blame for."*
- If tagging is insufficient to build a meaningful showback view, agree on a platform-level showback as a first pass and flag tagging improvements as a quick win in the output.

---

### Close and next steps (10 minutes)

**What you are doing**

Summarising what was produced, confirming the unit economics model is saved and shared, and making Workshop 4 completely clear.

**Talk track**

*"Here is what we have built today. We have agreed allocation rules, calculated baseline unit metrics for [METRICS], and built a first-pass showback view.*

*These numbers, cost per app, cost per tenant, and effective cost per vCPU, are what will land with leadership and Finance. They connect the platform cost to something the business recognises.*

*Workshop 4 is [DATE/TIME]. That is where we look at the other side of the equation, what value the platform is actually delivering. We will build a value and risk scorecard using DORA and SPACE as reference points, so cost is not the only lens leadership is looking through.*

*You will get a short recap from me within 24 hours, decisions made, actions, and the Workshop 4 pre-read."*

Then ask the final question:

*"Looking at these unit metrics, does anything surprise you? And is there anything that looks wrong before we go further?"*

---

## Handling difficult moments

### "Our tagging is too inconsistent to allocate costs properly"

Do not treat this as a blocker. Treat it as a finding.

*"Tagging gaps is a signal about how platform cost is currently managed. We will note the current state, use a proxy allocation for the model, and flag tagging improvement as a quick win in the output."*

### "That cost per app number seems way too high"

Explore it briefly rather than dismissing it.

*"Let us look at what is driving it. Is it compute? Tooling overhead? Operating effort? Understanding the driver is more useful than debating the number."*

### "Why is our non-production cost so high?"

This is one of the most common and most valuable findings.

*"High non-production cost is often a sign of cluster sprawl or over-provisioning in dev and test. It is one of the levers we will look at in the scenario modelling in Workshop 5."*

### "We do not have a reliable production app count"

*"A rough count is enough for the first pass. We will apply a Low confidence rating and note the assumption. If the number changes significantly when we have better data, we update the model."*

### Someone starts comparing platforms directly

This is a good sign, but handle it carefully. Direct comparison is the territory of Workshop 5.

*"That is exactly the kind of comparison we will do in Workshop 5 with the scenario modelling. For now, let us make sure the unit metrics are solid; we want the comparison to be based on good numbers."*

---

## Output checklist

Before you close the session, confirm these are in place:

- [ ] Allocation rules agreed and documented in the Assumptions Register.
- [ ] Unit economics model populated with baseline values
- [ ] Confidence ratings applied to every metric.
- [ ] Showback view built, at least first pass
- [ ] Assumptions Register updated with all allocation decisions.
- [ ] Workshop 4 date and time confirmed

---

## Post-session actions (within 24 hours)

- [ ] Send recap email, decisions made, actions, Workshop 4 confirmed.
- [ ] Save and share the unit economics model, clearly versioned.
- [ ] Save and share the showback view, clearly versioned.
- [ ] Update the Assumptions Register, version bumped with today's date.
- [ ] Send Workshop 4 pre-read and calendar invite.
- [ ] Follow up on any outstanding data items that affect unit metric confidence ratings.
