# Workshop 3 — Slides
## Allocation Rules and Unit Economics

**Version:** 1.0
**Last updated:** [DATE]
**Corresponding facilitator guide:** facilitator-guide.md v1.0

---

## Version history

| Version | Date | Changes |
|---------|------|---------|
| 1.0 | [DATE] | Initial version |

---

## How to use this file

Each slide includes a title, layout note, content, and speaker notes. Build your presentation deck from this file. This file is the source of truth. If you update the deck, update this file to match and bump the version number.

Speaker notes are written in your voice, conversational and plain. They are not a script to read verbatim, but a guide for what to cover and how to frame it.

---

## Slide 1: Title

**Layout:** Title slide — centred title, subtitle, and session details below

### Content

```
Kubernetes Platform Economics

Workshop 3 — Allocation Rules and Unit Economics

[DATE] | [FACILITATOR]
```

### Speaker Notes

Open with the slide visible and move straight into the recap of Workshop 2.
Do not linger here.

---

## Slide 2: Where We Are

**Layout:** Title at top, horizontal progress indicator with Workshop 3 highlighted

### Content

```
Workshop 0    Workshop 1    Workshop 2    Workshop 3    Workshop 4    Workshop 5
Setup         Scope, and     Cost          Unit          Value, and     Scenarios
              Rules         Baseline      Economics     Risk          and Plan

                                          [YOU ARE HERE]
```

### Speaker Notes

"In Workshop 2, we built the cost taxonomy and mapped known spend into the baseline model.

Today, we take that baseline and turn it into something leadership can act on. We are going to agree on allocation rules, build a unit economics model, and create a showback view that maps cost to teams and products."

---

## Slide 3: What We Are Producing Today

**Layout:** Title at top, clean list of five outputs

### Content

```
By the end of this session, we will have:

Agreed allocation rules — documented in the Assumptions Register

A unit economics model — baseline values for three to five metrics

A showback view — cost mapped to teams, products, or namespaces

A clear narrative — what does the platform cost per outcome?

A foundation for scenario modelling in Workshop 5
```

### Speaker Notes

"Today is where the cost model becomes useful to leadership.

We are moving from 'we spend X on Kubernetes' to ' a production application costs Y per month.' That is the shift that makes this output actionable for a CIO, a CFO, and a procurement team."

---

## Slide 4: Why Unit Economics — Not Just Total Cost

**Layout:** Title at top, two contrasting statements with explanation

### Content

```
Total cost is a number.

Unit economics is what that number means.

"We spend X on Kubernetes"
    Hard to act on. Hard to compare. Hard to defend.

"A production application costs Y per month"
    Leadership can act on this.
    Finance can benchmark this.
    Procurement can evaluate this.

The same spend. A completely different conversation.
```

### Speaker Notes

"When a CIO or CFO asks 'is this platform good value?' the answer cannot be 'it costs X.' The answer needs to connect cost to something the business recognises, an application, a team, a deployment, a
unit of capacity.

That connection is what unit economics gives us. It does not change the numbers. It changes what the numbers mean."

---

## Slide 5: What Allocation Rules Are

**Layout:** Title at top, plain explanation with a simple example

### Content

```
Some costs are straightforward to attribute.
A node pool running a specific workload.
A subscription that serves one platform.

Others are genuinely shared.
An observability stack serving three platforms.
A network platform serving the whole estate.

Allocation rules are the agreed method for distributing shared costs fairly and consistently.

They do not need to be perfect.
They need to be agreed upon, documented, and applied consistently.
```

### Speaker Notes

"Before we can calculate unit metrics, we need to agree on how to handle shared costs, the costs that serve more than one platform or team.

Allocation rules are how we do that. They do not need to be perfect; they need to be agreed and applied consistently so the output is comparable and defensible.

And we are doing showback first. That means we make costs visible before we start billing anyone for them."

---

## Slide 6: Allocation — Shared Platform Costs

**Layout:** Title at top, three options clearly laid out with space to record the decision

### Content

```
How do we distribute costs that serve multiple platforms?

Option A    Proportional by usage
            Most accurate — requires utilisation or tag data

Option B    Equal split across platforms
            Simpler — less precise

Option C    Shared unallocated bucket
            Honest about uncertainty — refine later

We agreed on in Workshop 1 to use: [RULE FROM WORKSHOP 1]

Does that still hold now that we can see the actual numbers?

Decision:
```

### Speaker Notes

"We agreed a rule for this in Workshop 1. Now that we have actual numbers in the model, I want to confirm it still makes sense.

Work through any challenges calmly. If someone questions the rule, ask: 'What would you suggest instead, and can we apply it consistently across all platforms?'

Record the confirmed decision in the Assumptions Register."

---

## Slide 7: Allocation — Platform Tooling

**Layout:** Title at top, three options and decision prompt

### Content

