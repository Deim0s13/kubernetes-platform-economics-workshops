# Workshop 5 — Facilitator Guide
## Scenarios, Recommendation, and 90-Day Plan

**Version:** 1.0
**Duration:** 3 hours
**Audience:** Product Owner, Platform Lead, Platform Engineers and SREs
**Facilitator:** [FACILITATOR]

---

## Version history

| Version | Date | Changes |
|---------|------|---------|
| 1.0 | [DATE] | Initial version |

---

## Purpose

Workshop 5 is where the work becomes a decision. Everything built across
four workshops — cost baseline, unit economics, showback view, and value
scorecard — is brought together here and turned into a set of scenarios,
a recommendation, and a plan.

This session is longer than the others because it needs to produce
something decision-ready. The output — a decision brief outline with a
recommended path and a 90-day plan — goes to CIO, GM of Technology and
Operations, Finance, and Procurement. It needs to be credible, balanced,
and defensible.

Your job in this session is to stay neutral on scenarios until the
evidence points somewhere. The recommendation should emerge from the
analysis — not precede it.

By the end of this session you will have:

- A workload placement matrix — agreed criteria and scored workloads
- A scenario comparison — four scenarios evaluated on cost, value,
risk, and time to value
- A recommended path — with a clear, evidence-based rationale
- A 90-day plan — no-regrets actions, decisions required, and pilots
- A decision brief outline — the structure of the exec-ready output

---

## Before the session

### Assemble the complete picture

Before Workshop 5, compile all outputs from Workshops 1 through 4 into
a single working document or shared view. The group needs to be able to
see the full picture during the session — cost model, unit economics,
showback view, and scorecard together.

Check for anything that looks inconsistent or incomplete. If something
is wrong, it is better to address it at the start of Workshop 5 than
to build scenarios on a flawed foundation.

### Prepare the scenario model

Set up a scenario comparison template before the session with four tabs
or sections — one per scenario. Each should include fields for:

- What changes
- Cost impact — hard savings, avoidance, capacity release, toil reduction
- Value and risk impact — against the scorecard categories
- Time to value
- Key dependencies
- Risk rating and mitigations
- Recommended next step

### Prepare the workload placement matrix

Set up a matrix with ten to twenty candidate workloads as rows and the
six placement criteria as columns. Leave the scoring blank — this is
filled in during the session.

### Know your constraints

Before the session, think through any constraints that will shape the
scenario discussion:

- Are there contract or renewal timelines that affect sequencing?
- Are there regulatory requirements that rule out certain options?
- Are there team capacity constraints that affect what is realistic?
- Are there known executive preferences that should be surfaced early?

You do not need to pre-solve these — but knowing they exist means you
can surface them at the right moment rather than letting them derail
the discussion later.

---

## Session agenda

| Time | Section | Duration |
|------|---------|----------|
| 0:00 | Welcome, recap, and full picture review | 15 minutes |
| 0:15 | Workload placement matrix | 40 minutes |
| 0:55 | Scenario comparison | 60 minutes |
| 1:55 | Recommendation | 20 minutes |
| 2:15 | 90-day plan | 30 minutes |
| 2:45 | Decision brief outline and close | 15 minutes |

---

## Section by section guidance

---

### Welcome, recap, and full picture review (15 minutes)

**What you are doing**

Opening the session, recapping the journey, presenting the full picture
of outputs from Workshops 1 through 4, and confirming everything is
accurate before building scenarios on top of it.

**Talk track**

*"Welcome to Workshop 5 — the final session. Over the last four workshops
we have built a cost baseline, unit economics, a showback view, and a
value and risk scorecard. Today we use all of that to evaluate scenarios,
agree a recommendation, and build a 90-day plan.*

*Before we get into scenarios I want to spend a few minutes reviewing
the full picture — because the scenarios are only as good as the inputs
they are built on. If anything looks wrong, I want to know now rather
than after we have built a recommendation on it."*

Present each output briefly:

- Cost baseline — headline spend by bucket, fixed versus variable split
- Unit economics — the three to five agreed metrics with baseline values
- Showback view — cost by team or namespace
- Value scorecard — headline measures with baselines and target directions

Then check in:

*"Does this picture feel accurate? Is there anything that looks wrong
or has changed since we last met?"*

**Facilitation notes**

