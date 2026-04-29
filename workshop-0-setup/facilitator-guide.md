# Workshop 0 — Facilitator Guide
## Setup and Expectations

**Version:** 1.0
**Duration:** 35–45 minutes
**Audience:** Product Owner, Platform Lead, Platform Engineers and SREs
**Facilitator:** [FACILITATOR]

---

## Version history

| Version | Date | Changes |
|---------|------|---------|
| 1.0 | [DATE] | Initial version |

---

## Purpose

Workshop 0 is a setup session. Nothing is built here — but everything that
follows depends on getting this right.

The goal is simple: make sure everyone in the room understands what the work
is, why it matters, and how it will run. More importantly, it is your first
opportunity to build trust. How you show up in this session sets the tone for
every workshop that follows.

By the end of this session you will have:

- A shared understanding of the five-workshop journey and what it produces
- A draft scope shape — platforms, environments, and time window
- An agreed delivery model — who runs what and how
- Named data owners with an initial minimum viable data list
- A confirmed working setup — where documents live and how versions are
managed
- Agreed ways of working between sessions

---

## Before the session

### Set up the working environment

Do this before the session, not after. It signals you are organised and
reduces friction on the day.

- [ ] Create the shared workspace — folder in SharePoint, Confluence page,
or equivalent. Confirm the location with the team before the session.
- [ ] Create the Assumptions Register document — even if it is empty. Having
it ready to open in the session makes it real.
- [ ] Create the Workshop Plan document — sessions 0 through 5, with dates
TBC, duration, and who attends each one.
- [ ] Prepare the Data Request List — empty but structured, ready to
populate together.
- [ ] Send the pre-read email — 3 to 5 days before the session, with the
pre-read document attached.

### Know the answer to this question

Before you walk in, make sure you can answer this clearly in two minutes:

*"What are we going to end up with at the end of all five workshops?"*

If you cannot answer it confidently and plainly, re-read the narrative spine
in the repository README before the session. Every conversation in Workshop 0
connects back to that story.

### Check your assumptions

Think through these before the session:

- Do you know which platforms are in scope? OpenShift, EKS, AKS are the
baseline. ARO and ROSA sit in the scenarios.
- Do you have a sense of who owns cloud billing and subscription data?
- Is there any known sensitivity around cost data you should be aware of
going in?
- Is there any known scepticism or concern about the process you should be
ready to address?

---

## Session agenda

| Time | Section | Duration |
|------|---------|----------|
| 0:00 | Welcome and introductions | 5 minutes |
| 0:05 | What we are doing and what it produces | 8 minutes |
| 0:13 | Scope shape | 8 minutes |
| 0:21 | Delivery model and logistics | 5 minutes |
| 0:26 | Data sensitivity and minimum viable data | 8 minutes |
| 0:34 | Ways of working and next steps | 5 minutes |
| 0:39 | Close | 3 minutes |

---

## Section by section guidance

---

### Welcome and introductions (5 minutes)

**What you are doing**

Opening the session, confirming who is in the room, and setting the tone
before anything else.

**Do not start with the agenda.** Start with the goal. People engage with
purpose before they engage with process.

**Talk track**

*"Thanks for making time. Before we get into any data or modelling I want to
spend around 35 to 40 minutes making sure we are all clear on what we are
doing, why we are doing it, and how we will work together.*

*The goal at the end of all five workshops is a decision brief your
leadership team, Finance, and Procurement can act on with confidence. Today
is just about making sure we set that up properly."*

Then ask one question and genuinely listen to the answers:

*"What would make this feel worthwhile to you — personally, not just as a
team outcome?"*

**Facilitation notes**

- Let people answer fully. Do not rush past this.
- What they say here tells you where the anxiety or scepticism sits.
- Note anything that needs addressing directly — do not hope it goes away.
- If someone says something that reveals a misconception about the process,
address it calmly and directly before moving on.

---

### What we are doing and what it produces (8 minutes)

**What you are doing**

Walking the group through the five-workshop journey in plain language.
Not presenting — having a conversation.

**Talk track**

*"We are going to run five workshops together. Let me walk you through what
each one does.*

*The first one locks in scope and rules — what we are measuring and how we
will treat costs. The second follows the money — where spend actually goes
across your estate. The third translates that into cost per outcome, so we
are not just looking at a total number. The fourth makes sure we are
measuring whether the platform is actually performing. And the fifth gives
you options with numbers attached and a plan for what to do next.*

