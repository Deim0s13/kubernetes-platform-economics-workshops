# Workshop 5 — Slides
## Scenarios, Recommendation, and 90-Day Plan

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

Workshop 5 — Scenarios, Recommendation, and 90-Day Plan

[DATE] | [FACILITATOR]
```

### Speaker Notes

Open with the slide visible. This is the final session — acknowledge that
briefly before moving into the recap. Do not linger on the title slide.

---

## Slide 2: Where We Are

**Layout:** Title at top, horizontal progress indicator with Workshop 5
highlighted

### Content

```
Workshop 0    Workshop 1    Workshop 2    Workshop 3    Workshop 4    Workshop 5
Setup         Scope and     Cost          Unit          Value and     Scenarios
              Rules         Baseline      Economics     Risk          and Plan

                                                                      [YOU ARE HERE]
```

### Speaker Notes

"This is the final session. Over the last four workshops we have built
a cost baseline, unit economics, a showback view, and a value and risk
scorecard.

Today we use all of that to evaluate scenarios, agree a recommendation,
and build a 90-day plan. By the end of this session we will have
everything we need to produce a decision brief for leadership, Finance,
and Procurement."

---

## Slide 3: What We Are Producing Today

**Layout:** Title at top, clean list of five outputs

### Content

```
By the end of this session we will have:

A workload placement matrix — which workloads belong where and why

A scenario comparison — four options evaluated on cost, value,
risk, and time to value

A recommendation — evidence-based, with trade-offs clearly stated

A 90-day plan — no-regrets actions, decisions required, and pilots

A decision brief outline — ready to populate for the exec audience
```

### Speaker Notes

"Today is where the work becomes a decision.

Everything we have built is in service of this session — and of the
decision brief that goes to your leadership team, Finance, and
Procurement afterwards.

Let us start by reviewing the full picture from the previous workshops
to make sure we are all working from the same foundation."

---

## Slide 4: The Full Picture — A Quick Review

**Layout:** Title at top, four summary boxes — one per workshop output

### Content

```
Cost baseline                       Unit economics
What the estate costs today         Cost per useful outcome
across six buckets                  [KEY METRIC] = [VALUE]
Total: [AMOUNT]                     [KEY METRIC] = [VALUE]

Showback view                       Value scorecard
Cost by team or namespace           [NUMBER] measures across
[TOP TEAM] = [AMOUNT]               delivery, reliability,
[NEXT TEAM] = [AMOUNT]              security, and developer
                                    experience
```

### Speaker Notes

"Before we build scenarios, I want to make sure the full picture
feels accurate.

Populate these four boxes with the headline numbers from Workshops
1 through 4 before the session. Present them briefly — one sentence
per box.

Then ask: 'Does this picture feel accurate? Is there anything that
looks wrong or has changed since we last met?'

If something material has changed, address it now. Do not build
scenarios on stale inputs."

---

## Slide 5: How We Compare Scenarios

**Layout:** Title at top, four dimensions with plain explanations

### Content

```
For each scenario we assess four dimensions:

Cost impact
Hard savings, cost avoidance, capacity release, toil reduction

Value and risk impact
Against the scorecard — delivery, reliability, security, developer
experience

Time to value
Realistic estimate — not best case

Dependencies and constraints
What needs to be true for this scenario to work
```

### Speaker Notes

"We are going to evaluate four scenarios. Before we get into them
I want to confirm how we are comparing them.

Four dimensions — cost, value and risk, time to value, and
dependencies. This is what stops the scenario comparison from
becoming a cost-only conversation.

And a note on cost impact — we distinguish between four types:
hard savings are actual spend reduction. Cost avoidance is future
growth that does not happen. Capacity release is using what you
already pay for more efficiently. Toil reduction is operational
time returned to higher-value work. Those are different things
and leadership needs to see them separately."

---

## Slide 6: Workload Placement Matrix — The Criteria

**Layout:** Title at top, six criteria as clear headings with
a one-line question each

### Content

```
Before we compare scenarios, we need to know where each
workload actually belongs.

Six criteria — scored High, Medium, or Low per workload:

Compliance and policy intensity
How much policy enforcement and audit evidence does this workload need?

Cloud-native coupling
How tightly is this workload coupled to provider-specific services?

Operational burden
How much day-two effort does this workload generate?

Portability need
Does this workload need to move between platforms or clouds?

Migration complexity
How difficult and risky would moving this workload be?

