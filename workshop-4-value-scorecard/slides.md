# Workshop 4 — Slides
## Value and Risk Scorecard

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

Workshop 4 — Value and Risk Scorecard

[DATE] | [FACILITATOR]
```

### Speaker Notes

Open with the slide visible and move straight into the recap of Workshop 3.
Do not linger here.

---

## Slide 2: Where We Are

**Layout:** Title at top, horizontal progress indicator with Workshop 4
highlighted

### Content

```
Workshop 0    Workshop 1    Workshop 2    Workshop 3    Workshop 4    Workshop 5
Setup         Scope and     Cost          Unit          Value and     Scenarios
              Rules         Baseline      Economics     Risk          and Plan

                                                        [YOU ARE HERE]
```

### Speaker Notes

"We have spent three workshops building a clear picture of what the
platform costs and what it costs per useful outcome.

Today is different. Today we look at what the platform enables — and
what we would risk if cost decisions were made without considering that.

By the end of this session we will have a value and risk scorecard that
sits alongside the unit economics model. Together they give leadership
a balanced view."

---

## Slide 3: What We Are Producing Today

**Layout:** Title at top, clean list of five outputs

### Content

```
By the end of this session we will have:

A value and risk scorecard — eight to twelve agreed measures

Baseline values — real data where available, proxies where not

Target directions — where each measure should move and why

A narrative — what the platform enables and what it protects

A foundation for balanced scenario evaluation in Workshop 5
```

### Speaker Notes

"Today completes the picture. The cost model tells us what the
platform costs. The scorecard tells us what it delivers and what
it guards against.

Without both, Workshop 5 becomes a cost-only conversation — and
that tends to produce decisions that reduce spend but shift cost
somewhere less visible."

---

## Slide 4: Cost Without Value Is an Incomplete Picture

**Layout:** Title at top, two contrasting scenarios

### Content

```
Platform that looks expensive           Platform that looks cheap

May be delivering significant           May be hiding cost in:
returns in:                             - Incidents and outages
- Delivery speed                        - Audit failures
- Reliability                           - Developer friction
- Security posture                      - Manual compliance work
- Developer productivity

Optimising cost without value           Shifts cost somewhere
reduces spend in one place              less visible
```

### Speaker Notes

"When leadership only sees cost, they optimise in one dimension.

A platform that looks expensive on the cost model may be delivering
significant returns that more than justify the spend. And a platform
that looks cheap may be hiding significant cost in incidents, audit
failures, and the friction that slows developers down.

The scorecard exists to make that full picture visible — so decisions
in Workshop 5 are made on evidence, not just on the cost number."

---

## Slide 5: The Frameworks We Use

**Layout:** Title at top, two frameworks side by side with plain
English descriptions

### Content

```
DORA                                SPACE
DevOps Research and Assessment      Developer Productivity

Four metrics for software           Five dimensions for thinking
delivery performance:               about developer productivity:

Deployment frequency                Satisfaction and wellbeing
Lead time for changes               Performance
Change failure rate                 Activity
Time to restore service             Communication and collaboration
                                    Efficiency and flow

Industry standard.                  Industry standard.
Not vendor-specific.                Not vendor-specific.
```

### Speaker Notes

"We are using two industry-standard frameworks for the scorecard —
neither of them is a vendor construct.

DORA gives us four well-understood metrics for delivery performance
and reliability. SPACE gives us a framework for thinking about
developer experience beyond just counting outputs.

You do not need to know these frameworks in depth. The pre-read
covers them. What matters is that Finance and Procurement will
recognise them as credible, independent references."

---

## Slide 6: The Four Scorecard Categories

**Layout:** Title at top, four categories as clear headings with
a one-line description each

### Content

```
Delivery performance
How effectively the platform enables teams to ship changes
safely and quickly

Reliability
How stable the platform is and how quickly it recovers
when things go wrong

Security and compliance effort
How much effort the platform requires — and reduces — for
security and compliance obligations

