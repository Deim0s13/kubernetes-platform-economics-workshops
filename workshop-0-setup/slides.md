# Workshop 0 — Slides
## Setup and Expectations

**Version:** 1.0  
**Last updated:** [DATE]  
**Corresponding facilitator guide:** facilitator-guide.md v1.0  

---

## Version history

| Version | Date | Changes |
|---------|------|---------|
| 1.0 | [DATE] | Initial version |

---

## How to use this file

Each slide includes a title, layout note, content, and speaker notes. Build your presentation deck from this file. This file is the source of truth. If you update the deck, update this file to match and bump the version number.

Speaker notes are written in your voice, conversational and plain. They are not a script to read verbatim, but a guide for what to cover and how to frame it.

---

## Slide 1: Title

**Layout:** Title slide — centred title, subtitle, and session details below

### Content

```
Kubernetes Platform Economics

Workshop 0 — Setup and Expectations

[DATE] | [FACILITATOR]
```

### Speaker Notes

Do not spend time on this slide. Open with it visible, welcome the group, and move straight into your opening question. The title slide is a signal that you are starting, nothing more.

---

## Slide 2: What Would Make This Worthwhile?

**Layout:** Title at top, single open question centred on slide, plenty of white space

### Content

```
What would make this feel worthwhile to you, personally, not just as a team outcome?
```

### Speaker Notes

Ask this question and stop talking. Let people answer fully. Do not rush past it and do not fill the silence.

What people say here tells you where the anxiety or scepticism sits. Note anything that needs addressing directly. If someone reveals a misconception about the process, address it calmly before moving on.

This is the most important two minutes of Workshop 0.

---

## Slide 3: What We Are Here to Do

**Layout:** Title at top, three clear statements below with enough white space to breathe

### Content

```
Three questions. Five workshops. One decision brief.

What does our Kubernetes estate cost today?

What value does it create for teams and the business?

What are our options for improving cost per outcome without increasing risk?
```

### Speaker Notes

Keep this conversational; you are not reading the slide, you are reinforcing it.

"These are the three questions we are going to answer with evidence over the course of five workshops. The output is a decision brief that your leadership team, Finance, and Procurement can act on. Today is just about making sure we set that up properly."

---

## Slide 4: What This Is — and What It Is Not

**Layout:** Title at top, two columns — left "What it is", right "What it is not"

### Content

```
What it is                        What it is not

A structured way to build a       A cost-cutting exercise
shared, trusted fact base

Evidence-based options with       A vendor exercise or
clear trade-offs                  predetermined outcome

A decision brief for leadership,  A request to boil the ocean
Finance, and Procurement

Grounded in industry-standard     A platform argument
frameworks
```

### Speaker Notes

"Before we go any further, I want to be clear about what this is and what it is not, because getting that wrong early creates friction later.

This is not a cost-cutting exercise. We are measuring cost and value together. And it is not a vendor exercise. The frameworks we are using, FinOps, TBM, DORA, and SPACE, are industry standards. The conclusions will follow the evidence."

Pause after this slide. Ask if anyone has questions before moving on.

---

## Slide 5: The Five Workshops

**Layout:** Title at top, table with workshop number, title, and duration

### Content

```
Workshop 0    Setup and Expectations              35-45 minutes
Workshop 1    Scope, Glossary, and Rules          90 minutes
Workshop 2    Cost Taxonomy and Baseline          2 hours
Workshop 3    Allocation and Unit Economics       2 hours
Workshop 4    Value and Risk Scorecard            90 minutes
Workshop 5    Scenarios and 90-Day Plan           3 hours
```

### Speaker Notes

Walk through this briefly, one sentence per workshop.

"Workshop 0 is today, setup and alignment. Workshop 1 locks in scope and rules. Workshop 2 follows the money. Workshop 3 translates spend into cost per outcome. Workshop 4 makes sure we are measuring platform
value alongside cost. And Workshop 5 gives you options with numbers and a practical plan."

Do not go into detail on any individual workshop here. If someone asks, acknowledge it and move on. There will be a pre-read before each session.

---

## Slide 6: The Frameworks We Use

**Layout:** Title at top, four framework names as clear headings with one-line descriptions beneath each

### Content

```
FinOps
Cost visibility, allocation, and unit economics, connecting technical decisions to financial outcomes.

TBM: Technology Business Management
A standard cost classification structure so IT and Finance work from the same language.

DORA
Four metrics for software delivery performance: deployment frequency, lead time, change failure rate, time to restore.

SPACE
Developer productivity across five areas: Satisfaction, Performance, Activity, Communication, Efficiency.
```

### Speaker Notes

"We are anchoring this work in four industry-standard frameworks, none of them proprietary, all of them widely used.

FinOps helps us move from ‘what do we spend?’ to ‘what do we spend per outcome?’ TBM gives us a cost structure that Finance will recognise. DORA and SPACE make platform value visible to leadership.