Data gravity and latency
Are there performance or data residency constraints pinning this workload?
```

### Speaker Notes

"Before we get into the scenario comparison, we are going to build
a workload placement matrix — a structured view of which workloads
belong on which platform and why.

This is important because without it, the scenario comparison becomes
a platform debate. With it, the conversation is grounded in workload
characteristics rather than preference.

We are going to take ten to twenty meaningful workloads and score
them against these six criteria. The output tells us which workloads
are consolidation candidates, which have genuine constraints, and
which should be considered for managed Kubernetes."

---

## Slide 7: Workload Placement Matrix

**Layout:** Title at top, table with workloads as rows and six
criteria as columns — to be scored live

### Content

```
Workload    Compliance    Cloud       Ops        Portability    Migration    Data
            intensity     coupling    burden     need           complexity   gravity

[WL 1]
[WL 2]
[WL 3]
[WL 4]
[WL 5]
[WL 6]
[WL 7]
[WL 8]
[WL 9]
[WL 10]

Score: H = High   M = Medium   L = Low
```

### Speaker Notes

"Let us work through the workloads now. Two to three minutes per
workload maximum — the pattern across workloads matters more than
the precision of any single score.

After scoring, look for three groups:
- Consolidation candidates — low coupling, high burden, high compliance,
low migration complexity
- Justified exceptions — high coupling, hard constraints, high complexity
- Managed platform candidates — high burden, low coupling

If a workload scores ambiguously, note it as a spike candidate rather
than forcing a placement decision."

Work through the matrix live. Keep pace steady.

---

## Slide 8: Placement Matrix — What It Tells Us

**Layout:** Title at top, three categories populated from matrix results

### Content

```
Consolidation candidates:
[WORKLOADS — POPULATE FROM MATRIX]

Justified exceptions — with documented reasons:
[WORKLOADS — POPULATE FROM MATRIX]

Managed platform candidates:
[WORKLOADS — POPULATE FROM MATRIX]

Spike candidates — needs further investigation:
[WORKLOADS — POPULATE FROM MATRIX]
```

### Speaker Notes

"Here is what the placement matrix is telling us.

Populate this slide live from the matrix results. This is the
diagnostic output that feeds directly into the scenario comparison.

Before moving on, check: 'Does this grouping feel right? Are there
any surprises — workloads you expected to land differently?'"

---

## Slide 9: Scenario A — Optimise the Current Estate

**Layout:** Title at top, four sections — what changes, cost impact,
value and risk impact, and time to value / risk

### Content

```
What changes:
Utilisation improvement, cluster sprawl reduction, resource
rightsizing, autoscaling, tooling consolidation where duplication
exists. No structural change to the platform estate.

Cost impact:
Hard savings:        [POPULATE]
Cost avoidance:      [POPULATE]
Capacity release:    [POPULATE]
Toil reduction:      [POPULATE]

Value and risk impact:
[POPULATE FROM SCORECARD — which measures improve?]

Time to value:   4 to 12 weeks (optimisations) / 1 to 2 quarters (consolidation)
Risk:            Low — no structural change, benefits are incremental
```

### Speaker Notes

"Scenario A is the baseline. It shows what is achievable without
structural change — and it sets the floor for how other scenarios
need to perform to justify their additional complexity.

Every other scenario needs to outperform Scenario A on at least
one dimension to be worth its complexity.

Populate the cost impact fields using the utilisation gap from
Workshop 3, the cluster ops cost, and the tooling duplication cost
from Workshop 2."

---

## Slide 10: Scenario B — Consolidate Workloads Across Platforms

**Layout:** Title at top, four sections — what changes, cost impact,
value and risk impact, and time to value / risk

### Content

```
What changes:
Consolidation candidates from the placement matrix migrate to a
preferred platform. Tooling, policy, and operational duplication
is reduced. The estate becomes more intentional.

Cost impact:
Hard savings:        [POPULATE]
Cost avoidance:      [POPULATE]
Capacity release:    [POPULATE]
Toil reduction:      [POPULATE]

Value and risk impact:
[POPULATE FROM SCORECARD — which measures improve or worsen?]

Time to value:   1 to 2 quarters (tooling) / 2 to 4 quarters (migration)
Risk:            Medium — migration introduces short-term risk
```

### Speaker Notes

"Scenario B is the consolidation option. It addresses the duplication
cost that is often the most significant hidden cost in a multi-platform
estate.

The cost case includes: tooling duplication cost eliminated, reduction
in ops cost per cluster as cluster count falls, and reduction in the
overhead of maintaining multiple sets of standards and runbooks.

Populate cost impact using the tooling duplication cost from Workshop
2 and the ops cost per cluster from Workshop 3."

---

## Slide 11: Scenario C — Move to Managed Kubernetes

**Layout:** Title at top, four sections — what changes, cost impact,
value and risk impact, and time to value / risk

### Content

```
What changes:
Selected clusters or workloads move to a managed Kubernetes offering.
Control plane management, upgrades, and infrastructure reliability
shift to the managed service. Platform team capacity is redirected.

