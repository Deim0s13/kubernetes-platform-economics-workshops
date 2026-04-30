# Workshop 2 — Slides
## Cost Taxonomy and Baseline Model

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

Each slide is written with a title, layout note, content, and speaker notes.
Build your presentation deck from this file. This file is the source of truth
— if you update the deck, update this file to match and bump the version number.

Speaker notes are written in your voice — conversational and plain. They are
not a script to read verbatim but a guide for what to cover and how to frame it.

---

## Slide 1: Title

**Layout:** Title slide — centred title, subtitle, and session details below

### Content

```
Kubernetes Platform Economics

Workshop 2 — Cost Taxonomy and Baseline Model

[DATE] | [FACILITATOR]
```

### Speaker Notes

Open with the slide visible and move straight into the recap of Workshop 1.
Do not linger here.

---

## Slide 2: Where We Are

**Layout:** Title at top, horizontal progress indicator with Workshop 2 highlighted

### Content

```
Workshop 0    Workshop 1    Workshop 2    Workshop 3    Workshop 4    Workshop 5
Setup         Scope and     Cost          Unit          Value and     Scenarios
              Rules         Baseline      Economics     Risk          and Plan

                            [YOU ARE HERE]
```

### Speaker Notes

"In Workshop 1 we locked in scope, agreed cost treatment rules, and
built the data request list.

Today we start building the cost model. We are going to agree a cost
taxonomy and map known spend into it. By the end of this session we
will have a baseline skeleton ready to populate as remaining data comes in."

---

## Slide 3: What We Are Producing Today

**Layout:** Title at top, clean list of five outputs

### Content

```
By the end of this session we will have:

A cost taxonomy — agreed and understood by the room

A baseline model skeleton — known spend mapped in

A fixed versus variable cost split — first pass

A clear view of gaps — with owners and dates

An initial picture of where spend concentrates
```

### Speaker Notes

"We will not have a complete model today. That is fine and expected.

What we need is the right structure and a clear view of what we know,
what we are estimating, and what we still need. The model will continue
to populate as the remaining data comes in."

---

## Slide 4: Why Structure Matters

**Layout:** Title at top, two contrasting columns

### Content

```
Without a taxonomy                  With a taxonomy

Costs scattered across              Every cost has a home
invoices, cloud bills,              and a source
and people's heads

IT and Finance disagree             IT and Finance work
on what the numbers mean            from the same structure

Output is contested                 Output is auditable
and argued over                     and trusted
```

### Speaker Notes

"Platform cost without structure is just a collection of numbers.
With the right structure it becomes a model Finance can audit,
leadership can act on, and your team can use to make better decisions.

That is what the taxonomy gives us."

---

## Slide 5: The Cost Taxonomy — Six Buckets

**Layout:** Title at top, six clearly labelled buckets with a one-line
description each

### Content

```
1   Cloud infrastructure
    Compute, storage, and network costs

2   Managed service fees
    Cloud provider charges for managed Kubernetes services

3   Platform tooling
    Observability, security, CI/CD, backup, and DR

4   Subscriptions
    Platform licences and support agreements

5   Operating effort
    Platform team time — the largest hidden cost

6   Shared services
    IAM, shared network, shared logging
```

### Speaker Notes

"There are six buckets. Every cost in scope sits in one of these.

We are using a TBM-aligned taxonomy — Technology Business Management
is an industry standard for classifying technology costs. Finance will
recognise this structure. That is the point.

Let me walk you through each one before we start mapping spend."

---

## Slide 6: Bucket 1 — Cloud Infrastructure

**Layout:** Title at top, three sub-categories with examples beneath each

### Content

```
Compute
Virtual machines, node pools, reserved instances, spot usage

Storage
Block storage, object storage, persistent volumes

Network
Load balancers, NAT gateways, data egress, peering

What to look for:
- Idle or oversized node pools
- Egress costs suggesting inefficient data movement
- Load balancer proliferation
```

### Speaker Notes

"Cloud infrastructure is typically the biggest bucket — and the most
visible on a cloud bill.

A few things worth looking for as we map this: idle or oversized node
pools, egress costs that suggest inefficient data movement, and load
balancer proliferation — one load balancer per service is a common
and expensive anti-pattern."

