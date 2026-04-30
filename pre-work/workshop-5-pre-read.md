# Kubernetes Platform Economics Workshops
## Workshop 5 Pre-Read — Scenarios, Recommendation, and 90-Day Plan

**Session:** Workshop 5 — Scenarios, Recommendation, and 90-Day Plan
**Duration:** 3 hours
**Audience:** Product Owner, Platform Lead, Platform Engineers and SREs

---

## What this is

This document is your pre-read for Workshop 5. It takes around fifteen
minutes to read and is the most important pre-read of the series.

Workshop 5 is the final session. Everything we have built across four
workshops comes together here — cost baseline, unit economics, showback
view, and value scorecard — and we turn it into a decision and a plan.

---

## What we are doing in Workshop 5

By the end of this session we will have:

- A workload placement matrix — a structured view of which workloads
belong on which platform and why
- A scenario comparison — three to five realistic options evaluated on
cost, value, risk, and time to value
- A recommended path — with a clear rationale that leadership can defend
- A 90-day plan — no-regrets actions, decisions required, and pilots or
spikes to validate assumptions
- A decision brief outline — the structure of the exec-ready output that
goes to CIO, GM of Technology and Operations, Finance, and Procurement

---

## Where we have got to

Before Workshop 5, you should have received the following from the
previous sessions:

- **Cost baseline** — what the Kubernetes estate costs today across six
buckets, with a fixed versus variable split
- **Unit economics model** — three to five unit metrics with baseline
values and confidence ratings
- **Showback view** — cost mapped to teams, products, or namespaces
- **Value and risk scorecard** — eight to twelve measures across delivery
performance, reliability, security and compliance effort, and developer
experience

If any of these are incomplete or feel inaccurate, raise it at the
start of Workshop 5. A flawed input produces a flawed recommendation.

---

## The scenarios we will evaluate

We will evaluate four scenarios. These are not predictions — they are
structured options that let leadership compare trade-offs with numbers
attached. A fifth scenario can be added if something specific to your
environment warrants it.

### Scenario A — Optimise the current estate

What changes:
The current platform estate stays broadly as-is. We focus on improving
utilisation, reducing cluster sprawl, enforcing resource requests and
limits, improving autoscaling, and consolidating tooling where duplication
exists.

Why it matters:
This is the baseline for comparison. It shows what is achievable without
structural change — and sets a floor for how other scenarios need to
perform to justify their complexity.

### Scenario B — Consolidate workloads across platforms

What changes:
Workloads currently running on multiple platforms are selectively
consolidated. Duplication in tooling, policy enforcement, and operational
overhead is reduced. The platform estate becomes more intentional —
fewer platforms, clearer reasons for each.

Why it matters:
Running multiple Kubernetes platforms means multiple versions of
everything — observability, security controls, CI/CD patterns, runbooks,
upgrade cycles, and on-call coverage. That duplication has a real cost
that does not show up on a subscription invoice. Consolidation reduces it.

### Scenario C — Move some or all clusters to managed Kubernetes

What changes:
Selected clusters or workloads move to a managed Kubernetes offering.
The operational burden of managing control planes, upgrades, and
infrastructure shifts to the managed service. Platform team capacity
is redirected toward higher-value work.

Why it matters:
Managed Kubernetes can reduce operational toil significantly — particularly
around upgrades, patching, and control plane reliability. The infrastructure
cost may be similar or slightly higher, but the reduction in operating
effort can more than offset it. This scenario is worth modelling honestly.

### Scenario D — Hybrid portfolio

What changes:
The estate is deliberately structured as a portfolio of platforms. Some
workloads remain on self-managed Kubernetes where there is a clear,
quantified reason — tight coupling to cloud-native services, specific
performance requirements, or regulatory constraints. The rest are
consolidated to reduce duplication and improve unit economics.

Why it matters:
This is often the most realistic outcome — not all-in on one platform,
but deliberate about which exceptions are justified and why. The
workload placement matrix we build in Workshop 5 is the tool that
makes this defensible.

---

## The workload placement matrix