- If something material has changed — new data, a significant revision
to the model — address it now. Do not build scenarios on stale inputs.
- If the group is broadly comfortable with the picture, move on. This
section is a checkpoint, not a re-run of Workshops 1 through 4.
- If a concern surfaces that cannot be resolved quickly, note it as an
assumption with a Low confidence rating and proceed. The recommendation
will carry an appropriate caveat.

---

### Workload placement matrix (40 minutes)

**What you are doing**

Building a structured view of which workloads belong on which platform
and why — using agreed criteria rather than habit or history. This
matrix is the foundation for the scenario comparison and for making
the recommendation defensible.

**Why this matters**

Without a placement matrix, the scenario comparison becomes a platform
debate. With it, the conversation is grounded in workload characteristics
rather than preference. That is what makes the recommendation credible
with Finance and Procurement.

**Talk track**

*"Before we compare scenarios I want to build a workload placement matrix.
This is a structured view of which workloads belong on which platform —
based on what the workload needs, not on habit or history.*

*We are going to take ten to twenty meaningful workloads and score them
against six criteria. The output tells us which workloads are good
candidates for consolidation or migration — and which have genuine
constraints that justify keeping them where they are."*

Walk through the six criteria:

*"Compliance and policy intensity — how much policy enforcement and audit
evidence does this workload require? High-compliance workloads tend to
benefit from platforms with strong, consistent policy controls.*

*Cloud-native coupling — how tightly is this workload coupled to services
specific to one cloud provider? A workload deeply integrated with
provider-specific managed services has a real switching cost.*

*Operational burden — how much day-two operational effort does this
workload generate? High-burden workloads are often good candidates for
consolidation onto a platform with better operational tooling.*

*Portability need — does this workload need to move between platforms
or clouds in the future? High portability needs favour platform-agnostic
deployment patterns.*

*Migration complexity — how difficult and risky would it be to move this
workload? This is the practical constraint on what is achievable in a
given timeframe.*

*Data gravity and latency — are there performance or data residency
constraints that pin this workload to a specific location or provider?"*

Work through the matrix:

Score each workload against each criterion — High, Medium, or Low.
Do not spend more than two to three minutes per workload. The pattern
across workloads matters more than the precision of any single score.

After scoring, identify:

- Consolidation candidates — workloads with low cloud-native coupling,
high operational burden, high compliance needs, and low migration
complexity
- Justified exceptions — workloads with high cloud-native coupling,
hard latency or data gravity constraints, or genuinely high migration
complexity
- Managed platform candidates — workloads with high operational burden
and low cloud-native coupling

**Facilitation notes**

- Keep the pace steady. Two to three minutes per workload maximum.
If the group gets stuck on a single workload, score it tentatively
and move on — you can revisit at the end.
- If a workload scores ambiguously, note it as a spike candidate
rather than forcing a placement decision now.
- The placement matrix is not a migration plan. It is a diagnostic
tool. The actual migration sequencing belongs in the 90-day plan.
- Watch for the person who wants to justify the current state for
every workload. If every workload is a justified exception, the
matrix is not working. Gently challenge:
  *"What would need to be true for this workload to be a
  consolidation candidate? Is that a hard constraint or a soft
  preference?"*

---

### Scenario comparison (60 minutes)

**What you are doing**

Evaluating four scenarios against cost, value, risk, and time to value —
using the placement matrix and the outputs from Workshops 1 through 4
as the evidence base.

**How to run it**

Work through the four scenarios in order. For each one spend roughly
twelve to fifteen minutes covering:

1. What changes — confirm the scope and shape of the scenario
2. Cost impact — hard savings, avoidance, capacity release, toil reduction
3. Value and risk impact — against the scorecard categories
4. Time to value — realistic estimate, not best case
5. Dependencies and constraints — what needs to be true for this to work
6. Risk rating — Low, Medium, or High, with brief mitigations

Keep the model visible on screen and update it live as each scenario
is discussed.

**Scenario guidance**

---

**Scenario A — Optimise the current estate**

What changes:
Current platforms stay broadly as-is. Focus on utilisation improvement,
cluster sprawl reduction, resource rightsizing, autoscaling, and tooling
consolidation where duplication exists.

Cost impact prompts:
- What is the utilisation gap identified in Workshop 3? What does closing
it by 20 to 30 percent mean in dollar terms?
- How many clusters could be retired or merged? What does each cluster
cost to operate?
- What tooling duplication could be eliminated? What does that save in
licences and operational overhead?