```
How do we allocate tooling that serves multiple platforms? (Observability, security, CI/CD)

Option A    Allocate by cluster or node count per platform

Option B    Allocate equally across platforms

Option C    Hold as shared — do not allocate to platforms

Note: Where tooling duplication exists, model it as a separate line rather than allocating it.

Decision:
```

### Speaker Notes

"For tooling that serves more than one platform, we need a consistent allocation rule.

If we identified tooling duplication in Workshop 2, the same capability running separately across multiple platforms, we model that duplication cost as its own line rather than allocating it. That keeps it visible
as a lever in Workshop 5."

Record the decision in the Assumptions Register.

---

## Slide 8: Allocation — Operating Effort

**Layout:** Title at top, three options and decision prompt

### Content

```
How do we allocate platform team time across platforms and workloads?

Option A    Allocate by estimated time spent per platform

Option B    Allocate equally across platforms

Option C    Hold as a platform-level cost — do not allocate
            to individual workloads

Decision:
```

### Speaker Notes

"Operating effort is often the trickiest to allocate because the data is an estimate rather than a measured number.

Option C is often the most practical for the first pass; it keeps operating effort visible as a platform cost without trying to distribute an estimate too precisely.

Record the decision and the reason."

---

## Slide 9: Minimum Tagging Standard

**Layout:** Title at top, explanation and table for live population

### Content

```
To allocate costs by namespace or team, we need a minimum tagging standard.

What tags or labels exist today?

Tag / label          What it identifies          Coverage
[TAG]
[TAG]
[TAG]

What is the minimum we need for showback to work?

Gaps to close:
```

### Speaker Notes

"Tagging is the foundation of the showback view. Without it, we cannot allocate costs to teams or products meaningfully.

I want to understand what exists today and agree on the minimum standard we need for this work. Any gaps become a quick win in the output. Improving tagging is usually low effort and high value."

Capture the agreed minimum standard and tag gaps in the Assumptions Register.

---

## Slide 10: The Unit Metrics We Are Building

**Layout:** Title at top, table of shortlisted metrics confirmed in Workshop 1

### Content

```
In Workshop 1, we shortlisted these metrics:

[METRIC 1]
[METRIC 2]
[METRIC 3]
[METRIC 4]
[METRIC 5]

For each one, we will define:

Numerator:      Which costs are included
Denominator:    What we divide by
Data sources:   Where the numbers come from
Confidence:     How certain we are about the result
```

### Speaker Notes

"These are the metrics we agreed to build in Workshop 1. Today, we bring them to life with actual numbers.

We will work through each one in turn. The goal is a baseline value for each metric, even if some of those values carry a Low confidence rating to start with."

---

## Slide 11: Metric — Cost Per Production App Per Month

**Layout:** Title at top, definition and calculation fields to be populated live

### Content

```
What it tells you:
What it costs to run one production application on this platform.

Numerator:
Total platform cost allocated to production environments

Denominator:
Number of production applications

Data sources:
[POPULATE IN SESSION]

Baseline value:
[POPULATE IN SESSION]

Confidence:    H / M / L

What does this number enable?
[POPULATE IN SESSION]
```

### Speaker Notes

"This is the headline metric for most leadership conversations.

When someone asks 'is this platform good value?' this is the number that answers it, or at least starts the conversation.

What is driving the cost? Is it compute, tooling overhead, or operating effort? Understanding the driver is as important as the number itself."

Populate the slide live. Note any surprises and what they might signal.

---

## Slide 12: Metric — Cost Per Tenant or Namespace Per Month

**Layout:** Title at top, definition and calculation fields to be populated live

### Content

```
What it tells you:
What it costs to serve one team or product on the platform.

Numerator:
Total platform cost allocated to a team or namespace

Denominator:
Number of active tenants or namespaces

Data sources:
[POPULATE IN SESSION]

Baseline value:
[POPULATE IN SESSION]

Confidence:    H / M / L

What does this number enable?
[POPULATE IN SESSION]
```

### Speaker Notes

"This is the most useful metric if you run a multi-tenant platform.

A few things worth exploring as we populate this: are costs distributed evenly, or are some tenants significantly more expensive to serve? Are there inactive namespaces consuming cost? Does the cost per tenant reflect the value each tenant gets from the platform?"

Populate live. Note variation across tenants if visible.

---

## Slide 13: Metric — Cost Per Environment

**Layout:** Title at top, definition and split fields to be populated live

### Content

```
What it tells you:
How much of the total platform cost is dedicated to production versus non-production?

Production cost:       [POPULATE]    [%] of total
Non-production cost:   [POPULATE]    [%] of total

Data sources:
[POPULATE IN SESSION]

Confidence:    H / M / L

What does a high non-production share signal?
Cluster sprawl. Over-provisioning in dev and test.
Environments that run continuously when they could be ephemeral.
```

### Speaker Notes

"This one is a split rather than a unit cost, but it is one of the most revealing metrics in most estates.

A high non-production share is often a sign of cluster sprawl or over-provisioning in dev and test environments. It is one of the levers we will look at in the scenario modelling in Workshop 5."

