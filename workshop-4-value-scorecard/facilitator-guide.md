# Workshop 4 — Facilitator Guide
## Value and Risk Scorecard

**Version:** 1.0
**Duration:** 90 minutes
**Audience:** Product Owner, Platform Lead, Platform Engineers and SREs
**Facilitator:** [FACILITATOR]

---

## Version history

| Version | Date | Changes |
|---------|------|---------|
| 1.0 | [DATE] | Initial version |

---

## Purpose

Workshop 4 completes the picture. The first three workshops built a cost
model. This session adds the value side — what the platform enables, what
it protects, and what would be at risk if cost decisions were made without
considering it.

The output is a value and risk scorecard that sits alongside the unit
economics model. Together they give leadership, Finance, and Procurement
a balanced view — not just what the platform costs, but what it delivers
and what it guards against.

This is also where you protect the integrity of the final output. Without
a value scorecard, Workshop 5 becomes a cost-only conversation. That tends
to produce decisions that reduce spend but shift cost somewhere less
visible — into incidents, audit failures, or developer friction.

By the end of this session you will have:

- A value and risk scorecard — eight to twelve agreed measures
- Baseline values — using real data where available, proxies where not
- Target directions — where each measure should move and why
- A narrative connecting platform cost to platform value
- A foundation for balanced scenario evaluation in Workshop 5

---

## Before the session

### Review what data has come in

Check whether any delivery, reliability, or developer experience data
has been shared since the pre-read went out. Even rough data changes
the quality of the scorecard significantly — a real number with a Low
confidence rating is better than a pure estimate.

### Prepare the scorecard template

Set up a scorecard template in the working model before the session
with tabs or sections for each of the four categories:

- Delivery performance
- Reliability
- Security and compliance effort
- Developer experience

Each measure should have fields for: measure name, definition, data
source or proxy, baseline value, confidence rating, target direction,
and notes.

### Know the DORA and SPACE frameworks well

You do not need to present them in depth — the pre-read covers them.
But you do need to be comfortable enough to answer questions and
suggest appropriate proxies when data is not available.

The key thing to communicate is that these frameworks are not Red Hat
constructs. They are industry standards used widely across technology
organisations regardless of platform choice. That neutrality matters
for the credibility of the scorecard.

### Anticipate where resistance may come from

Workshop 4 sometimes surfaces resistance from platform teams who feel
that being measured on DORA metrics is unfair — because delivery
performance depends on many things outside the platform team's control.

Acknowledge this directly and early. The scorecard is not an assessment
of the platform team. It is a measure of what the platform enables for
the teams that use it. The distinction matters.

---

## Session agenda

| Time | Section | Duration |
|------|---------|----------|
| 0:00 | Welcome, recap, and outcomes | 8 minutes |
| 0:08 | Why value alongside cost | 7 minutes |
| 0:15 | Introduce the scorecard categories | 10 minutes |
| 0:25 | Build the scorecard — category by category | 45 minutes |
| 1:10 | Agree target directions | 10 minutes |
| 1:20 | Close and next steps | 10 minutes |

---

## Section by section guidance

---

### Welcome, recap, and outcomes (8 minutes)

**What you are doing**

Opening the session, recapping the cost picture built so far, and
framing why today's session is different — and important.

**Talk track**

*"Welcome back. In the last three workshops we built a cost taxonomy,
a baseline model, and a unit economics picture. We now have a clear
view of what the Kubernetes estate costs and what it costs per useful
outcome.*

*Today is different. Today we look at what the platform enables — and
what we would risk if cost decisions were made without considering that.*

*By the end of this session we will have a value and risk scorecard
that sits alongside the unit economics model. Together they give
leadership a balanced view — not just cost, but value, risk, and
delivery performance."*

Check in:

*"Before we start — any questions from Workshop 3, or anything in
the unit economics model that is still sitting uncomfortably?"*

**Facilitation notes**

- If the unit economics model produced surprises in Workshop 3, address
any residual concerns now before moving forward.
- Frame this session as completing the picture — not as a separate
activity. The scorecard and the cost model belong together.

---

### Why value alongside cost (7 minutes)

**What you are doing**

Making the case for the scorecard before building it. This section
is short but important — it sets the frame for everything that follows
and prevents Workshop 5 from becoming a cost-only conversation.

**Talk track**

*"I want to spend a few minutes on why this matters — because it is
easy to treat the scorecard as a nice-to-have after three workshops of
cost modelling.*