*At the end you will have a decision brief that clearly shows what you
spend, what drives it, what the platform enables, and what your realistic
options are. It will be written for technology leadership, Finance, and
Procurement — not just the platform team."*

Then be clear about what it is not:

*"This is not a vendor exercise. The frameworks we are using — FinOps, TBM,
DORA, and SPACE — are industry standards. If the numbers point toward
consolidation or a particular platform option, it will be because the data
supports it. If they point somewhere else, we will say that too."*

Pause and check in:

*"Any questions on the overall shape before we talk about scope?"*

**Facilitation notes**

- Keep this conversational. You are not presenting slides — you are having
a conversation.
- If someone asks a detailed technical question about a specific workshop,
acknowledge it and park it:
  *"Good question — that is exactly what we will dig into in Workshop
  [X]. Let us get the foundations right today first."*
- If someone raises the vendor question — "is this just a way to get us to
renew?" — address it directly. See the section on difficult moments later
in this guide.

---

### Scope shape (8 minutes)

**What you are doing**

Agreeing the boundaries of the work so nobody feels surprised later.
You are not locking down detail — you are confirming the shape.

**Talk track**

*"Before we can build anything we need to agree what we are looking at.
I want to confirm four things with you now — we will get into the detail
in Workshop 1, but let us make sure we are aligned on the shape."*

Work through these four questions and capture the answers in the
Assumptions Register as you go:

**Platforms**
*"Which platforms are we including in the baseline? I am assuming OpenShift,
EKS, and AKS — is that right? Is there anything else running that we
should not miss?"*

Note: ARO and ROSA are scenario options, not baseline platforms. You do not
need to explain this in detail here — just confirm the baseline.

**Environments**
*"Are we including non-production environments? The default is yes, but
some teams prefer to separate them. Either works — we just need to agree
it now."*

**Time window**
*"What time window are we working with? The last full quarter is usually
the cleanest. The last three months works if quarter boundaries are messy.
Which feels more representative of your normal operating picture?"*

**Cost types**
*"Are we including tooling costs — observability, security, CI/CD? And
are we including operating effort — time your team spends running the
platforms? Both matter, but if you are not ready to put numbers on ops
effort yet, we can note it as a gap and come back to it."*

Close this section with:

*"Is there anything in your Kubernetes estate that we would be embarrassed
to miss — or anything that should definitely stay out of scope?"*

**Facilitation notes**

- Capture every decision directly into the Assumptions Register in real
time. Do not wait until after the session.
- If scope starts expanding, bring it back:
  *"Let us capture that as a potential addition and park it for now.
  I want to make sure we have agreed the core scope before we add to it."*
- If they are unsure about a cost type, default to including it with a
low confidence rating rather than excluding it.

---

### Delivery model and logistics (5 minutes)

**What you are doing**

Agreeing how the workshops will be run and locking in the practicalities.

**Talk track**

*"There are two ways we can approach this. Your team runs the sessions
using the toolkit I will provide — agendas, templates, facilitation notes,
and example outputs. Or we facilitate together, building the model and
outputs jointly while your team owns the assumptions and decisions
throughout.*

*Either works. What matters is that the outputs stay yours regardless of
how we get there. What feels right for your team?"*

Once agreed, move to logistics:

*"A few practical things to lock in while we are here.*

*Where do we want working documents to live? I have already set up
[LOCATION] — does that work for everyone?*

*After each session I will send a short recap — decisions made, actions,
and the next session confirmed. That recap will go out within 24 hours.*

*Can we confirm dates for the remaining workshops now, or at least agree
a cadence?"*

**Facilitation notes**

- Most teams will want some level of support, especially for the scenario
modelling in Workshop 5. That is fine — just make sure the model is
agreed now.
- Do not oversell either delivery option. Present them neutrally and let
the team decide.
- If they cannot confirm dates today, agree a process for doing so within
the next 48 hours. Do not leave without a clear next step.

---

### Data sensitivity and minimum viable data (8 minutes)

**What you are doing**

Removing anxiety about data, naming what you need, and getting owners
against each item.

**Talk track**

*"We do not need perfect data to get started. Where we do not have exact
numbers we will use ranges and confidence ratings. The goal is decision
quality, not spreadsheet precision.*

*What I do need is a small set of inputs to get the baseline going. Let
me walk you through them and we can put a name against each one."*

Work through the minimum viable data list together:

