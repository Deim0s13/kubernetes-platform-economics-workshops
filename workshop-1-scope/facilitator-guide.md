# Workshop 1 — Facilitator Guide
## Scope, Glossary, and Rules of the Game

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

Workshop 1 is where the assessment begins in earnest. The goal is to agree
the scope, the rules, and the language that every subsequent workshop builds
on.

This session is less about data and more about decisions. Every decision made
here goes into the Assumptions Register — a versioned record that makes the
final output defensible with leadership, Finance, and Procurement.

By the end of this session you will have:

- A written scope statement agreed by the room
- Assumptions Register v1 populated with every scope and cost treatment
decision made today
- A glossary of agreed terms that everyone will use consistently
- A unit metrics shortlist — three to five measures to report cost per
outcome
- A data request list with named owners and due dates
- A list of the decisions leadership will need to make at the end of the
five workshops

---

## Before the session

### Confirm these are in place

- [ ] Pre-read email sent three to five days before the session
- [ ] Assumptions Register document created and shared — even if empty
- [ ] Data request list template open and ready to populate
- [ ] Workshop plan updated with today's session confirmed
- [ ] Recap from Workshop 0 sent and any open actions followed up

### Review before you walk in

- Scope shape agreed in Workshop 0 — confirm it is still accurate
- Data owners identified in Workshop 0 — check whether any inputs have
already come in
- Any open questions or concerns raised in Workshop 0 — address these
early in today's session if they are still live

### Know the answer to this question

*"If someone asked me right now what counts as a platform cost versus a
workload cost in this environment — could I explain the distinction clearly
and consistently?"*

If you cannot, work through the cost scope section of this guide before
the session. This is the concept that trips up most groups in Workshop 1.

---

## Session agenda

| Time | Section | Duration |
|------|---------|----------|
| 0:00 | Welcome, recap, and outcomes | 10 minutes |
| 0:10 | Confirm and lock scope | 20 minutes |
| 0:30 | Agree cost treatment rules | 20 minutes |
| 0:50 | Unit metrics shortlist | 15 minutes |
| 1:05 | Data request and owners | 10 minutes |
| 1:15 | Close and next steps | 5 minutes |

---

## Section by section guidance

---

### Welcome, recap, and outcomes (10 minutes)

**What you are doing**

Opening the session, recapping what was agreed in Workshop 0, and
confirming what this session produces. Give the group a clear line of
sight from where they are now to the output they will have in 90 minutes.

**Talk track**

*"Welcome back. In Workshop 0 we agreed scope shape, delivery model, and
data owners. Today we go a level deeper — we are going to lock in the
scope, agree the rules for how we treat costs, and make sure we all mean
the same things when we use the same words.*

*By the end of this session we will have the Assumptions Register v1
populated, a unit metrics shortlist agreed, and a data request list with
names against every item.*

*Everything we agree today becomes the foundation for the baseline we build
in Workshop 2 — so it is worth taking the time to get it right."*

Then check in:

*"Before we get started — anything from Workshop 0 that needs clearing up,
or anything that has come up since that we should know about?"*

**Facilitation notes**

- If new concerns have emerged since Workshop 0, address them now rather
than letting them sit.
- If data has already started coming in, acknowledge it and note it in
the register.
- Keep this section tight — ten minutes is enough for a recap.

---

### Confirm and lock scope (20 minutes)

**What you are doing**

Moving from the draft scope shape agreed in Workshop 0 to a written,
agreed scope statement. Every decision goes into the Assumptions Register
in real time.

**Talk track**

*"We agreed a rough scope shape in Workshop 0. Today I want to lock that
down properly — so there is no ambiguity later about what is in and what
is out.*

*Let us work through this section by section."*

**Platforms**

*"We agreed [PLATFORMS FROM WORKSHOP 0] are in scope for the baseline.
Is that still right? Is there anything running that we have missed?"*

Confirm:

- OpenShift — in scope for baseline
- EKS — in scope for baseline
- AKS — in scope for baseline
- ARO / ROSA — scenario options, not baseline platforms
- Anything else — confirm or exclude explicitly

**Environments**

*"Are we including non-production in the baseline? The default is yes,
but some organisations prefer to model them separately."*

Confirm and record the decision. If separating prod and non-prod, note
how they will be distinguished — by cluster, by namespace, or by tag.

**Time window**

*"We discussed [TIME WINDOW FROM WORKSHOP 0] as our reporting period.
Does that still feel right, or has anything changed?"*

Confirm a start and end date. Note it in the Assumptions Register with
the reason for that choice.

**Cost types**

Work through each cost type explicitly and confirm in or out:

| Cost type | Examples | In scope? |
|-----------|---------|-----------|
| Cloud compute | EC2, virtual machines, node pools | |
| Cloud storage | Block storage, object storage | |
| Cloud network | Load balancers, NAT, egress | |
| Managed service fees | EKS fees, AKS fees | |
| Platform tooling | Observability, security, CI/CD | |
| Subscriptions | Platform licences, support | |
| Operating effort | Platform team time | |
| Shared services | IAM, shared logging platforms | |