Value and risk impact prompts:
- Does this scenario improve or worsen the scorecard measures?
- Does it reduce operational burden — or does it require significant
upfront effort with delayed benefit?

Time to value:
- No-regrets optimisations: 4 to 12 weeks
- Cluster consolidation: 1 to 2 quarters

Risk: Low. No structural change. Benefits are incremental.

This scenario sets the floor. Every other scenario needs to perform
better on at least one dimension to justify its additional complexity.

---

**Scenario B — Consolidate workloads across platforms**

What changes:
Workloads identified as consolidation candidates in the placement matrix
are migrated to a preferred platform. Platform and tooling duplication
is reduced. The estate becomes more intentional.

Cost impact prompts:
- What is the tooling duplication cost identified in Workshop 2?
Consolidation eliminates it.
- What is the ops cost per cluster from Workshop 3? How does it change
if cluster count reduces?
- What is the cost of running three separate sets of standards, runbooks,
and on-call coverage? Consolidation reduces it.

Value and risk impact prompts:
- Fewer platforms means fewer contexts for the platform team to maintain.
Does that improve or worsen delivery and reliability measures?
- Does consolidation improve policy coverage and security posture?
- What is the migration risk for the consolidation candidates?

Time to value:
- Tooling consolidation: 1 to 2 quarters
- Workload migration: 2 to 4 quarters depending on complexity

Risk: Medium. Migration introduces short-term risk. Mitigated by
sequencing consolidation candidates before complex workloads.

---

**Scenario C — Move some or all clusters to managed Kubernetes**

What changes:
Selected clusters or workloads move to a managed Kubernetes offering.
Control plane management, upgrades, and infrastructure reliability shift
to the managed service. Platform team capacity is redirected.

Cost impact prompts:
- What is the operating effort cost for upgrade and patching cycles?
Managed Kubernetes eliminates most of it.
- What is the infrastructure cost difference between self-managed and
managed? Model honestly — managed may cost more per node.
- What is the net impact — managed infrastructure cost versus reduced
operating effort?

Value and risk impact prompts:
- Does managed Kubernetes improve reliability — particularly around
upgrade reliability and control plane availability?
- Does it reduce the security and compliance effort for platform
infrastructure?
- What is the impact on developer experience — does managed simplify
or constrain the platform?

Time to value:
- Landing zone and pilot: 1 quarter
- Broader migration: 2 to 4 quarters

Risk: Low to Medium. Managed Kubernetes is a mature offering. Risk
is concentrated in the migration period and any workloads with
non-standard requirements.

---

**Scenario D — Hybrid portfolio**

What changes:
The estate is structured deliberately. Justified exceptions — workloads
with hard cloud-native coupling, data gravity, or compliance constraints
— stay where they are with documented reasons. Everything else is
consolidated to reduce duplication and improve unit economics.

Cost impact prompts:
- What is the cost of maintaining the justified exceptions versus
migrating them? Is the switching cost worth it?
- What is the consolidation saving for the non-exception workloads?
- What is the ongoing governance cost of maintaining a deliberate
hybrid model?

Value and risk impact prompts:
- Does the hybrid model preserve the delivery and reliability benefits
of both platforms?
- Does it reduce tooling and operational duplication sufficiently?
- Is the governance overhead of a deliberate hybrid model manageable?

Time to value:
- Governance model: 1 quarter
- Consolidation of non-exceptions: 2 to 4 quarters

Risk: Medium. Requires strong governance to prevent the hybrid model
from becoming an unmanaged sprawl by a different name.

---

**Facilitation notes for the scenario comparison**

- Keep the comparison balanced. Do not let any single scenario dominate
the discussion before all four have been evaluated.
- If someone advocates strongly for one scenario early, acknowledge it
and park it: *"Let us get all four scenarios on the table before we
start comparing. We want the recommendation to follow the evidence."*
- If cost and value point in different directions for a scenario, name
it explicitly: *"This scenario reduces cost but has a higher short-term
risk impact. That is a trade-off leadership needs to see clearly."*
- Update the scenario comparison table live. Seeing all four scenarios
side by side is what produces the recommendation — not evaluating
each one in isolation.

---

### Recommendation (20 minutes)

