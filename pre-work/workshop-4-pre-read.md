# Kubernetes Platform Economics Workshops
## Workshop 4 Pre-Read — Value and Risk Scorecard

**Session:** Workshop 4 — Value and Risk Scorecard
**Duration:** 90 minutes
**Audience:** Product Owner, Platform Lead, Platform Engineers and SREs

---

## What this is

This document is your pre-read for Workshop 4. It takes around ten minutes to read and will make the session more productive for everyone in the room.

Workshop 4 is where we look at the other side of the equation. We have spent three workshops building a clear picture of what the platform costs. Today, we build a picture of what it enables, and what we would risk losing if cost decisions were made without considering value.

---

## What we are doing in Workshop 4

By the end of this session, we will have:

- A value and risk scorecard has eight to twelve measures that capture what the platform delivers and what it protects.
- Baseline values for each measure using real data where available, and agreed proxies where they are not
- Target directions, where we want each measure to move and why
- A clear narrative, “here is what the platform enables, and here is what we would risk if we optimised cost without considering this”

---

## Why a value scorecard — not just a cost model

Cost without value is an incomplete picture. A platform that appears expensive in the cost model may deliver significant returns in terms of delivery speed, reliability, security posture, and developer productivity. Conversely, a platform that looks cheap may be hiding costs in incidents, audit failures, and team friction.

The scorecard exists for two reasons:

**First, it protects good decisions.** When leadership sees cost per app alongside lead time and incident rate, they can make a genuinely informed decision. When they only see cost, they optimise in one dimension and often shift the cost to a less visible place.

**Second, it makes platform value tangible.** Platform teams often struggle to articulate value in terms that leadership recognises. "We keep the lights on" is not a conversation that lands in a boardroom. "We reduced mean time to restore by 40% and increased deployment frequency by 3x"
is.

---

## The frameworks we use

### DORA — software delivery performance

DORA (DevOps Research and Assessment) is one of the most widely used frameworks for measuring software delivery performance. It uses four metrics:

**Deployment frequency**
How often is code successfully deployed to production? Higher frequency signals a healthy, low-friction delivery pipeline.

**Lead time for changes**
The time from code commit to running in production. Shorter lead time signals faster, lower-risk delivery.

**Change failure rate**
The percentage of deployments that cause a failure in production. Lower is better; it signals quality and stability.

**Time to restore service**
How long does it take to recover from a production incident? Shorter recovery time signals good observability and operational maturity.

### SPACE — developer productivity

SPACE is a framework developed by researchers at Microsoft and GitHub for thinking about developer productivity across five dimensions:

**Satisfaction and wellbeing**
How developers feel about their work, tools, and environment.

**Performance**
The outcomes of developer work are quality, reliability, and impact.

**Activity**
The volume of actions, outputs, deployments, pull requests, and reviews.

**Communication and collaboration**
How well teams work together and share knowledge.

**Efficiency and flow**
How smoothly work moves through the system, with minimal interruption, minimal toil.

We do not need to formally measure all five dimensions. SPACE gives us a framework for thinking beyond a single productivity metric and avoiding the trap of measuring only what is easy to count.

---

## The four scorecard categories

We organise the scorecard into four categories that connect DORA and SPACE to the platform reality:

### Delivery performance

How effectively the platform enables teams to ship changes safely and quickly.

Measures include deployment frequency, change lead time, and change failure rate, drawn from DORA.

### Reliability

How stable the platform is and how quickly it recovers when things go wrong.

Measures include time to restore service, incident volume, and availability, drawn from DORA and platform operations data.

### Security and compliance effort

How much effort does the platform require to meet security and compliance obligations, and how much does it reduce that effort compared to alternatives?

Measures include time to patch critical vulnerabilities, policy coverage, and the effort required to generate audit evidence.

### Developer experience

How much friction developers experience when building and deploying on the platform.

Measures include onboarding time for new services or teams, time to first deployment, and ticket or toil volume, drawn from SPACE.

---

## A note on proxies

Not every organisation has formal DORA metrics in place. That is fine.

For each measure, we will agree on a proxy if the direct measurement is not available. A proxy is an imperfect but directionally useful substitute that gives us a baseline to work from.

For example:
- If deployment frequency is not tracked formally, release cadence per team is a reasonable proxy.
- If MTTR is not tracked, average incident duration from on-call logs is a reasonable proxy.
- If onboarding time is not tracked, a rough estimate from the platform team is enough to start.

The goal is not precision. It is direction. We want to know whether things are getting better or worse, and whether platform decisions are helping or hurting.

---

## What to bring to Workshop 4

Having a rough sense of the following will make the session more productive:

- **Deployment frequency:** how often teams deploy to production, even a rough estimate per team or service
- **Lead time:** from code ready to running in production
- **Incident data:** volume and rough recovery times for the last quarter
- **Security signals:** time to patch critical vulnerabilities, any recent audit findings related to the platform
- **Developer experience signals:** onboarding time, known friction points, any team satisfaction data, even if informal.

Nothing needs to be precise. Rough is fine. We will agree on confidence ratings and proxies in the session.

---

## What you will have at the end of Workshop 4

- A value and risk scorecard — eight to twelve measures, baselined and directionally targeted
- Agreed proxies where direct measurement is not available
- A narrative that connects platform cost to platform value — ready to sit alongside the unit economics model in the final decision brief - A foundation for the scenario modelling in Workshop 5 — so scenarios are evaluated on cost and value, not cost alone

---

## Questions before we meet?

If anything in this pre-read raises questions, get in touch with [FACILITATOR] before the session.

See you on [DATE] at [TIME].

---

## Glossary

| Term | Plain English |
|------|---------------|
| DORA | DevOps Research and Assessment — four metrics for software delivery performance |
| SPACE | A framework for developer productivity across five dimensions |
| Deployment frequency | How often code is successfully deployed to production |
| Lead time for changes | Time from code commit to running in production |
| Change failure rate | Percentage of deployments that cause a production failure |
| Time to restore service | How long it takes to recover from a production incident |
| MTTR | Mean Time to Restore — average recovery time from incidents |
| Proxy | An imperfect but directionally useful substitute for a direct measurement |
| Scorecard | A structured set of agreed measures with baseline and target values |
| Toil | Repetitive, manual, automatable work that does not add long-term value |
| Golden path | A recommended, supported way of building and deploying on a platform |
| Policy coverage | The percentage of workloads governed by automated policy controls |