For any cost type that is uncertain or contested, note it as a gap with
a confidence rating and move on. Do not let one line item stall the
session.

Close this section with:

*"Is there anything we have included that we should not have — or anything
we have left out that we would regret missing?"*

**Facilitation notes**

- Capture every decision in the Assumptions Register as it is made. Do
not wait until after the session.
- If disagreement surfaces about a cost type, apply this test:
  *"Would excluding this create a misleading picture of the true cost?
  If yes, include it with a low confidence rating."*
- Scope creep is common here. If the list starts expanding, apply the
same discipline as Workshop 0 — park additions and protect the core.

---

### Agree cost treatment rules (20 minutes)

**What you are doing**

Agreeing how shared and complex costs will be handled. This is the most
important section of Workshop 1 — and the one most likely to surface
disagreement.

**Why this matters**

Most cost debates come from hidden assumptions about how costs are treated.
By making these rules explicit and agreed now, you prevent the kind of
"that number is wrong" conversations that derail the final output.

**Talk track**

*"Every cost baseline has shared costs — things that serve more than one
platform or team and cannot be cleanly attributed to one place. We need
to agree how we handle those before we start building the model.*

*I want to be clear: we are not implementing chargeback today. We are
agreeing showback rules — making costs visible before we start billing
anyone for them."*

Work through these four rules and agree each one:

**Rule 1 — Shared platform costs**

*"Some platform costs — shared tooling, shared infrastructure, shared
services — serve multiple platforms or teams. How do we want to treat
those in the baseline?"*

Options:

- Allocate proportionally by usage (best if tagging exists)
- Allocate equally across platforms (simpler but less precise)
- Hold in a shared bucket and note as unallocated (acceptable for v1)

Record the decision and the reason.

**Rule 2 — Non-production environments**

*"Do we allocate non-production costs separately, include them in the
total, or exclude them from the unit economics?"*

Options:

- Include in total, separate line item
- Include in total, not separated
- Exclude from unit economics but include in total cost

Record the decision and the reason.

**Rule 3 — Operating effort**

*"We agreed to include operating effort in scope. How do we want to
capture it? A time-split estimate from the platform team is the most
practical starting point."*

Options:

- Percentage split of platform team time across activities
- Rough hours per activity per month
- Fully exclude if too uncertain — note as a gap

Record the decision. If excluding, note the confidence impact.

**Rule 4 — Tooling duplication**

*"Where the same capability exists across multiple platforms — for
example, separate observability stacks for each platform — do we want
to call that out explicitly as a duplication cost?"*

Options:

- Yes — model it as a separate line with an estimated consolidation saving
- No — include in platform tooling cost without separating

Record the decision.

**Close this section with:**

*"Those are the rules we will apply consistently throughout the model.
If anything changes as we gather data, we update the Assumptions Register
and note the version. Agreed?"*

**Facilitation notes**

- If the group gets stuck on a rule, offer a default and move on:
  *"The default approach is to hold shared costs in an unallocated
  bucket for v1 and refine allocation in Workshop 3. Does that work
  as a starting point?"*
- Watch for perfectionism — someone will want to get the allocation
rules exactly right before proceeding. Remind them:
  *"We can refine the rules as we get better data. What matters now
  is that we agree a consistent approach."*
- If operating effort is deeply uncomfortable, offer to estimate it
as a range rather than a point figure. That is usually enough to
move forward.

---

### Unit metrics shortlist (15 minutes)

**What you are doing**

Agreeing a shortlist of three to five unit metrics — the measures that
will translate total spend into cost per useful outcome. You are not
defining them in full detail here — that is Workshop 3. You are agreeing
which ones are worth pursuing.

**Talk track**

*"Total spend is a number. Unit economics is what that number means.*

*Instead of saying 'we spend X on Kubernetes' we want to be able to say
'a production application costs Y per month' or 'each tenant costs Z per
quarter.' Those are the numbers leadership and Finance can actually act on.*

*I want to agree a shortlist of three to five unit metrics now — the ones
that make sense for your environment. We will define them properly and
build the model in Workshop 3."*

Present the menu and ask the group to shortlist:

| Unit metric | What it tells you |
|-------------|-------------------|
| Cost per production app per month | What it costs to run one app in production |
| Cost per tenant or namespace per month | What it costs to serve one team or product |
| Cost per environment | Prod versus non-prod cost split |
| Effective cost per vCPU-hour used | How efficiently purchased capacity is being used |
| Ops cost per cluster per month | The operational overhead of each cluster |
| Cost per deployment or release | What it costs to ship a change |

Ask:

*"Which three to five of these would be most useful to your leadership
team and Finance? Which ones connect most directly to how you talk about
the platform internally?"*

Once shortlisted, note any data dependencies that are already obvious —
for example, cost per app requires an app inventory, effective cost per
vCPU requires utilisation data.

