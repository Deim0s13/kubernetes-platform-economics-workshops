# Kubernetes Platform Economics Workshops
## Workshop 3 Pre-Read — Allocation Rules and Unit Economics

**Session:** Workshop 3 — Allocation Rules and Unit Economics
**Duration:** 2 hours
**Audience:** Product Owner, Platform Lead, Platform Engineers and SREs

---

## What this is

This document is your pre-read for Workshop 3. It takes around ten minutes
to read and will make the session more productive for everyone in the room.

Workshop 3 is where we move from total cost to unit economics — translating
the baseline we built in Workshop 2 into cost per useful outcome. By the end
of this session we will have a set of unit metrics that leadership, Finance,
and Procurement can actually act on.

---

## What we are doing in Workshop 3

By the end of this session we will have:

- Agreed allocation rules — how shared costs are distributed across
platforms, teams, and workloads
- A populated unit economics model — three to five unit metrics with
baseline values
- A showback view — cost mapped to teams, products, or namespaces
- An updated Assumptions Register — reflecting every allocation decision
made today
- A clear sense of what the numbers mean and what decisions they enable

---

## From total cost to unit economics — why it matters

In Workshop 2 we built a cost baseline. We know — at least roughly —
what the Kubernetes estate costs in total across the six buckets.

But total cost is a number that is hard to act on. When a CIO or CFO
asks "is this platform good value?" the answer cannot be "it costs X."
The answer needs to be something like:

- "A production application costs Y per month to run on this platform."
- "Each tenant costs Z per quarter."
- "We pay for capacity but only use A% of it effectively."

Those are unit economics. They connect cost to something the business
recognises — an application, a team, a deployment, a unit of capacity.
That connection is what makes the output actionable rather than
just informative.

---

## What allocation rules are — and why we need them

Before we can calculate unit economics we need to agree how to distribute
shared costs across the things we are measuring.

Some costs are straightforward to attribute — a node pool running a
specific workload, a subscription that serves one platform. Others are
genuinely shared — an observability stack that serves three platforms,
a network platform that serves the whole estate.

Allocation rules are the agreed method for distributing those shared
costs fairly and consistently. They do not need to be perfect — they
need to be agreed, documented, and applied consistently so that the
output is comparable and defensible.

We use a showback-first approach. That means we make costs visible
to teams and products before we start billing anyone for them. Showback
builds transparency and reduces the political friction that comes with
chargeback.

---

## The unit metrics we shortlisted in Workshop 1

In Workshop 1 we agreed a shortlist of three to five unit metrics.
Workshop 3 is where we bring those to life with actual numbers.

Here is a reminder of the menu we worked from — the shortlist your
team selected is in the attendee materials:

| Unit metric | What it tells you |
|-------------|-------------------|
| Cost per production app per month | What it costs to run one app in production |
| Cost per tenant or namespace per month | What it costs to serve one team or product |
| Cost per environment | Prod versus non-prod cost split |
| Effective cost per vCPU-hour used | How efficiently purchased capacity is being used |
| Ops cost per cluster per month | The operational overhead of each cluster |
| Cost per deployment or release | What it costs to ship a change |

Each unit metric has four components we will define properly in the
session:

- **Numerator** — which costs are included in the calculation
- **Denominator** — what we are dividing by (app count, tenant count,
vCPU hours, and so on)
- **Data sources** — where the numbers come from
- **Confidence rating** — how certain we are about the result

---

## A note on utilisation

One of the most revealing unit metrics is effective cost per vCPU-hour
used — not purchased or allocated, but actually used.

Most Kubernetes estates have a meaningful gap between what they pay for
and what they actually consume. That gap — called the utilisation gap —
is often where the most straightforward cost improvements sit.

To calculate this metric we need utilisation data — CPU and memory
requests versus actual consumption. If this data is available from your
monitoring platform, it is worth having it to hand before Workshop 3.

---

## What to bring to Workshop 3

- Any outstanding data from the Workshop 2 gaps list — particularly
namespace or team mappings and utilisation data
- A rough count of production applications across the estate
- Any existing showback or chargeback reports, even partial ones
- The Workshop 1 unit metrics shortlist — this is in your attendee
materials from Workshop 1

---

## What you will have at the end of Workshop 3

- Agreed allocation rules — documented in the Assumptions Register
- A unit economics model with baseline values for three to five metrics
- A showback view — cost mapped to teams, products, or namespaces
- A clear narrative — "what does the platform cost per useful outcome?"
- A foundation for the scenario modelling in Workshop 5

---

## Questions before we meet?

If anything in this pre-read raises questions, get in touch with
[FACILITATOR] before the session.

See you on [DATE] at [TIME].

---

## Glossary

| Term | Plain English |
|------|---------------|
| Unit economics | Cost per useful outcome — e.g. cost per app per month |
| Allocation rules | The agreed method for distributing shared costs |
| Showback | Making costs visible to teams without billing them |
| Chargeback | Billing teams directly for their platform usage |
| Numerator | The cost included in a unit metric calculation |
| Denominator | What you divide by — app count, tenant count, vCPU hours |
| Utilisation gap | The difference between capacity purchased and capacity used |
| Namespace | A Kubernetes construct for grouping and isolating workloads |
| Tenant | A team or product that uses a shared platform |
| Confidence rating | H = measured, M = estimated, L = rough guess |
| Assumptions Register | A versioned log of every scope and cost treatment decision |
| Showback view | A report showing what each team or product is spending |