You do not need to know these frameworks in detail going in. That is what the pre-reads are for. What matters is that the output is credible and defensible, and these frameworks are how we get there."

---

## Slide 7: Today's Agenda

**Layout:** Title at top, clean numbered list with topic and time

### Content

```
1.   Welcome and introductions             5 minutes
2.   What we are doing and why             8 minutes
3.   Scope shape                           8 minutes
4.   Delivery model and logistics          5 minutes
5.   Data and data owners                  8 minutes
6.   Ways of working and next steps        5 minutes
7.   Close and recap                       3 minutes
```

### Speaker Notes

"Here is what we are covering today. Nothing heavy, this is a setup session. The goal is to leave with clarity on scope, ownership, and how we are going to work together."

Move through this slide quickly. It is orientation, not content.

---

## Slide 8: Scope Shape

**Layout:** Title at top, four questions as clear headings with space to capture answers live

### Content

```
Which platforms are in scope?

Which environments are we including?

What time window are we working with?

What cost types are we including?
```

### Speaker Notes

Work through these four questions live and capture answers in the Assumptions Register as you go. Do not just talk about scope; agree on it.

“We are not locking down the details today, that is Workshop 1. But I want to make sure we are aligned on the shape before we go any further.”

Close this slide with: “Is there anything in your Kubernetes estate we would be embarrassed to miss, or anything that should definitely stay out of scope?”

---

## Slide 9: Delivery Model

**Layout:** Title at top, two clear options side by side

### Content

```
Option A — You run it               Option B — We run it together

Your team runs the workshops        We facilitate jointly
using the toolkit provided
                                    You own the assumptions
Agendas, templates, facilitation    and decisions throughout
notes, and example outputs
included                            Model and outputs built
                                    together
Best for: teams with capacity
and confidence to self-serve        Best for: teams who want
                                    acceleration and a
                                    second perspective
```

### Speaker Notes

Present both options neutrally, do not steer toward either one.

"There are two ways we can approach this. What matters is that the outputs stay yours regardless of how we get there. The assumptions and decisions are always owned by your team."

---

## Slide 10: Minimum Viable Data

**Layout:** Title at top, two-column table, data needed and why we need it. The owner column is to be filled in live.

### Content

```
Data needed                      Why we need it

Cluster inventory                Defines scope — prevents gaps

Cloud billing exports            Source of truth for actual spend
(AWS CUR / Azure)

Platform subscription            Separates fixed from variable cost
overview

Tooling list                     Identifies duplication across
                                 platforms

Platform ops effort              Captures cost invoices do not show
estimate (rough)

Production app list              Grounds unit economics in reality
or top 20 workloads
```

### Speaker Notes

"We do not need perfect data to get started. Where we do not have exact numbers, we will use ranges and confidence ratings.

What I do need is this minimum set of inputs. Let us put a name against each item now."

Work through the table live and fill in the owner column together.

For anything sensitive: "If you would prefer to keep certain figures internal, that is completely fine. We can work with ranges, or you populate that part of the model yourselves."

---

## Slide 11: Ways of Working

**Layout:** Title at top, four clear labelled points

### Content

```
Documents       Everything lives in [LOCATION] — one place,
                always current

Versioning      Every document carries a version number and date

Recaps          Short summary within 24 hours of every session —
                decisions, actions, next session confirmed

Cadence         [WORKSHOP DATES / AGREED CADENCE]
```

### Speaker Notes

"A few practical things before we close."

Confirm the shared workspace location, open it on screen if you can, so people can see it exists.

"On versioning, this matters more than it sounds. When leadership asks which version of the model you used, you want a clear answer.

On recaps, I will keep them short. One page, one email. Decisions made, actions outstanding, next session confirmed."

Confirm dates or a process for agreeing on them before moving on.

---

## Slide 12: What We Have Agreed Today

**Layout:** Title at top, clean summary checklist

### Content

```
Scope shape confirmed

Delivery model agreed

Data owners named

Working environment set up

Workshop 1 confirmed — [DATE] | [TIME]

Recap email coming within 24 hours
```

### Speaker Notes

"Here is where we have landed."

Read through the list briefly and confirm each item is genuinely agreed upon. If anything is still open, name it and confirm who is closing it and when.

Then ask the final question and mean it:

"Is there anything we have not covered today that would make you feel less confident going into this?"

Listen. If something comes up, address it. Do not close the session with unresolved concerns sitting in the room.

---

## Slide 13: See You in Workshop 1

**Layout:** Clean closing slide — next session details centred, plenty of white space

### Content

```
Workshop 1 — Scope, Glossary, and Rules of the Game

[DATE] | [TIME] | [LOCATION / LINK]

Pre-read coming your way before the session.
```

### Speaker Notes

"Thanks for the time today. Workshop 1 is where the real work starts. We will lock in the scope and rules, then begin building the Assumptions Register together.

You will get a short pre-read before the session so you know exactly what to expect."

Close the session cleanly. If anything comes up about platform specifics, park it and pick it up in Workshop 1.