---

## Slide 7: Bucket 2 — Managed Service Fees

**Layout:** Title at top, explanation and examples

### Content

```
Fees charged by cloud providers for managed Kubernetes services.
These are separate from the compute cost of running the nodes.

Examples:
- EKS cluster management fees
- AKS management fees
- Equivalent managed control plane charges

What to look for:
- How many clusters are incurring management fees?
- Are any low-utilisation or candidates for retirement?
```

### Speaker Notes

"Managed service fees are easy to miss because they sit separately
from the compute line on a cloud bill. But across a large estate they
add up — particularly if cluster counts are higher than they need to be.

This is one of the places where cluster sprawl becomes visible as a
cost driver."

---

## Slide 8: Bucket 3 — Platform Tooling

**Layout:** Title at top, categories with examples and a note on duplication

### Content

```
Everything that makes the platforms operable —
above and beyond raw infrastructure.

Observability       Monitoring, logging, alerting, dashboards
Security            Scanning, policy enforcement, secrets management
CI/CD               Pipeline tooling, artefact management
Backup and DR       Backup services, disaster recovery tooling

What to look for:
- The same capability running separately across multiple platforms
- SaaS tooling costs that do not appear on the cloud bill
- Tooling that was set up and never reviewed for value
```

### Speaker Notes

"Platform tooling is often where the most interesting findings sit —
particularly if the same capability exists across multiple platforms.

Separate observability stacks, separate security tooling, separate
CI/CD pipelines — each is a real cost in money, in people time, and
in cognitive overhead. We will look explicitly for duplication here."

---

## Slide 9: Bucket 4 — Subscriptions

**Layout:** Title at top, explanation and examples

### Content

```
Platform licences, support agreements, and recurring software fees.
Typically fixed costs — do not change with usage in the short term.

What to look for:
- Subscriptions that predate current platform usage patterns
- Support tiers that may be higher than current needs
- Licences covering more capacity than is being used
- Renewal dates that are approaching
```

### Speaker Notes

"Subscriptions are straightforward to identify but often not reviewed
regularly. A licence that made sense two years ago may no longer reflect
how the platform is actually being used.

Renewal dates are worth capturing here — they become relevant in
Workshop 5 when we look at scenarios and timing."

---

## Slide 10: Bucket 5 — Operating Effort

**Layout:** Title at top, explanation, examples, and note on how
we capture it

### Content

```
The time your platform team spends running, maintaining,
and improving the platforms.

Often the largest hidden cost —
and the one most commonly left out of cost reviews.

Examples:
- Upgrade and patching cycles
- Incident response and on-call
- Onboarding new teams and workloads
- Building and maintaining golden paths and standards

How we capture it:
A rough time split across activities is enough.
We do not need timesheets — we need a reasonable estimate.
```

### Speaker Notes

"This is the bucket that gets the most pushback — because it is an
estimate rather than a number on an invoice.

But if we leave it out, we are missing a significant part of the true
cost picture. A platform that looks cheap on the cloud bill can be
very expensive when you factor in the team time it consumes.

A rough percentage split is all we need — we will rate it Low or
Medium confidence and note the assumptions."

---

## Slide 11: Bucket 6 — Shared Services

**Layout:** Title at top, explanation and examples

### Content

```
Costs that sit beneath the platforms and serve them —
without being attributable to one platform alone.

Examples:
- Identity and access management (IAM)
- Shared network infrastructure
- Shared logging or audit platforms
- Centralised certificate management

Note:
Often the least complete bucket in the first pass.
Capture what we can — note gaps and move on.
```

### Speaker Notes

"Shared services are often the hardest to attribute because they serve
everything — not just the Kubernetes estate.

We will capture what we can, note what we cannot attribute, and flag
it in the Assumptions Register. A partial view is better than no view."

---

## Slide 12: Mapping Spend — How We Work Through It

**Layout:** Title at top, simple four-step process

### Content

```
For each cost bucket we will:

1   Ask what spend is known and what its source is

2   Enter the amount with a confidence rating
    H = measured   M = estimated   L = rough guess

3   Note any gaps or questions

4   Move on — we do not get stuck on any single line item

The goal is a populated skeleton — not a finished model.
```