Cost impact:
Hard savings:        [POPULATE]
Cost avoidance:      [POPULATE]
Capacity release:    [POPULATE]
Toil reduction:      [POPULATE — ops effort for upgrades and patching]

Value and risk impact:
[POPULATE FROM SCORECARD — reliability, security, ops burden]

Time to value:   1 quarter (pilot) / 2 to 4 quarters (broader migration)
Risk:            Low to Medium — mature offering, risk in migration period
```

### Speaker Notes

"Scenario C is the managed Kubernetes option. The infrastructure
cost may be similar or slightly higher — but the reduction in operating
effort can more than offset it.

The cost case is primarily in toil reduction — particularly upgrade
and patching cycles, which can consume a disproportionate amount of
platform team time.

Model the net impact honestly: managed infrastructure cost versus
reduced operating effort. Use the operating effort breakdown from
Workshop 2 as the basis for the toil reduction estimate."

---

## Slide 12: Scenario D — Hybrid Portfolio

**Layout:** Title at top, four sections — what changes, cost impact,
value and risk impact, and time to value / risk

### Content

```
What changes:
The estate is structured deliberately. Justified exceptions stay
where they are with documented reasons. Consolidation candidates
migrate. The estate is intentional — not sprawling.

Cost impact:
Hard savings:        [POPULATE]
Cost avoidance:      [POPULATE]
Capacity release:    [POPULATE]
Toil reduction:      [POPULATE]

Value and risk impact:
[POPULATE FROM SCORECARD]

Time to value:   1 quarter (governance model) / 2 to 4 quarters (consolidation)
Risk:            Medium — governance overhead required to prevent drift
```

### Speaker Notes

"Scenario D is the hybrid portfolio option — often the most realistic
outcome, and the one most organisations end up with when they are
deliberate about it.

The difference between a managed hybrid and unmanaged sprawl is
governance. Without clear placement rules and documented exceptions,
a hybrid model tends to expand rather than contract over time.

The cost case is similar to Scenario B for the consolidated workloads,
minus the switching cost for the justified exceptions."

---

## Slide 13: Scenario Comparison

**Layout:** Title at top, comparison table with all four scenarios
across the four dimensions — populated live

### Content

```
                    Scenario A      Scenario B      Scenario C      Scenario D
                    Optimise        Consolidate     Managed K8s     Hybrid

Cost impact         [POPULATE]      [POPULATE]      [POPULATE]      [POPULATE]

Value and risk      [POPULATE]      [POPULATE]      [POPULATE]      [POPULATE]

Time to value       4-12 weeks      1-4 quarters    1-4 quarters    1-4 quarters

Risk                Low             Medium          Low-Medium      Medium

Key dependency      Governance      Placement       Landing zone    Placement
                                    rules           readiness       rules + gov
```

### Speaker Notes

"Here are all four scenarios side by side. This is the view that
produces the recommendation.

Take a moment to look at it as a whole. Where do cost and value
point in the same direction? Where are there genuine trade-offs?

Before we discuss the recommendation, I want to ask three questions:
Which scenarios does the evidence most clearly support? Which have
dependencies or risks that make them less viable near-term? And is
there a combination that performs better than any single scenario alone?"

Let the group respond before moving to the recommendation slide.

---

## Slide 14: The Recommendation

**Layout:** Title at top, four clearly labelled sections

### Content

```
Recommended path:
[POPULATE IN SESSION]

Why this path:
[POPULATE IN SESSION]

Trade-offs we are accepting:
[POPULATE IN SESSION]

What would change this recommendation:
[POPULATE IN SESSION — key assumptions it depends on]
```

### Speaker Notes

"A recommendation is not 'the only right answer.' It is the path
that best fits the evidence, the constraints, and the organisation's
risk appetite — with the trade-offs clearly stated.

Populate this slide live from the discussion. Make sure the rationale
is grounded in the evidence — not in preference or familiarity.

If there is genuine disagreement in the room, note both positions.
A recommendation does not need to be unanimous — it needs to be
reasoned."

---

## Slide 15: 90-Day Plan — Track 1 — No-Regrets Actions

**Layout:** Title at top, table with action, owner, timeframe, and
expected outcome columns — to be populated live

### Content

```
Start these now — they improve the situation regardless of
which scenario is chosen.

Action                          Owner    Timeframe    Expected outcome