*Cost without value is an incomplete picture. A platform that looks
expensive may be delivering significant returns in delivery speed,
reliability, security posture, and developer productivity. A platform
that looks cheap may be hiding cost in incidents, audit failures, and
team friction.*

*When leadership only sees cost, they optimise in one dimension —
and they often shift cost somewhere less visible. The scorecard exists
to prevent that.*

*It also gives the platform team something they often lack — a way
to articulate value in terms leadership recognises. Not 'we keep the
lights on' but 'we reduced recovery time by X and increased deployment
frequency by Y.' That is a different conversation."*

**Facilitation notes**

- If someone in the room is sceptical — "we already know the platform
is valuable, we do not need to prove it" — engage with it directly:
  *"The scorecard is not about proving value internally. It is about
  having a defensible answer when leadership asks the question in
  Workshop 5 or in the final review."*
- Keep this section tight. Seven minutes is enough.

---

### Introduce the scorecard categories (10 minutes)

**What you are doing**

Walking the group through the four scorecard categories and the
frameworks behind them — quickly and in plain language.

**Talk track**

*"The scorecard is organised into four categories. Let me walk you
through them before we start building.*

*We are using DORA for delivery performance and reliability — it is
one of the most widely used frameworks for measuring software delivery,
used across the industry regardless of platform. And SPACE for developer
productivity — it gives us a way to think about developer experience
beyond just counting commits or deployments.*

*Neither of these is a Red Hat framework. They are industry standards.
That matters for the credibility of the scorecard with Finance and
Procurement."*

Walk through the four categories briefly:

**Delivery performance**
*"How effectively the platform enables teams to ship changes safely
and quickly — deployment frequency, lead time, change failure rate."*

**Reliability**
*"How stable the platform is and how quickly it recovers when things
go wrong — incident volume, time to restore, availability."*

**Security and compliance effort**
*"How much effort the platform requires to meet security and compliance
obligations — time to patch, policy coverage, audit evidence effort."*

**Developer experience**
*"How much friction developers experience — onboarding time, time to
first deployment, ticket and toil volume."*

Then address proxies:

*"Not every organisation has formal DORA metrics in place. That is
completely fine. For each measure, we will agree a proxy if the direct
measurement is not available. A proxy is an imperfect but directionally
useful substitute — and a rough number with a Low confidence rating is
more useful than no number at all."*

**Facilitation notes**

- If someone asks for more detail on DORA or SPACE, acknowledge it
and move on — the pre-read covers it and the session is not a
framework tutorial.
- If someone challenges the relevance of a category to their
environment, note it and ask them to hold the thought — it will
surface in the scorecard building exercise.

---

### Build the scorecard — category by category (45 minutes)

**What you are doing**

Working through each category and agreeing measures, baselines,
and data sources. This is the core exercise of Workshop 4.

**How to run it**

Work through the four categories in order. For each category:

1. Present the suggested measures — ask the group to confirm,
swap, or add
2. For each confirmed measure, agree the data source or proxy
3. Capture the baseline value — real data or estimate with
confidence rating
4. Note what the measure signals and why it matters

Allow roughly ten to twelve minutes per category. Keep pace steady
— it is better to have eight well-understood measures than twelve
poorly understood ones.

**Category guidance**

---

**Delivery performance (10-12 minutes)**

Suggested measures:

- Deployment frequency — how often teams deploy to production
- Lead time for changes — from code commit to production
- Change failure rate — percentage of deployments causing failure

*"Let us start with delivery performance. These three measures —
deployment frequency, lead time, and change failure rate — are the
core DORA delivery metrics.*

*Does your organisation track any of these formally? If not, let us
agree a proxy for each one."*

Proxy options if formal tracking is not in place:

| Measure | Proxy if not tracked |
|---------|---------------------|
| Deployment frequency | Release cadence per team per month |
| Lead time | Estimated time from code review to production |
| Change failure rate | Proportion of deployments followed by a hotfix or rollback |

For each measure agreed, capture:
- Data source or proxy
- Baseline value
- Confidence rating (H / M / L)

*"What does the current picture tell us? Is the platform accelerating
or constraining delivery?"*

**Facilitation notes**

- If delivery performance data is completely unavailable, agree three
proxies and rate them all Low confidence. That is still a baseline
worth having.
- If the platform team feels that delivery metrics are outside their
control, acknowledge it:
  *"The scorecard is not measuring the platform team's performance.
  It is measuring what the platform enables for the teams using it.
  The distinction matters — and it is what makes this defensible."*