**What you are doing**

Facilitating the group to a recommended path — one that is grounded in
the evidence, accounts for trade-offs, and can be defended to leadership,
Finance, and Procurement.

**Talk track**

*"We have four scenarios evaluated. Now I want to work toward a
recommendation.*

*A recommendation is not 'the only right answer.' It is the path that
best fits the evidence, the constraints, and the organisation's risk
appetite — with the trade-offs clearly stated.*

*Let me ask three questions to start:*

*First — which scenarios does the evidence most clearly support? Where
do cost and value point in the same direction?*

*Second — which scenarios have dependencies or risks that make them
less viable in the near term?*

*Third — is there a combination — for example, Scenario A as a foundation
with elements of Scenario C — that performs better than any single
scenario alone?"*

Work toward a recommendation that includes:

- A primary recommended path — the scenario or combination that best
fits the evidence and constraints
- A clear rationale — why this path, why now
- Acknowledged trade-offs — what you are accepting or deferring
- A note on what would change the recommendation — the key assumptions
it depends on

**Facilitation notes**

- If the group cannot agree, name the disagreement and surface it as
a decision for leadership: *"There is a genuine difference of view
here. Let us document both positions and present them to leadership
as a decision they need to make — rather than us resolving it here."*
- If someone wants to recommend a scenario that the evidence does not
support, engage with it directly: *"Help me understand what the
evidence is for that path. I want to make sure the recommendation
can be defended when Finance and Procurement look at it."*
- The recommendation does not need to be unanimous in the room. It
needs to be evidence-based and clearly reasoned. Note any dissenting
views in the decision brief.

---

### 90-day plan (30 minutes)

**What you are doing**

Building a practical, actionable plan that leadership can approve and
the team can execute — structured across three tracks.

**Talk track**

*"The recommendation tells leadership what to do. The 90-day plan
tells them — and the team — what to do next.*

*We are going to build it across three tracks. No-regrets actions that
start immediately. Decisions that leadership needs to make before we
can go further. And pilots or spikes that validate key assumptions
before committing to structural change.*

*Let us work through each track."*

**Track 1 — No-regrets actions**

These improve the situation regardless of which scenario is chosen.
They can start immediately and do not require leadership approval
beyond the plan itself.

Prompt questions:
- What optimisations from Scenario A can start now?
- What tagging or governance improvements are prerequisite to everything else?
- What cluster retirements or merges are clearly justified regardless
of the broader scenario direction?
- What quick wins in the unit economics — rightsizing, autoscaling,
tooling consolidation — can be sequenced immediately?

For each action agree: owner, timeframe, expected outcome.

**Track 2 — Decisions required**

These are questions leadership needs to answer before the preferred
scenario can be fully committed to. Surface them clearly — not buried
in the appendix.

Prompt questions:
- What commercial or procurement decisions are time-sensitive?
- What organisational or resourcing decisions are blocking progress?
- What governance decisions need to be made about platform standards?
- What risk appetite decisions need leadership sign-off?

For each decision agree: who decides, by when, what the options are.

**Track 3 — Pilots and spikes**

These are short, time-boxed investigations to validate key assumptions
before committing to structural change.

Prompt questions:
- Which scenario assumptions carry the most uncertainty?
- What is the smallest experiment that would validate or invalidate
the managed Kubernetes option?
- What would a consolidation pilot look like — which workloads, which
platform, what success criteria?
- What technical unknowns need a spike before we can cost a scenario
with confidence?

For each pilot or spike agree: scope, success criteria, timeframe,
who runs it.

**Facilitation notes**

- Keep the 90-day plan realistic. It is better to have fewer actions
with clear owners than a long list that nobody acts on.
- If the group generates a long backlog, help them prioritise:
  *"If we could only do five things in the next 90 days, what would
  they be? What is the highest leverage and lowest risk starting point?"*
- Connect the plan back to the unit economics: *"If we do these
things, what do we expect to see move in the unit metrics? Which
scorecard measures should improve and by roughly how much?"*
- Every action needs an owner. Do not close this section without
a name against every item.

---

### Decision brief outline and close (15 minutes)

**What you are doing**

Confirming the structure of the decision brief that will be produced
for leadership, Finance, and Procurement — and closing the workshop
series.

**Talk track**

