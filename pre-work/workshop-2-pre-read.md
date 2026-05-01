# Kubernetes Platform Economics Workshops
## Workshop 2 Pre-Read — Cost Taxonomy and Baseline Model

**Session:** Workshop 2 — Cost Taxonomy and Baseline Model  
**Duration:** 2 hours  
**Audience:** Product Owner, Platform Lead, Platform Engineers and SREs  

---

## What this is

This document is your pre-read for Workshop 2. It takes around ten minutes to read and will make the session more productive for everyone in the room.

Workshop 2 is where we start building the cost model. By the end of this session, we will have a cost taxonomy agreed and a baseline model skeleton populated with the data that has come in so far.

---

## What we are doing in Workshop 2

By the end of this session, we will have:

- A cost taxonomy, a structured way of grouping spend that Finance and IT can both work from
- A baseline model skeleton with known spend mapped in and gaps identified
- A clear view of which cost buckets are well understood and which need more data
- An updated data gaps list with owners and revised due dates where needed
- An initial view of fixed versus variable costs across the estate

---

## What a cost taxonomy is — and why it matters

A cost taxonomy is simply a structured way of grouping technology costs into categories that are consistent, comparable, and recognisable to Finance and Procurement.

Without one, platform cost ends up scattered across invoices, cloud bills, team budgets, and people's heads. The taxonomy brings it together into a single structure so that:

- IT and Finance are working from the same categories.
- Costs can be compared across platforms and over time.
- The output is auditable; every number has a home and a source.

We build ours using TBM (Technology Business Management) as the reference framework. TBM is a widely used industry standard for technology cost classification. It gives us a language that Finance will recognise without requiring anyone to become a TBM expert.

---

## The cost taxonomy we will use

We organise platform costs into six buckets. Every cost in scope sits in one of these.

### Cloud infrastructure

The raw compute, storage, and network costs that underpin the platforms.

Examples:
- Virtual machines and node pools (compute)
- Block storage and object storage (storage)
- Load balancers, NAT gateways, and data egress (network)

### Managed service fees

Fees charged by cloud providers for managed Kubernetes services, where applicable.

Examples:
- EKS cluster management fees
- AKS management fees
- Any equivalent managed control plane charges

### Platform tooling

The software and services that make the platforms operational, beyond raw infrastructure.

Examples:
- Observability (monitoring, logging, alerting)
- Security scanning and policy enforcement
- CI/CD tooling
- Backup and disaster recovery

### Subscriptions

Platform licences, support agreements, and any recurring software fees.

Examples:
- Platform licence fees
- Enterprise support agreements
- Any SaaS tooling subscriptions that serve the platform

### Operating effort

The time your platform team spends running, maintaining, and improving the platforms. This is often the highest hidden cost, and the one most commonly left out of cost reviews.

Examples:
- Upgrade and patching cycles
- Incident response and on-call
- Onboarding new teams and workloads
- Building and maintaining golden paths and standards

We capture this as an estimate — a rough time split across activities is enough to put a number on it.

### Shared services

Costs that sit beneath the platforms and serve them without being attributable to any one platform.

Examples:
- Identity and access management (IAM)
- Shared network infrastructure
- Shared logging or audit platforms
- Centralised certificate management

---

## Fixed versus variable costs

As we populate the baseline, we will distinguish between fixed and variable costs. This matters because they behave differently and require
different levers to change.

**Fixed costs** do not change with usage in the short term. A platform subscription fee is the same whether you run ten workloads or a hundred. Reducing fixed costs requires structural change, renegotiating contracts, consolidating platforms, or moving to a different model.

**Variable costs** scale with usage. Compute consumption, storage, and data egress go up and down with demand. Reducing variable costs requires operational changes — rightsizing, autoscaling, better utilisation, or workload consolidation.

Understanding the split helps us identify which levers are available and how quickly they can be pulled.

---

## What to bring to Workshop 2

If you have actioned your data request items from Workshop 1, please share them before the session if you can. Even partial data is useful.

It would particularly help to have:

- **Cloud billing exports** — AWS Cost and Usage Report (CUR) or Azure cost export, even for a single month
- **Tooling list** — what sits across your platforms and roughly what it costs
- **Subscription details** — platform licences or support agreements in scope
- **A rough cluster inventory** — platforms, environments, approximate node counts

If some items are not ready yet, do not worry. We will map what we have, identify the gaps, and agree on how to fill them.

---

## A note on data quality

You will not have perfect data at this stage. That is expected and completely fine.

We use confidence ratings throughout — High, Medium, or Low — to be honest about what is measured versus estimated. A baseline with clear confidence ratings is more trustworthy than one that pretends every number is exact.

Where data is missing, we use one of three approaches:

- **Estimate with a low confidence rating** — the most common approach
- **Range** — when even an estimate feels too speculative
- **Gap** — when we genuinely have no basis for an estimate

Every gap is noted in the Assumptions Register with an owner and a plan to close it.

---

## What you will have at the end of Workshop 2

- A cost taxonomy — the structure every subsequent workshop builds on
- A baseline model skeleton — known spend mapped in, gaps identified.
- A fixed versus variable cost split — even if partial at this stage
- An updated data gaps list — with owners and revised due dates
- A clear sense of where spending concentrates and where we need more data

---

## Questions before we meet?

If anything in this pre-read raises questions, get in touch with [FACILITATOR] before the session.

See you on [DATE] at [TIME].

---

## Glossary

| Term | Plain English |
|------|---------------|
| Cost taxonomy | A structured way of grouping technology costs into consistent categories |
| TBM | Technology Business Management — a standard cost classification framework |
| Fixed cost | A cost that does not change with usage in the short term |
| Variable cost | A cost that scales with usage |
| Baseline | The current state — what things cost today before any changes |
| Cost pool | A grouping of similar costs — e.g. cloud compute, people effort |
| Confidence rating | High, Medium, or Low — how certain we are about a figure |
| Assumptions Register | A versioned log of every scope and cost treatment decision |
| Data egress | The cost of moving data out of a cloud provider |
| Node pool | A group of virtual machines that run workloads in a Kubernetes cluster |
| Operating effort | The time a platform team spends running and maintaining the platforms |
| Shared services | Costs that serve multiple platforms or teams without clean attribution |