Populate live. If the non-production share is high, note it explicitly as a finding.

---

## Slide 14: Metric — Effective Cost Per vCPU-Hour Used

**Layout:** Title at top, definition, and three-level comparison to be populated live

### Content

```
What it tells you: How efficiently you are using the capacity you pay for.

Purchased / allocated:   [POPULATE]   vCPU hours
Requested:               [POPULATE]   vCPU hours
Actually used:           [POPULATE]   vCPU hours

Utilisation gap:         [POPULATE]   %

Effective cost per vCPU-hour used:    [POPULATE]

Confidence:    H / M / L

The gap between purchased and used is often where the most straightforward cost improvements sit.
```

### Speaker Notes

"This is the utilisation metric, and it is often the most eye-opening number in the whole exercise.

Most estates have a meaningful gap between what they purchase and what they actually use. That gap does not require a structural change to close; it requires better utilisation. Rightsizing, autoscaling, enforcing requests and limits.

If utilisation data is available from the monitoring platform, this metric is worth getting right. If not, we estimate with a Low confidence rating and flag it as a data gap to close."

---

## Slide 15: Metric — Ops Cost Per Cluster Per Month

**Layout:** Title at top, definition and calculation fields to be populated live

### Content

```
What it tells you:
The operational overhead of each cluster in people cost.

Numerator:
Operating effort cost allocated to clusters

Denominator:
Number of clusters

Data sources:
[POPULATE IN SESSION]

Baseline value:
[POPULATE IN SESSION]

Confidence:    H / M / L

What does a high ops cost per cluster signal?
Cluster sprawl. Clusters that are disproportionately expensive to operate relative to the workloads they run.
```

### Speaker Notes

"This metric is one of the clearest signals for cluster consolidation.

If the ops cost per cluster is high, particularly for clusters running low-value or low-utilisation workloads, that is a direct argument for consolidation.

What would the ops cost per cluster look like if cluster count were reduced by a quarter or a third? We will explore that in Workshop 5."

---

## Slide 16: Unit Economics Summary

**Layout:** Title at top, summary table populated from session results

### Content

```
Metric                              Baseline value    Confidence

[METRIC 1]                          [VALUE]           H / M / L
[METRIC 2]                          [VALUE]           H / M / L
[METRIC 3]                          [VALUE]           H / M / L
[METRIC 4]                          [VALUE]           H / M / L
[METRIC 5]                          [VALUE]           H / M / L

Key findings:
[POPULATE IN SESSION]
```

### Speaker Notes

"Here is the unit economics picture, the numbers that will anchor the leadership conversation.

Before we move to the showback view, I want to note any findings that have emerged. What surprised the group? What is the most important number in this table and why?"

Populate the key findings field in real time from the discussion.

---

## Slide 17: Showback View

**Layout:** Title at top, table structure with teams or namespaces as rows and cost breakdown as columns, to be populated live

### Content

```
Making costs visible — not billing anyone.

Team / namespace     Compute    Tooling    Ops effort    Total    % of total

[TEAM / NS]
[TEAM / NS]
[TEAM / NS]
[TEAM / NS]
Shared / unallocated
Total
```

### Speaker Notes

"Now that we have unit metrics and allocation rules in place, let us build a first-pass showback view — a report that shows what each team or product is spending on the platform.

This is showback, not chargeback. We are making costs visible, not billing anyone. The value is that it creates accountability and surfaces conversations that would otherwise not happen.

If the namespace or team mapping is incomplete, we use a proxy structure and note the confidence rating."

Populate the table live. Handle any surprises carefully, frame them as findings worth understanding, not things to assign blame for.

---

## Slide 18: What We Have Agreed Today

**Layout:** Title at top, clean summary checklist

### Content

```
Allocation rules agreed — documented in the Assumptions Register

Unit economics model populated — baseline values confirmed

Showback view built — first pass complete

Assumptions Register updated

Workshop 4 confirmed — [DATE] | [TIME]
```

### Speaker Notes

"Here is where we have landed."

Read through the list and confirm each item is genuinely agreed.

Then ask the final question:

"Looking at these unit metrics, does anything surprise you?
And is there anything that looks wrong before we go further?"

If something looks wrong, address it now. The unit economics model is what Workshop 5 builds on; it needs to be trusted.

---

## Slide 19: See You in Workshop 4

**Layout:** Clean closing slide — next session details centred,
plenty of white space

### Content

```
Workshop 4 — Value and Risk Scorecard

[DATE] | [TIME] | [LOCATION / LINK]

Pre-read coming your way before the session.

Workshop 4 looks at the other side of the equation, what value the platform is actually delivering.
```

### Speaker Notes

"Thanks for the work today. Workshop 4 is where we look at the other side of the equation, not just what the platform costs, but what it enables.

We will build a value and risk scorecard using DORA and SPACE as reference points, so cost is not the only lens leadership is looking through.

You will get a short pre-read before the session."

Close the session cleanly.