---

**Reliability (10-12 minutes)**

Suggested measures:

- Incident volume — number of production incidents per quarter
- Time to restore service (MTTR) — average recovery time
- Platform availability — uptime percentage

*"Reliability is the other half of the DORA picture. How stable is
the platform — and how quickly does it recover when things go wrong?*

*Do you have incident data from the last quarter? Even a rough count
and a sense of typical recovery time is enough to start."*

Proxy options if formal tracking is not in place:

| Measure | Proxy if not tracked |
|---------|---------------------|
| Incident volume | On-call escalations per quarter |
| MTTR | Estimated average duration from on-call logs |
| Availability | Rough uptime estimate from the platform team |

For each measure agreed, capture:
- Data source or proxy
- Baseline value
- Confidence rating (H / M / L)

*"Is there a pattern here — are incidents concentrated on specific
platforms or clusters? Are recovery times improving or worsening?"*

**Facilitation notes**

- If a recent major incident is fresh in people's minds, it may
dominate the reliability conversation. Acknowledge it and then
move to the broader pattern:
  *"That incident is important context. For the scorecard we want
  to capture the broader pattern — not just the outlier."*
- If availability is tracked formally, great. If not, a rough
estimate from the platform team is fine with a Low confidence rating.

---

**Security and compliance effort (10-12 minutes)**

Suggested measures:

- Time to patch critical vulnerabilities — from disclosure to patched
- Policy coverage — percentage of workloads governed by automated
policy controls
- Audit evidence effort — time spent generating evidence per audit cycle

*"Security and compliance effort is one of the most underappreciated
platform value measures — because it is invisible when it is working
well and very visible when it is not.*

*The question we are asking is: how much effort does the platform
require to meet security and compliance obligations? And is that
effort increasing or decreasing?"*

Proxy options if formal tracking is not in place:

| Measure | Proxy if not tracked |
|---------|---------------------|
| Time to patch | Estimated average from recent CVE responses |
| Policy coverage | Rough percentage of workloads with enforced controls |
| Audit evidence effort | Estimated person-days per audit cycle |

For each measure agreed, capture:
- Data source or proxy
- Baseline value
- Confidence rating (H / M / L)

*"Is the platform reducing security and compliance effort — or
adding to it? How would this picture change if the platform
were consolidated or fragmented?"*

**Facilitation notes**

- Security and compliance effort is often most relevant to regulated
environments. If the organisation is not heavily regulated, adjust
the emphasis accordingly — policy coverage and patch time still
matter but audit evidence effort may be less central.
- If policy coverage is low, note it as a risk signal rather than
a platform failure — it is a finding that belongs in the decision
brief.

---

**Developer experience (10-12 minutes)**

Suggested measures:

- Onboarding time — time for a new service or team to reach first
deployment
- Time to first deployment — from zero to production for a new workload
- Ticket and toil volume — support tickets or manual steps per
deployment

*"Developer experience is where platform value is felt most directly
by the people using it — but it is often the hardest to measure.*

*We are using SPACE as a reference here — not to measure all five
dimensions formally, but to make sure we are thinking about developer
experience beyond just output metrics.*

*What do you know about the current experience? What takes longer than
it should? Where do teams get stuck?"*

Proxy options if formal tracking is not in place:

| Measure | Proxy if not tracked |
|---------|---------------------|
| Onboarding time | Estimated from recent team onboarding experiences |
| Time to first deployment | Estimated from platform team experience |
| Ticket and toil volume | Support ticket count per month or per deployment |

For each measure agreed, capture:
- Data source or proxy
- Baseline value
- Confidence rating (H / M / L)

*"Is the platform reducing friction for developers — or adding to it?
What would improving these measures be worth in developer time and
satisfaction?"*

**Facilitation notes**

- Developer experience data is often the most anecdotal. That is
fine — anecdote with a Low confidence rating is still a baseline.
- If the platform team is defensive about developer experience
findings — "that is not our fault, it is the teams" — acknowledge
it and reframe:
  *"The scorecard is not assigning blame. It is establishing a
  baseline so we can track whether things improve. If there are
  structural reasons for friction that are outside the platform
  team's control, we note that in the findings."*
- If the group starts generating a long list of developer pain
points, note them but keep the scorecard to three to four measures
per category. Depth over breadth.

---

### Agree target directions (10 minutes)

**What you are doing**