[ACTION]
[ACTION]
[ACTION]
[ACTION]
[ACTION]
```

### Speaker Notes

"No-regrets actions are things that make sense to do regardless of
the broader scenario direction. They start immediately and do not
require additional leadership sign-off beyond approval of the plan.

Common no-regrets actions include: rightsizing, enforcing resource
requests and limits, retiring or merging clearly redundant clusters,
improving tagging for better cost allocation, and tooling consolidation
where duplication is obvious.

Every action needs an owner. Do not leave this slide without a
name against every item."

---

## Slide 16: 90-Day Plan — Track 2 — Decisions Required

**Layout:** Title at top, table with decision, who decides, by when,
and options columns — to be populated live

### Content

```
Leadership needs to make these decisions before the preferred
scenario can be fully committed to.

Decision                        Who decides    By when    Options

[DECISION]
[DECISION]
[DECISION]
```

### Speaker Notes

"These are the questions that cannot be answered in this room —
they need to go to leadership.

Be explicit about what the options are and what is at stake. Leadership
cannot make a good decision without understanding what they are deciding.

Surface these clearly in the decision brief — not buried in the
appendix."

---

## Slide 17: 90-Day Plan — Track 3 — Pilots and Spikes

**Layout:** Title at top, table with pilot or spike, scope, success
criteria, timeframe, and owner columns — to be populated live

### Content

```
Time-boxed investigations to validate key assumptions before
committing to structural change.

Pilot or spike       Scope    Success criteria    Timeframe    Owner

[PILOT / SPIKE]
[PILOT / SPIKE]
[PILOT / SPIKE]
```

### Speaker Notes

"Pilots and spikes are how we reduce the risk of structural decisions.

A managed Kubernetes viability spike, for example, might involve
standing up a landing zone and migrating one or two candidate workloads
to validate the operational model, the cost, and the migration approach
before committing to a broader programme.

For each pilot or spike agree: what we are testing, what success looks
like, how long it should take, and who owns it."

---

## Slide 18: Decision Brief — What Goes to Leadership

**Layout:** Title at top, structured list of decision brief sections

### Content

```
The decision brief covers:

Executive summary       What we assessed, key findings, recommended path

Methodology             Frameworks used, confidence levels, assumptions

Cost baseline           TBM-aligned baseline, fixed vs variable, key drivers

Unit economics          Three to five metrics with baselines and meaning

Value scorecard         Eight to twelve measures with baselines and targets

Scenario comparison     Four scenarios on cost, value, risk, time to value

Recommendation          Recommended path, rationale, trade-offs

90-day plan             No-regrets actions, decisions required, pilots

Appendix                Assumptions register, data sources, sensitivity notes

Audience: [CIO] | [GM TECH AND OPS] | [FINANCE] | [PROCUREMENT]
Draft by: [DATE]
```

### Speaker Notes

"This is the structure of the decision brief that will go to your
leadership team.

It is written for people who were not in these workshops — who need
to understand the methodology, trust the numbers, and make a decision.

I will produce a draft by [DATE] and share it for your review before
it goes to the exec audience. Please flag anything that does not
accurately represent what was agreed in the workshops."

---

## Slide 19: What We Have Built

**Layout:** Title at top, journey summary — one line per workshop

### Content

```
Workshop 1    Scope, rules, and assumptions locked

Workshop 2    Cost baseline built — six buckets, trusted sources

Workshop 3    Unit economics — cost per useful outcome

Workshop 4    Value scorecard — what the platform enables and protects

Workshop 5    Scenarios, recommendation, and 90-day plan

The decision brief brings it all together for leadership,
Finance, and Procurement.
```

### Speaker Notes

"That is the journey we have been on.

We came in with a commercial question and a cost concern. We are
leaving with a trusted fact base, a balanced view of cost and value,
a set of realistic options, and a plan.

Thank you for the time and the honesty throughout this process."

Pause. Let that land.

---

## Slide 20: Next Steps

**Layout:** Clean closing slide — three clear next steps

### Content

```
Decision brief draft            [FACILITATOR] → by [DATE]

Brief review session            [PLATFORM TEAM + PO] → by [DATE]

Leadership presentation         [DATE / TBC]

90-day plan actions start       Immediately
```

### Speaker Notes

"Three things happen from here.

I will have a draft of the decision brief to you by [DATE]. We will
review it together before it goes to leadership. And the 90-day plan
actions start now — do not wait for the brief to be finalised before
beginning the no-regrets work.

Thank you."

Close the session. This is the end of the workshop series — keep the
close warm, brief, and forward-looking.