### Speaker Notes

"We are going to work through the six buckets now.

The key thing is pace — roughly six to seven minutes per bucket on
average. Cloud infrastructure will take longer. Shared services will
probably be shorter.

If something surprises us — a number that looks too high or a gap
that is bigger than expected — we note it and move on. The finding
is the finding. Analysis comes later.

Let us start with cloud infrastructure."

---

## Slide 13: Fixed Versus Variable Costs

**Layout:** Title at top, two columns with definitions and examples,
decision prompt below

### Content

```
Fixed costs                         Variable costs

Do not change with usage            Scale with usage
in the short term                   as demand changes

Require a structural decision       Require an operational decision
to change                           to change

Examples:                           Examples:
- Subscriptions                     - Compute consumption
- Support agreements                - Storage usage
- Licence fees                      - Data egress

Which lever is available — and how quickly can you pull it?
```

### Speaker Notes

"Now that we have spend mapped in, I want to work through a simple
but important distinction.

Fixed costs require structural decisions — renegotiating a contract,
consolidating platforms, changing model. Those take time and planning.

Variable costs respond to operational decisions — rightsizing,
autoscaling, better utilisation. Those can often be pulled more quickly.

Understanding the split tells us which levers are available and helps
us build realistic scenarios in Workshop 5."

Work through the taxonomy and tag each line item. Where something is
genuinely mixed, note it as partially fixed and partially variable.

---

## Slide 14: Data Gaps Review

**Layout:** Title at top, table with gap, approach, owner, and date
columns — to be populated live

### Content

```
For each gap we agree one of three approaches:

Estimate    Use a reasonable estimate with a Low confidence rating

Wait        Data is coming — confirm a firm date

Exclude     Genuinely not available — note the impact on confidence

Gap         Approach    Owner    Date
[ITEM]
[ITEM]
[ITEM]
```

### Speaker Notes

"Let us look at what we still need.

For each gap I want to agree one of those three things and confirm
who owns it and by when.

Be direct about gaps that are blocking the model. If we can agree an
estimate now for something the owner is uncertain about, that is
usually better than waiting."

Update the Assumptions Register with every gap decision.

---

## Slide 15: What the Baseline Is Telling Us

**Layout:** Title at top, three summary points populated live
from session findings

### Content

```
Where spend concentrates:
[POPULATE IN SESSION]

Fixed versus variable split:
[POPULATE IN SESSION]

Key gaps still to close:
[POPULATE IN SESSION]
```

### Speaker Notes

"Before we close I want to summarise what the baseline is already
telling us — even at this early stage.

Populate this slide live from what has emerged in the session. Even
a partial picture is useful — it gives the group a sense of progress
and signals that the model is already producing insight."

---

## Slide 16: What We Have Agreed Today

**Layout:** Title at top, clean summary checklist

### Content

```
Cost taxonomy agreed — six buckets, understood by the room

Baseline skeleton populated — known spend mapped in

Fixed versus variable split — first pass complete

Data gaps list updated — approach, owner, and date confirmed

Assumptions Register updated

Workshop 3 confirmed — [DATE] | [TIME]
```

### Speaker Notes

"Here is where we have landed."

Read through the list and confirm each item is genuinely agreed.
If anything is still open, name it and confirm who is closing it and when.

Then ask the final question:

"Is there anything in what we have built today that concerns you —
or anything that looks wrong before we go further?"

If something looks wrong, address it now. A flawed baseline that
goes unchallenged here will cause bigger problems in Workshop 5.

---

## Slide 17: See You in Workshop 3

**Layout:** Clean closing slide — next session details centred,
plenty of white space

### Content

```
Workshop 3 — Allocation Rules and Unit Economics

[DATE] | [TIME] | [LOCATION / LINK]

Pre-read coming your way before the session.

Please action any outstanding data items —
the model updates as data comes in.
```

### Speaker Notes

"Thanks for the work today. Workshop 3 is where we move from total
cost to unit economics — cost per app, cost per tenant, cost per
environment. That is the number that will land with leadership and Finance.

You will get a short pre-read before the session. And please action
any outstanding data items — the model will be updated and shared
before Workshop 3 as new data comes in."

Close the session cleanly.
