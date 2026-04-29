# Kubernetes Platform Economics Workshops

A practical, vendor-neutral playbook for running platform economics workshops
across any Kubernetes estate.

---

## What this is

This repository contains everything you need to run a structured series of
workshops that help an organisation answer three questions with evidence:

1. What does our Kubernetes platform estate cost today?
2. What value does it create for teams and the business?
3. What changes would improve cost per outcome without increasing risk?

The work is structured as five workshops, each building on the last, and
produces a decision brief that technology leadership, Finance, and Procurement
can act on with confidence.

---

## What this is not

This is not a vendor exercise. It is not a cost-cutting programme. It is not
a pre-determined recommendation dressed up as analysis.

It is a structured way to build a shared, trusted fact base — using recognised
industry frameworks — so that platform decisions are made on evidence rather
than assumption or commercial pressure.

---

## The frameworks we use

The workshops are anchored to four industry-standard frameworks. None of them
are vendor-specific.

**FinOps**
A practical operating model for connecting technical decisions to financial
outcomes. We use it for cost visibility, allocation rules, and unit economics.
[FinOps Foundation](https://www.finops.org)

**TBM (Technology Business Management)**
A standard taxonomy for classifying and reporting technology costs so that IT
and Finance can work from the same structure.
[TBM Council](https://www.tbmcouncil.org)

**DORA**
Four metrics that measure software delivery performance and operational
stability: deployment frequency, lead time for changes, change failure rate,
and time to restore service.
[DORA](https://dora.dev)

**SPACE**
A framework for understanding developer productivity across five dimensions:
Satisfaction, Performance, Activity, Communication and collaboration,
Efficiency and flow.
[SPACE framework](https://queue.acm.org/detail.cfm?id=3454124)

---

## The narrative

Every workshop, every template, and every output in this playbook serves one
story:

*Before making any platform decisions, let's find out what's actually true.*

That plays out in five beats:

1. **Get honest about scope** — what are we actually looking at, and what
rules are we playing by?
2. **Follow the money** — where does spend go, and what is driving it?
3. **Put a price on outcomes** — what does the platform cost per useful thing
it delivers?
4. **Measure what matters** — is the platform actually performing, and would
we know if it was not?
5. **Make a decision** — here are your options, with numbers and trade-offs,
and here is what to do next.

---

## The workshops

| Workshop | Title | Duration |
|----------|-------|----------|
| 0 | Setup and Expectations | 35–45 minutes |
| 1 | Scope, Glossary, and Rules of the Game | 90 minutes |
| 2 | Cost Taxonomy and Baseline Model | 2 hours |
| 3 | Allocation Rules and Unit Economics | 2 hours |
| 4 | Value and Risk Scorecard | 90 minutes |
| 5 | Scenarios, Recommendation, and 90-Day Plan | 3 hours |

---

## What each workshop folder contains

Each workshop folder contains three files:

**`facilitator-guide.md`**
The full playbook and facilitation notes for the person running the session.
Covers purpose, agenda, talk tracks, facilitation tips, and output checklist.

**`slides.md`**
Every slide written out with title, content, layout note, and speaker notes.
Use this as the source of truth when building your presentation deck.

**`attendee-materials.md`**
Everything the attendees need — pre-work, completion sheets, reference
content, and a short glossary for the session.

---

## Templates

The `templates/` folder contains reusable working documents that are
introduced and populated across the workshops:

| Template | Used in |
|----------|---------|
| `assumptions-register.md` | Workshop 1 onwards |
| `data-request-list.md` | Workshop 0 and 1 |
| `cost-taxonomy.md` | Workshop 2 |
| `unit-metrics-definition.md` | Workshop 3 |
| `scenario-comparison.md` | Workshop 5 |
| `workload-placement-matrix.md` | Workshop 5 |

---

## How to use this repository

**If you are facilitating these workshops:**
Start with the `pre-work/` folder. Read the facilitator guide for Workshop 0
before anything else. Everything you need to run each session is in the
workshop folder — the facilitator guide tells you what to do, the slides give
you what to say, and the attendee materials handle the rest.

**If you are adapting this for a specific engagement:**
The content is deliberately generic. Anywhere you see `[ORGANISATION]`,
`[CLUSTER COUNT]`, `[TIME WINDOW]`, or similar placeholders, substitute your
customer's specifics. Keep the repository content clean and agnostic — make
your customisations in your presentation deck.

**If you are contributing:**
Keep it vendor-neutral. Keep it plainspoken. Keep it grounded in the
frameworks above. If you are adding content, follow the existing file and
folder naming conventions and update this README accordingly.

---

## Placeholder conventions

Throughout this repository, square brackets indicate content that should be
customised per engagement:

| Placeholder | What it represents |
|-------------|-------------------|
| `[ORGANISATION]` | The customer or organisation name |
| `[PLATFORM TEAM]` | The platform or SRE team name |
| `[CLUSTER COUNT]` | Number of clusters in scope |
| `[TIME WINDOW]` | The agreed reporting period |
| `[FACILITATOR]` | The person running the workshops |
| `[DATE]` | Session date |
| `[ENVIRONMENT]` | e.g. production, non-production |

---

## A note on trust

The most valuable thing you can build through this process is not a cost
model. It is credibility.

When you help an organisation understand their platform economics clearly —
without steering the outcome, without glossing over uncomfortable numbers, and
without making every finding point back to a predetermined answer — you become
someone they rely on. That is a different relationship to the one that starts
and ends at renewal time.

Run these workshops well and the output is not just a decision brief. It is a
demonstrated track record of giving good advice. That is what a trusted
advisor looks like in practice — and it is what makes every future
conversation easier, more honest, and more productive for both sides.

So while the frameworks and templates in this playbook are important, how you
facilitate matters just as much. Stay curious. Stay neutral. Let the evidence
do the work.

---

*This playbook is designed to be reused, adapted, and improved. If something
does not work in practice, change it and share what you learned.*