*"We have everything we need to produce the decision brief. Let me
confirm the structure so we are aligned on what goes to leadership.*

*The decision brief will cover:*

*Executive summary — what we assessed, key findings, and the
recommended path.*

*Methodology — how we structured the assessment, the frameworks
we used, and the confidence levels throughout.*

*Cost baseline — the TBM-aligned baseline with fixed versus variable
split and key drivers.*

*Unit economics — the three to five agreed metrics with baseline
values and what they mean.*

*Value and risk scorecard — the eight to twelve measures with
baselines and target directions.*

*Scenario comparison — the four scenarios evaluated on cost, value,
risk, and time to value.*

*Recommendation and rationale — the recommended path with clear
trade-offs and acknowledged assumptions.*

*90-day plan — no-regrets actions, decisions required, and pilots.*

*Appendix — assumptions register, data sources, confidence ratings,
sensitivity notes, and glossary.*

*That brief will go to [CIO / GM TECH AND OPS / FINANCE /
PROCUREMENT]. I will produce a draft within [TIMEFRAME] and share
it for review before it goes to that audience.*

*Any questions on the structure before we close?"*

Then close the workshop series:

*"That is the end of the five workshops. We came in with a commercial
question and a cost concern. We are leaving with a trusted fact base,
a balanced view of cost and value, a set of realistic options, and a
plan.*

*Thank you for the time and the honesty throughout this process. The
quality of the output depends on the quality of the inputs — and
this group has given us good inputs to work with.*

*I will have the decision brief draft to you by [DATE]."*

**Facilitation notes**

- Agree a specific date for the decision brief draft before closing.
Do not leave it as "soon" or "in the next few weeks."
- If there are outstanding data items that will affect the brief,
name them and agree who is closing them and by when.
- End the series on a note of genuine progress — not just process
completion. The group has built something real and useful.

---

## Handling difficult moments

### "The recommendation is obvious — why are we going through all four?"

*"Because the recommendation needs to be defensible, not just obvious.
When Finance or Procurement challenges it, 'we evaluated four scenarios
and this one came out ahead on cost and value' is a much stronger
answer than 'we thought this was the right thing to do.' The process
is what makes the output credible."*

### "We cannot recommend consolidation — the migration risk is too high"

Engage with this rather than accepting it at face value.

*"Let us look at what makes the migration risk high. Is it the
complexity of specific workloads — in which case the placement matrix
should have flagged those as justified exceptions? Or is it a general
risk aversion? If it is the latter, that is a reasonable position for
leadership to hold — but it should be a stated trade-off, not a reason
to avoid the analysis."*

### "I thought we were going to recommend [SPECIFIC OPTION]"

If someone came in with a predetermined answer, address it directly.

*"I hear that — and it may well be where the evidence lands. Let us
make sure we get there through the analysis rather than starting from
it. That is what makes the recommendation something Finance and
Procurement can stand behind."*

### The 90-day plan becomes a long wishlist

Bring it back to what is realistic and owned.

*"Let us be honest about what is achievable in 90 days. I would
rather we committed to five things with clear owners than listed
thirty things nobody acts on. What are the five highest-leverage
actions?"*

### "We do not have enough data to make a confident recommendation"

*"We never have perfect data — and we have been transparent about
confidence levels throughout. The recommendation is based on the
best available evidence, with clear assumptions noted. That is more
defensible than waiting for certainty that will not come."*

---

## Output checklist

Before you close the session, confirm these are in place:

- [ ] Workload placement matrix completed and agreed
- [ ] All four scenarios evaluated — cost, value, risk, time to value
- [ ] Recommendation agreed — with rationale and trade-offs noted
- [ ] 90-day plan built — actions, decisions, and pilots with owners
- [ ] Decision brief structure confirmed and review date agreed
- [ ] Any outstanding data items named with owners and dates
- [ ] Assumptions Register updated with any final decisions

---

## Post-session actions (within 48 hours)

- [ ] Send recap email — decisions made, recommendation confirmed,
90-day plan summary, decision brief timeline
- [ ] Save and share all session outputs — scenario comparison,
placement matrix, 90-day plan
- [ ] Update the Assumptions Register — final version, fully versioned
- [ ] Begin drafting the decision brief
- [ ] Circulate 90-day plan to action owners for confirmation
- [ ] Book decision brief review session with the platform team
before it goes to leadership