**Facilitation notes**

- If the group wants more than five, push back gently:
  *"More metrics means more data to gather and more to explain to
  leadership. Let us keep it to five for now and add later if needed."*
- If the group is unsure, suggest starting with cost per production app
per month and effective cost per vCPU-hour used — these two tend to
land well with both technical and financial audiences.
- Note the data dependencies now so they feed into the data request list
in the next section.

---

### Data request and owners (10 minutes)

**What you are doing**

Finalising the data request list with a named owner and a realistic due
date against every item. You want to leave this session with no blank
owner fields.

**Talk track**

*"We touched on data ownership in Workshop 0. Now that we have agreed
scope and unit metrics, let us finalise the list and make sure everything
has a name against it.*

*I am not looking for perfect data by Workshop 2. I am looking for a best
available first pass — something we can build the baseline skeleton from
and refine as better data comes in."*

Work through the data request list together:

| Data needed | Why we need it | Owner | Due date | Confidence |
|-------------|----------------|-------|----------|------------|
| Cluster inventory | Defines scope | | | |
| Cloud billing exports (AWS CUR / Azure) | Source of truth for spend | | | |
| Platform subscription details | Fixed vs variable cost | | | |
| Tooling list and costs | Duplication and consolidation | | | |
| Ops effort estimate | Cost not on invoices | | | |
| Production app list or top 20 | Unit economics foundation | | | |
| Namespace or team mapping | Allocation rules | | | |
| Utilisation data (CPU / memory) | Effective cost per vCPU | | | |

For any item without a clear owner:

*"Who is best placed to track this down? It does not have to be the
person who owns the data — it just needs to be someone who can get it."*

For any item where the due date is uncertain:

*"What is a realistic date — not the ideal date, the realistic one?"*

**Facilitation notes**

- Do not leave without a name against every item. TBC is acceptable
temporarily — but agree who TBC means and when they will confirm.
- If something is going to take longer than expected, note it and agree
whether to proceed with an estimate in Workshop 2 or delay.
- Add any data items that emerged from the unit metrics discussion in
the previous section.

---

### Close and next steps (5 minutes)

**What you are doing**

Summarising what was agreed, confirming the Assumptions Register is
captured, and making Workshop 2 completely clear.

**Talk track**

*"Here is what we have agreed today.*

*Scope is locked — [brief summary]. Cost treatment rules are agreed and
in the Assumptions Register. We have a unit metrics shortlist of [METRICS].
And we have a data request list with names and dates against every item.*

*Workshop 2 is [DATE/TIME]. That is where we build the cost taxonomy and
baseline model skeleton — we will use the data that comes in between now
and then to start filling it in.*

*You will get a short recap from me within 24 hours — decisions made,
actions, and the Workshop 2 pre-read."*

Then ask the final question and mean it:

*"Is there anything we have not resolved today that would make you less
confident going into Workshop 2?"*

---

## Handling difficult moments

### "We do not know what our utilisation looks like"

This is common. Do not treat it as a blocker.

*"That is fine — it is one of the things the baseline will surface.
We will note it as a gap, give it a low confidence rating, and use a
reasonable estimate as a placeholder. When the data comes in, we update
the model."*

### "Our tagging is a mess"

Also common. Same approach.

*"Tagging gaps are a finding, not a blocker. We will note the current
state, agree a minimum viable tagging standard for this work, and flag
it as an improvement in the output."*

### "Why are we including operating effort? That feels arbitrary"

*"Operating effort is often the largest hidden cost in a platform team.
If we exclude it, we risk making decisions based on an incomplete cost
picture. We can capture it as a range with a low confidence rating — it
does not need to be precise to be useful."*

### "Can we just use our existing cost reports?"

*"Absolutely — existing reports are a great starting point. What we
are doing here is agreeing how to interpret and structure them
consistently so the output is comparable and defensible. Existing
reports will feed straight into the model."*

### Disagreement about what counts as a platform cost

Apply this test out loud:

*"If we excluded this cost, would the picture of true platform cost be
misleading? If yes, include it with a note and a confidence rating.
If no, exclude it and note why."*

---

## Output checklist

Before you close the session, confirm these are in place:

- [ ] Scope statement written and agreed
- [ ] Assumptions Register v1 populated with all scope and cost treatment
decisions
- [ ] Glossary updated with any new terms agreed today
- [ ] Unit metrics shortlist confirmed — three to five metrics named
- [ ] Data request list finalised — every item has a named owner and
due date
- [ ] Workshop 2 date and time confirmed

---

## Post-session actions (within 24 hours)

- [ ] Send recap email — decisions made, actions, Workshop 2 confirmed
- [ ] Save and version the Assumptions Register — v1.0 with today's date
- [ ] Share the data request list with all owners
- [ ] Send Workshop 2 pre-read and calendar invite
- [ ] Follow up individually with any data owners who seemed uncertain
about their items