Developer experience
How much friction developers experience when building
and deploying on the platform
```

### Speaker Notes

"We organise the scorecard into four categories. Together they give
a complete picture of platform value — not just delivery speed, but
reliability, security posture, and the day-to-day experience of
the people using the platform.

We will build each category in turn. For each measure we will agree
a data source or a proxy if direct measurement is not available.
A rough number with a Low confidence rating is more useful than
no number at all."

---

## Slide 7: A Note on Proxies

**Layout:** Title at top, explanation and example table

### Content

```
Not every organisation tracks DORA metrics formally.
That is fine.

For each measure we will agree a proxy if direct measurement
is not available.

Measure                  Direct             Proxy if not tracked
Deployment frequency     Tracked in CI/CD   Release cadence per month
Lead time                Tracked in Git     Estimated by platform team
MTTR                     Tracked in ops     Average duration from on-call logs
Onboarding time          Not tracked        Estimated from recent examples

A proxy with Low confidence is better than no baseline at all.
```

### Speaker Notes

"Before we start building the scorecard I want to address the
question that is probably in some people's minds — 'we do not
track most of these.'

That is completely fine. For each measure we will agree a proxy —
an imperfect but directionally useful substitute. The goal is not
precision. It is direction. We want to know whether things are
getting better or worse — and whether platform decisions are
helping or hurting."

---

## Slide 8: Category 1 — Delivery Performance

**Layout:** Title at top, three measures with data source and
baseline fields to be populated live

### Content

```
How effectively does the platform enable teams to ship
changes safely and quickly?

Measure              Data source / proxy    Baseline    Confidence

Deployment
frequency

Lead time for
changes

Change failure
rate
```

### Speaker Notes

"Let us start with delivery performance — the core DORA delivery
metrics.

Does your organisation track any of these formally? If not, let us
agree a proxy for each one.

What does the current picture tell us? Is the platform accelerating
delivery or constraining it?"

Work through each measure live. Capture data source or proxy,
baseline value, and confidence rating.

If the platform team feels these metrics are outside their control,
address it directly: "The scorecard is measuring what the platform
enables — not the platform team's performance. The distinction matters."

---

## Slide 9: Category 2 — Reliability

**Layout:** Title at top, three measures with data source and
baseline fields to be populated live

### Content

```
How stable is the platform — and how quickly does it recover
when things go wrong?

Measure              Data source / proxy    Baseline    Confidence

Incident volume
(per quarter)

Time to restore
service (MTTR)

Platform
availability
```

### Speaker Notes

"Reliability is the other half of the DORA picture.

Do you have incident data from the last quarter? Even a rough count
and a sense of typical recovery time is enough to start.

Is there a pattern here — are incidents concentrated on specific
platforms or clusters? Are recovery times improving or worsening?"

Work through each measure live. Capture data source or proxy,
baseline value, and confidence rating.

If a recent major incident dominates the conversation, acknowledge
it and move to the broader pattern: "That incident is important
context. For the scorecard we want to capture the broader trend —
not just the outlier."

---

## Slide 10: Category 3 — Security and Compliance Effort

**Layout:** Title at top, three measures with data source and
baseline fields to be populated live

### Content

```
How much effort does the platform require to meet security
and compliance obligations — and how much does it reduce
that effort?

Measure              Data source / proxy    Baseline    Confidence

Time to patch
critical vulnerabilities

Policy coverage
(% of workloads)

Audit evidence
effort (days per cycle)
```

### Speaker Notes

"Security and compliance effort is one of the most underappreciated
platform value measures — because it is invisible when it is working
well and very visible when it is not.

The question we are asking is: how much effort does the platform
require to meet security and compliance obligations? And is that
effort increasing or decreasing?

How would this picture change if the platform were consolidated —
or fragmented across more platforms?"

Work through each measure live. Note any risk signals — low policy
coverage or long patch times are findings that belong in the
decision brief.

---

## Slide 11: Category 4 — Developer Experience

**Layout:** Title at top, three measures with data source and
baseline fields to be populated live

### Content

```
How much friction do developers experience when building
and deploying on the platform?

Measure              Data source / proxy    Baseline    Confidence

Onboarding time
(new service or team)

Time to first
deployment

