# Kubernetes Platform Economics Workshops
## Workshop 0 Pre-Read — Setup and Expectations

**Session:** Workshop 0 — Setup and Expectations
**Duration:** 35–45 minutes
**Audience:** Product Owner, Platform Lead, Platform Engineers and SREs

---

## What this is

This document is your pre-read for Workshop 0. It takes about ten minutes to
read and will make our first session more useful for everyone in the room.

You do not need to prepare anything or bring any data to this session. That
comes later. This is simply about making sure we all start from the same
place.

---

## What we are doing and why

Recent commercial changes and broader cost pressures make it sensible to take
a structured look at platform economics. Not to re-argue platform decisions,
but to answer three practical questions with evidence:

1. What does our Kubernetes estate actually cost today — across platforms,
tooling, and operating effort?
2. What value is the platform enabling for teams and the business?
3. What options do we have to improve cost per outcome without increasing
risk?

The way we answer those questions is through a short series of five workshops.
Each one builds on the last. Together they produce a clear, trusted view that
is credible with technology leadership, Finance, and Procurement.

---

## What this is not

It is worth being clear about what this is not, because it shapes how we
approach the work.

**It is not a cost-cutting exercise.**
We are measuring cost and value together. Reducing cost at the expense of
delivery speed, reliability, or control is not the goal.

**It is not a vendor exercise.**
The frameworks we use are industry standards — FinOps, TBM, DORA, and SPACE.
None of them are proprietary. The conclusions will follow the evidence.

**It is not a foregone conclusion.**
We are not arriving with a predetermined answer. We are building a shared
fact base and then working out what it means together.

---

## The five workshops at a glance

| Workshop | Title | Duration |
|----------|-------|----------|
| 0 | Setup and Expectations | 35–45 minutes |
| 1 | Scope, Glossary, and Rules of the Game | 90 minutes |
| 2 | Cost Taxonomy and Baseline Model | 2 hours |
| 3 | Allocation Rules and Unit Economics | 2 hours |
| 4 | Value and Risk Scorecard | 90 minutes |
| 5 | Scenarios, Recommendation, and 90-Day Plan | 3 hours |

Each workshop has a clear purpose, a defined output, and a facilitator guide.
You will receive a short pre-read before each session so you always know what
to expect.

---

## What Workshop 0 is for

Workshop 0 is a setup session. It is shorter and lighter than the workshops
that follow. We are not building anything yet — we are making sure the
foundations are right before we do.

By the end of Workshop 0 we will have agreed:

- **Scope shape** — which platforms and environments we are looking at, and
what time window we are working with
- **Delivery model** — whether your team runs the workshops using our
toolkit, or whether we facilitate together
- **Data owners** — who in your team owns which inputs, so we can request
the right things from the right people
- **Ways of working** — where documents live, how we handle version control,
and how we communicate between sessions
- **Minimum viable data** — the small set of inputs we need to get started,
and a realistic plan for getting them

---

## The frameworks we use (plain English)

You do not need prior knowledge of these. Here is what they are and why they
matter for this work.

**FinOps**
A practical way for engineering, finance, and the business to work together
on cost visibility and optimisation. We use it to move from "what do we
spend?" to "what do we spend per outcome?" — a concept called unit economics.

**TBM — Technology Business Management**
A standard way of classifying technology costs so that IT and Finance can
report and decide using the same language. It stops debates about what counts
as a platform cost versus a workload cost.

**DORA**
Four metrics that tell you how well your software delivery pipeline is
performing: deployment frequency, lead time for changes, change failure rate,
and time to restore service. We use these to make platform value visible to
leadership.

**SPACE**
A broader way of thinking about developer productivity across five areas:
Satisfaction, Performance, Activity, Communication and collaboration,
Efficiency and flow. It prevents the conversation from becoming purely about
cost.

---

## What to bring to Workshop 0

Nothing formal. But it would help to have a rough sense of:

- Which Kubernetes platforms your organisation runs and roughly how many
clusters
- Who in your team owns cloud billing (AWS or Azure)
- Who owns the platform subscription details
- Any known pain points — things that slow the team down or create
unnecessary overhead

If you do not have all of this off the top of your head, do not worry. We
will work through it together in the session.

---

## A note on data sensitivity

We know that cost data can be sensitive. Here is how we handle that:

- Where exact numbers are not available or cannot be shared, we use ranges
and confidence ratings
- You always own the numbers — we help you interpret and structure them
- If you prefer to keep certain figures internal, we can work with
driver-based modelling instead
- Nothing leaves the working sessions without your sign-off

The goal is decision quality, not spreadsheet precision.

---

## What you will have at the end of all five workshops

A short decision brief — written for technology leadership, Finance, and
Procurement — that clearly shows:

- What you spend, what drives it, and how confident you are in the numbers
- Cost per outcome across your Kubernetes estate
- Value and risk considerations alongside the cost picture
- Realistic options and the trade-offs between them
- A 90-day plan that is practical and actionable

---

## Questions before we meet?

If anything in this pre-read raises questions, get in touch with [FACILITATOR]
before the session. Better to address them early than carry uncertainty into
the work.

See you on [DATE] at [TIME].

---

## Glossary

| Term | Plain English |
|------|---------------|
| FinOps | A way for engineering and finance to manage cloud and platform costs together |
| TBM | A standard cost classification structure for technology spend |
| Unit economics | Cost per useful outcome — e.g. cost per app per month |
| DORA | Four metrics for measuring software delivery performance |
| SPACE | A framework for measuring developer productivity |
| Showback | Showing teams what they spend without billing them for it |
| Chargeback | Billing teams directly for their platform usage |
| Cost allocation | Distributing shared costs across teams or products |
| Baseline | The current state — what things cost today before any changes |
| Unit metric | A single measure of cost per outcome, agreed and defined |
| Assumptions register | A versioned log of every decision made about scope and cost treatment |
| Decision brief | The final output — options and recommendation for leadership |