| Data needed | Why we need it | Owner | How hard to get? |
|-------------|----------------|-------|-----------------|
| Cluster inventory | Defines scope — prevents gaps | | |
| Cloud billing exports (AWS CUR / Azure) | Source of truth for actual spend | | |
| Platform subscription overview | Separates fixed from variable cost | | |
| Tooling list | Identifies duplication across platforms | | |
| Platform ops effort estimate | Captures cost invoices do not show | | |
| Production app list or top 20 workloads | Grounds unit economics in reality | | |

For any item where sensitivity comes up:

*"If you would prefer to keep certain numbers internal, that is completely
fine. We can work with banded ranges, or you populate that part of the
model yourselves. The important thing is that the assumptions are recorded,
not that I see every figure."*

**Facilitation notes**

- Fill in the owner column in real time. Do not leave without a name
against every item, even if the answer is "TBC — [NAME] will confirm."
- If an item is genuinely not available, note it as a gap and agree
whether to estimate, exclude, or come back to it.
- Watch for the person who says "I can get that" about everything.
Gently check whether they actually own it or are just being helpful.
- The ops effort estimate is often the most uncomfortable item. Normalise
it early: *"Even a rough split is fine — upgrade work, patching,
incidents, onboarding. We are not auditing anyone's timesheet."*

---

### Ways of working and next steps (5 minutes)

**What you are doing**

Confirming the practical details so there is no ambiguity between sessions.

**Cover these four things:**

**Documents**
Confirm the shared workspace location. Make sure everyone knows where to
find and update artefacts between sessions. Open it in the session so
people can see it exists.

**Versioning**
*"Every document gets a version number and a date. The Assumptions Register
especially — because when Finance asks which version of the model you used,
you want a clear answer."*

**Comms**
*"After every workshop I will send a short recap — decisions made, actions,
and the next session confirmed. It will be one page or one email, no more."*

**Cadence**
Confirm dates or windows for Workshops 1 through 5. Even rough placeholders
are better than nothing — they signal commitment and maintain momentum.

---

### Close (3 minutes)

**What you are doing**

Summarising what was agreed and making the next step completely clear.

**Talk track**

*"Here is where we have landed. We have agreed scope shape, delivery model,
and who owns which data. I will send a recap within 24 hours with the
workshop plan, the shared workspace link, and the data request list with
names against each item.*

*Workshop 1 is [DATE/TIME] — that is where we lock in scope and rules
properly and start building the Assumptions Register together."*

Then ask one final question and mean it:

*"Is there anything we have not covered today that would make you feel
less confident going into this?"*

Listen carefully. If something comes up, address it directly.

---

## Handling difficult moments

### "Is this just a way to get us to renew or buy something?"

Do not get defensive. Be direct and calm.

*"That is a fair question and I would rather address it now than have it
sit in the background. The frameworks we are using are vendor-neutral —
FinOps, TBM, DORA, and SPACE are industry standards used across the
industry regardless of platform. The model will show what it shows. If a
particular option makes sense, the numbers will support it. If there are
better options for some workloads, we will say that too. The whole point
is that you end up with something you can defend, not something I have
steered."*

### Someone goes quiet or seems disengaged

Check in directly but gently.

*"I want to make sure this feels useful for everyone in the room.
Anything you would add or push back on?"*

### The data conversation gets complicated

Do not try to solve it in the room. Name the gap, assign an owner,
and move on.

*"Let us note that as a gap, put your name against it, and we will work
out the best approach before Workshop 2."*

### The scope starts expanding

Bring it back without making anyone feel shut down.

*"Let us capture that as a potential addition and park it for now. I want
to make sure we have agreed the core scope before we add to it."*

### Someone challenges the frameworks

*"These are not frameworks we invented — FinOps, TBM, DORA, and SPACE
are all widely used across the industry. We are using them because they
give us a common language with Finance and Procurement, not because they
favour any particular outcome."*

---

## Output checklist

Before you close the session, confirm these exist or are in progress:

- [ ] Workshop plan created — sessions 0 through 5, dates, attendees
- [ ] Scope draft written — one paragraph, agreed in the room
- [ ] Data owners list populated — names, items, due dates
- [ ] Shared workspace created and open
- [ ] Assumptions Register v0 created — even if empty
- [ ] Recap email drafted and ready to send within 24 hours

---

## Post-session actions (within 24 hours)

- [ ] Send recap email — decisions made, actions, next session confirmed
- [ ] Update Assumptions Register v0 with scope decisions from the session
- [ ] Share workshop plan with all attendees
- [ ] Confirm Workshop 1 date and send calendar invite
- [ ] Follow up individually with any data owners who seemed uncertain