Ticket and toil
volume per month
```

### Speaker Notes

"Developer experience is where platform value is felt most directly
by the people using it — but it is often the hardest to measure.

What do you know about the current experience? What takes longer than
it should? Where do teams get stuck?

If formal tracking is not in place, an honest estimate from the
platform team is a perfectly valid starting point."

Work through each measure live. If the group starts generating a long
list of pain points, note them but keep the scorecard to three to four
measures per category.

---

## Slide 12: Scorecard Summary

**Layout:** Title at top, summary table with all measures,
baselines, confidence ratings, and target direction columns —
to be populated live

### Content

```
Category                  Measure              Baseline    Confidence    Direction

Delivery performance      Deployment frequency
                          Lead time
                          Change failure rate

Reliability               Incident volume
                          MTTR
                          Availability

Security and compliance   Time to patch
                          Policy coverage
                          Audit effort

Developer experience      Onboarding time
                          Time to first deploy
                          Ticket and toil volume
```

### Speaker Notes

"Here is the scorecard — the full picture of platform value alongside
the cost model.

Before we agree target directions, take a moment to look at it as a
whole. What stands out? What surprises you? Is there anything that
looks wrong?"

Let the group respond before moving to target directions.

---

## Slide 13: Agreeing Target Directions

**Layout:** Title at top, explanation and prompt questions

### Content

```
For each measure — where should it move, and over what timeframe?

We are agreeing directions, not precise targets.

Questions to ask for each measure:

Should this increase, decrease, or stay the same?

What is a realistic improvement over six to twelve months?

What would achieving that improvement be worth —
in cost, in risk reduction, in team capacity?
```

### Speaker Notes

"A scorecard without target directions is just a snapshot. We want
it to be a management tool — something we can use to track progress
and evaluate scenarios.

For each measure, let us agree the direction and a rough sense of
what realistic improvement looks like. We do not need precise numbers.
'Reduce MTTR by roughly 30% over six months' is more useful than a
number that will be argued over.

And where you can, connect the target back to the cost model. If we
reduce onboarding time, what does that free up in platform team
capacity? How does that show up in the unit economics?"

Work through the scorecard and add target directions to the summary
table on the previous slide.

---

## Slide 14: What the Scorecard Tells Us

**Layout:** Title at top, three summary points populated live
from session findings

### Content

```
What the platform is enabling well:
[POPULATE IN SESSION]

Where there is room to improve:
[POPULATE IN SESSION]

What would be at risk if cost were optimised without
considering value:
[POPULATE IN SESSION]
```

### Speaker Notes

"Before we close I want to capture the narrative the scorecard is
telling us — because this is what will land in the final decision
brief.

What is the platform enabling well? Where is there room to improve?
And what would be at risk if cost decisions were made without
considering the scorecard?"

Populate live from the discussion. This slide becomes the value
narrative in the decision brief.

---

## Slide 15: What We Have Agreed Today

**Layout:** Title at top, clean summary checklist

### Content

```
Value and risk scorecard built — [NUMBER] measures agreed

Baselines confirmed — with confidence ratings throughout

Target directions agreed for each measure

Scorecard saved and versioned

Assumptions Register updated

Workshop 5 confirmed — [DATE] | [TIME]
```

### Speaker Notes

"Here is where we have landed."

Read through the list and confirm each item is genuinely agreed.

Then ask the final question:

"Looking at the scorecard — does anything surprise you? And is there
anything that feels wrong or missing before we take this into the
scenario modelling?"

If something is missing, add it now. The scorecard needs to be
trusted before Workshop 5 builds on it.

---

## Slide 16: See You in Workshop 5

**Layout:** Clean closing slide — next session details centred,
plenty of white space

### Content

```
Workshop 5 — Scenarios, Recommendation, and 90-Day Plan

[DATE] | [TIME] | [LOCATION / LINK]

Pre-read coming your way before the session.

Workshop 5 brings everything together — cost model,
unit economics, and value scorecard — and turns it
into a decision and a plan.
```

### Speaker Notes

"Thanks for the work today. Workshop 5 is the final session —
where we bring everything together.

We will model three to five scenarios, compare them on cost and
value, agree a recommended path, and build a 90-day plan that
leadership, Finance, and Procurement can act on.

You will get a short pre-read before the session."

Close the session cleanly.