For each measure on the scorecard, agreeing whether the target is
to increase, decrease, or maintain — and roughly by how much and
over what timeframe.

**Talk track**

*"We have a baseline for each measure. Now I want to agree target
directions — not precise targets, but a clear sense of where each
measure should move and over what timeframe.*

*This is important for two reasons. First, it turns the scorecard
from a snapshot into a management tool. Second, it gives us a way
to evaluate scenarios in Workshop 5 — not just by cost impact but
by impact on these measures."*

Work through the scorecard:

For each measure:
- Is the target direction increase, decrease, or maintain?
- What is a realistic improvement over six to twelve months?
- What would achieving that improvement be worth?

**Facilitation notes**

- Keep targets directional rather than precise. "Reduce MTTR by
roughly 30% over six months" is more useful than a precise number
that will be argued over.
- If the group cannot agree a target for a measure, note it as
"direction TBC" and move on. Unresolved targets belong in the
decision brief as decisions required.
- Connect targets back to the cost model where you can:
  *"If we reduce onboarding time from three weeks to one week,
  what does that free up in platform team capacity? How does that
  show up in the ops cost per cluster metric?"*

---

### Close and next steps (10 minutes)

**What you are doing**

Summarising what was produced, confirming the scorecard is saved
and shared, and making Workshop 5 completely clear.

**Talk track**

*"Here is what we have built today. A value and risk scorecard with
[NUMBER] measures across delivery performance, reliability, security
and compliance effort, and developer experience. Every measure has a
baseline and a target direction.*

*This scorecard sits alongside the unit economics model. Together
they give leadership a complete picture — not just what the platform
costs, but what it enables and what would be at risk if we optimised
cost without considering value.*

*Workshop 5 is [DATE/TIME]. That is the final session — where we
bring everything together. We will model three to five scenarios,
compare them on cost and value, agree a recommended path, and build
a 90-day plan.*

*You will get a short recap from me within 24 hours — decisions made,
actions, and the Workshop 5 pre-read."*

Then ask the final question:

*"Looking at the scorecard — does anything surprise you? And is there
anything that feels wrong or missing before we take this into the
scenario modelling?"*

---

## Handling difficult moments

### "We do not track any of these metrics"

Do not treat it as a blocker. Treat it as a finding and an opportunity.

*"That is actually useful information. Not tracking delivery or
reliability metrics is itself a signal — and improving measurement is
a quick win we can include in the 90-day plan. For today, let us agree
proxies and rate them Low confidence. A rough baseline is more useful
than no baseline."*

### "DORA metrics are not relevant to our environment"

Engage with this directly rather than dismissing it.

*"DORA is designed to be applicable across different delivery contexts.
The specific numbers will vary — what matters is the direction. Are
deployments getting faster or slower? Is recovery time improving or
worsening? If the standard measures do not fit, let us agree proxies
that do."*

### "The platform team should not be measured on delivery performance —
that is the product teams' responsibility"

This comes up often. Address it clearly.

*"The scorecard is not measuring the platform team. It is measuring
what the platform enables for the teams using it. If delivery
performance is constrained by something outside the platform — tooling,
process, organisation — we note that. The scorecard is a fact base,
not a performance review."*

### "Some of these measures will make the platform look bad"

Be direct and reassuring.

*"That is possible — and that is okay. A scorecard that only shows
positive measures is not credible. What matters is that the baseline
is honest, the confidence ratings are accurate, and the target
directions are realistic. An honest baseline is what enables a
credible improvement story."*

### The session runs short

If you finish the scorecard with time to spare, use it to deepen
the target direction discussion — particularly connecting scorecard
targets to the unit economics model. That connection is what makes
Workshop 5 stronger.

---

## Output checklist

Before you close the session, confirm these are in place:

- [ ] Scorecard populated — eight to twelve measures with baselines
and confidence ratings
- [ ] Proxies agreed and documented where direct measurement is
not available
- [ ] Target directions agreed for each measure
- [ ] Scorecard saved and versioned
- [ ] Assumptions Register updated with any new decisions
- [ ] Workshop 5 date and time confirmed

---

## Post-session actions (within 24 hours)

- [ ] Send recap email — decisions made, actions, Workshop 5 confirmed
- [ ] Save and share the value and risk scorecard — clearly versioned
- [ ] Update the Assumptions Register — version bumped with today's date
- [ ] Send Workshop 5 pre-read and calendar invite
- [ ] Begin assembling the full decision brief outline — cost model,
unit economics, showback view, and scorecard together for the
first time