Before we compare scenarios we will build a workload placement matrix —
a structured view of which workloads belong on which platform, based on
agreed criteria rather than habit or history.

The criteria we use:

| Criterion | What we are asking |
|-----------|-------------------|
| Compliance and policy intensity | How much policy enforcement and audit evidence does this workload require? |
| Cloud-native coupling | How tightly is this workload coupled to cloud-provider-specific services? |
| Operational burden | How much day-two operational effort does this workload generate? |
| Portability need | Does this workload need to move between platforms or clouds? |
| Migration complexity | How difficult and risky would it be to move this workload? |
| Data gravity and latency | Are there performance or data residency constraints that pin this workload? |

We will apply these criteria to ten to twenty meaningful workloads.
The output tells us which workloads are good candidates for consolidation
or migration and which are justified exceptions.

---

## How we compare scenarios

For each scenario we will assess four dimensions:

**Cost impact**
We distinguish between four types of cost change:
- Hard savings — actual spend reduction
- Cost avoidance — growth that does not happen
- Capacity release — using what you already pay for more efficiently
- Toil reduction — operational time returned to higher-value work

**Value and risk impact**
We assess each scenario against the value scorecard from Workshop 4.
Does it improve delivery performance? Does it reduce operational risk?
Does it improve or worsen developer experience?

**Time to value**
How long before the scenario delivers its benefits? Quick wins versus
structural changes have very different timelines.

**Dependencies and constraints**
What needs to be true for this scenario to work? What are the risks
if those dependencies are not met?

---

## The 90-day plan

The final output of Workshop 5 is a 90-day plan — a practical set of
actions that leadership can approve and the team can execute.

It is structured into three tracks:

**No-regrets actions**
Things that improve the situation regardless of which scenario is chosen.
These can start immediately. Examples include rightsizing, enforcing
resource requests and limits, retiring unused clusters, and improving
tagging for better cost allocation.

**Decisions required**
Questions that leadership needs to answer before the preferred scenario
can be fully committed to. These are surfaced clearly — not buried in
the appendix.

**Pilots and spikes**
Short, time-boxed investigations to validate key assumptions before
committing to a structural change. A managed Kubernetes viability spike,
for example, or a consolidation pilot for a small set of workloads.

---

## What to bring to Workshop 5

Having thought through the following before the session will make the
scenario discussion more productive:

- Are there any scenarios you would rule out immediately — and why?
- Are there workloads you know are good consolidation candidates?
- Are there workloads that have hard constraints keeping them where
they are?
- What decisions does leadership need to make — and when?
- Are there any contract, renewal, or compliance timelines that affect
the sequencing of actions?

---

## What you will have at the end of Workshop 5

- A workload placement matrix — structured and agreed
- A scenario comparison — evaluated on cost, value, risk, and time
- A recommendation — with a rationale that is defensible
- A 90-day plan — no-regrets actions, decisions, pilots
- A decision brief outline — ready to populate for the exec audience

---

## Questions before we meet?

If anything in this pre-read raises questions, get in touch with
[FACILITATOR] before the session.

See you on [DATE] at [TIME].

---

## Glossary

| Term | Plain English |
|------|---------------|
| Scenario | A structured option for how the platform estate could be organised |
| Workload placement matrix | A structured view of which workloads belong on which platform and why |
| Hard savings | Actual reduction in spend |
| Cost avoidance | Future spend growth that does not happen |
| Capacity release | Using what you already pay for more efficiently |
| Toil reduction | Operational time returned to higher-value work |
| No-regrets actions | Improvements that make sense regardless of which scenario is chosen |
| Spike | A short, time-boxed investigation to validate a key assumption |
| Pilot | A small-scale implementation to test a scenario before committing |
| Decision brief | The exec-ready output that goes to leadership, Finance, and Procurement |
| Cloud-native coupling | Tight dependency on services specific to one cloud provider |
| Data gravity | Performance or data residency constraints that pin workloads to a location |
| Control plane | The management layer of a Kubernetes cluster |
| Managed Kubernetes | A Kubernetes offering where the cloud provider manages the control plane |
