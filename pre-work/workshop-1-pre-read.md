# Kubernetes Platform Economics Workshops
## Workshop 1 Pre-Read — Scope, Glossary, and Rules of the Game

**Session:** Workshop 1 — Scope, Glossary, and Rules of the Game  
**Duration:** 90 minutes  
**Audience:** Product Owner, Platform Lead, Platform Engineers and SREs  

---

## What this is

This document is your pre-read for Workshop 1. It takes around ten minutes
to read and will make the session more useful for everyone in the room.

Workshop 1 is where the real work begins. We are going to agree the scope
of the assessment — what we are looking at, how we will treat costs, and
what the rules of the game are. Getting this right early means everything
that follows is built on a solid, trusted foundation.

---

## What we are doing in Workshop 1

By the end of this session we will have agreed:

- **Scope** — which platforms, environments, and cost types are included
- **Time window** — the reporting period we are working with
- **Cost treatment rules** — how we handle shared costs, non-production
environments, and anything that sits across multiple platforms
- **Unit metrics shortlist** — the three to five measures we will use to
report cost per outcome
- **Data owners** — who provides which inputs and by when
- **Assumptions Register v1** — a versioned record of every decision we
make about scope and cost treatment

---

## Why this matters

Most cost debates do not come from bad data. They come from hidden
assumptions — what is included, what is shared, what gets allocated, and
what counts as platform cost versus workload cost.

The Assumptions Register we build in this session fixes that. It makes
every decision explicit and agreed, so the outputs are trusted rather
than argued over.

---

## The key concepts for this session

### Cost scope

When we talk about platform cost we mean more than the subscription or
the cloud bill. A complete picture includes:

- **Cloud infrastructure** — compute, storage, network, and egress across
all platforms
- **Managed service fees** — charges for managed Kubernetes services where
applicable
- **Platform tooling** — observability, security scanning, CI/CD, backup,
and disaster recovery
- **Subscriptions** — any platform licences or support agreements
- **Operating effort** — the time your team spends running, maintaining,
and improving the platforms

Some of these are easy to find on an invoice. Others — particularly
operating effort — require an estimate. Both matter, and we will handle
both with appropriate confidence ratings.

### Shared costs

Some costs serve multiple platforms or teams and cannot be cleanly
attributed to one place. We handle these with agreed allocation rules
rather than ignoring them or arguing about them.

In Workshop 1 we will agree a simple approach — showback first, meaning
we make costs visible before we start billing anyone for them.

### Unit economics

Total spend is a number. Unit economics is what that number means.

Instead of "we spend X on Kubernetes" we want to be able to say "a
production application costs Y per month" or "each tenant costs Z per
quarter." That is the kind of number leadership, Finance, and Procurement
can act on.

We will shortlist the unit metrics that make sense for your environment
in this session and define them properly in Workshop 3.

### The Assumptions Register

Every decision we make about scope, cost treatment, and allocation goes
into a versioned Assumptions Register. This is not bureaucracy — it is
what makes the final output defensible.

When Finance asks "how did you treat shared tooling costs?" the answer
is in the Assumptions Register, with a date and a version number.

---

## What to bring to Workshop 1

Nothing needs to be formal or complete. Having a rough sense of the
following will make the session more productive:

- **Cluster inventory** — platforms, environments, approximate counts.
Even a rough list is fine.
- **Cloud billing owners** — who in your team can access AWS Cost and
Usage Reports and Azure cost exports
- **Tooling landscape** — what sits across your platforms for
observability, security, CI/CD, and backup
- **Subscription overview** — a high-level sense of what platform
licences or agreements are in place
- **Known pain points** — anything that feels expensive, duplicated,
or harder than it should be

If you do not have all of this, do not worry. We will work through it
together in the session.

---

## The data we will need (and why)

This table gives you a head start on identifying who owns what. We will
confirm owners and due dates together in the session.

| Data needed | Why we need it | Likely owner |
|-------------|----------------|--------------|
| Cluster inventory | Defines scope — prevents gaps | Platform Lead |
| Cloud billing exports (AWS CUR / Azure) | Source of truth for actual spend | Cloud or FinOps team |
| Platform subscription details | Separates fixed from variable cost | Platform Lead or Procurement |
| Tooling list | Identifies duplication across platforms | Platform Lead |
| Ops effort estimate (rough) | Captures cost invoices do not show | Platform Lead or SRE Lead |
| Production app list or top 20 workloads | Grounds unit economics in reality | Product Owner or Platform Lead |

---

## What you will have at the end of Workshop 1

- A written scope statement — what is in, what is out, and why
- Assumptions Register v1 — every scope and cost treatment decision,
versioned and agreed
- A unit metrics shortlist — the three to five measures we will report in
- A data request list with named owners and due dates
- A list of the decisions leadership will need to make at the end of all
five workshops

---

## A note on confidence ratings

We will not always have perfect data. That is normal and expected.

Throughout this work we use confidence ratings — High, Medium, or Low —
against every figure and assumption. This does two things: it keeps us
honest about what we know versus what we are estimating, and it prevents
the kind of "spreadsheet wars" where people argue about precision instead
of decisions.

If you are not sure about a number, say so. We will rate it Low
confidence, note the assumption we are making, and move on. The goal is
decision quality, not false precision.

---

## Questions before we meet?

If anything in this pre-read raises questions, get in touch with
[FACILITATOR] before the session.

See you on [DATE] at [TIME].

---

## Glossary

| Term | Plain English |
|------|---------------|
| Scope | What is included in the assessment and what is not |
| Cost allocation | Distributing shared costs across teams or products |
| Showback | Making costs visible to teams without billing them |
| Chargeback | Billing teams directly for their platform usage |
| Unit economics | Cost per useful outcome — e.g. cost per app per month |
| Assumptions Register | A versioned log of every scope and cost treatment decision |
| Confidence rating | High, Medium, or Low — how certain we are about a figure |
| Baseline | The current state — what things cost today before any changes |
| Unit metric | A single agreed measure of cost per outcome |
| FinOps | A way for engineering and finance to manage platform costs together |
| TBM | A standard cost classification structure for technology spend |
| DORA | Four metrics for measuring software delivery performance |
| SPACE | A framework for measuring developer productivity |
