# Workshop 1 — Slides
## Scope, Glossary, and Rules of the Game

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

Workshop 1 — Scope, Glossary, and Rules of the Game

[DATE] | [FACILITATOR]
```

### Speaker Notes

Open with the slide visible and move straight into the recap of Workshop 0.
Do not linger here.

---

## Slide 2: Where We Are

**Layout:** Title at top, horizontal progress indicator showing five workshops with Workshop 1 highlighted

### Content

```
Workshop 0    Workshop 1    Workshop 2    Workshop 3    Workshop 4    Workshop 5
Setup         Scope and     Cost          Unit          Value and     Scenarios
              Rules         Baseline      Economics     Risk          and Plan

              [YOU ARE HERE]
```

### Speaker Notes

"We agreed on the scope shape, delivery model, and data owners in Workshop 0. Today, we go a level deeper, we lock in scope, agree on cost treatment rules, and make sure we all mean the same things when we use the same words.

Everything we agree today goes into the Assumptions Register. That is what makes the final output trusted and defensible."

---

## Slide 3: What We Are Producing Today

**Layout:** Title at top, clean list of five outputs

### Content

```
By the end of this session we will have:

A written scope statement — agreed by the room

Assumptions Register v1 — every decision, versioned

A glossary of agreed terms

A unit metrics shortlist — three to five measures

A data request list — every item has a named owner
```

### Speaker Notes

"These five things are the foundation for everything that follows. Workshop 2 builds the cost model. Workshop 3 builds the unit economics. Both of those depend on what we agree on today.

It is worth taking the time to get this right."

---

## Slide 4: Why Scope and Rules Matter

**Layout:** Title at top, single strong statement centred, supporting
explanation below

### Content

```
Most cost debates do not come from bad data.

They come from hidden assumptions.

What is included. What is shared. What gets allocated.
What counts as platform cost versus workload cost.

Agreeing the rules now means the output is trusted, not argued over.
```

### Speaker Notes

"Before we get into the detail I want to explain why we are spending time on this.

Every cost review I have seen that went wrong did not go wrong because the numbers were bad. It went wrong because people disagreed about what the numbers meant, because the assumptions were never made explicit.

That is what the Assumptions Register fixes. Every decision we make today is written down, versioned, and agreed upon. When someone asks later, ‘Why did you include that?’ the answer is right there."

---

## Slide 5: Confirming Scope — Platforms

**Layout:** Title at top, table with platform names, and in-scope status to be confirmed live

### Content

```
Platform              Role              In scope?

[PLATFORM A]          Baseline          Confirm
[PLATFORM B]          Baseline          Confirm
[PLATFORM C]          Baseline          Confirm
[PLATFORM D]          Scenario only     Confirm
[PLATFORM E]          Scenario only     Confirm

Anything missing?
```

### Speaker Notes

"We agreedon on a rough scope shape in Workshop 0. Let us confirm it now.

Walk through the platform list and confirm each one. Note any changes from what was agreed in Workshop 0. If something new has come up, discuss it briefly and make a decision."

Record decisions in the Assumptions Register as they are made.

---

## Slide 6: Confirming Scope — Environments and Time Window

**Layout:** Title at top, two sections side by side

### Content

```
Environments                        Time window

Production                          Last full quarter
Non-production                      Last three months
Both                                Other: [confirm]
Separated or combined?

Confirm and record.                 Confirm start and end date.
```

### Speaker Notes

"Two more scope decisions to lock in.

On environments: the default is to include both production and non-production. Some teams prefer to model them separately. Either works; we just need to agree on it now so we are consistent throughout.

In the time window, a full quarter is usually the cleanest. If quarter boundaries are messy for your organisation, three calendar months work just as well."

Record both decisions in the Assumptions Register.

---

## Slide 7: Confirming Scope — Cost Types

**Layout:** Title at top, table with cost types and in-scope status to be confirmed live

### Content

```
Cost type              Examples                       In scope?

Cloud compute          EC2, VMs, node pools           Confirm
Cloud storage          Block and object storage        Confirm
Cloud network          Load balancers, NAT, egress     Confirm
Managed service fees   EKS fees, AKS fees              Confirm
Platform tooling       Observability, security, CI/CD  Confirm
Subscriptions          Platform licences, support      Confirm
Operating effort       Platform team time              Confirm
Shared services        IAM, shared logging             Confirm
```

### Speaker Notes

"Let us work through the cost types now. For each one, in or out?

For anything that is uncertain or contested, we note it as a gap with a low confidence rating and move on. We do not let one line item stall the session.

A useful test: if we excluded this cost, would our picture of true platform cost be misleading? If yes, include it. If no, exclude it and note why."

Record every decision in the Assumptions Register.

---

## Slide 8: Cost Treatment Rules

**Layout:** Title at top, four rules as clear numbered headings

### Content

```
We are not implementing chargeback.
We are agreeing showback rules, making costs visible before billing anyone.

Rule 1    How do we treat shared platform costs?

Rule 2    How do we treat non-production environments?

Rule 3    How do we capture operating effort?

Rule 4    Do we explicity call out tooling duplication?
```

### Speaker Notes

"Now we have scope locked, we need to agree on how we handle the costs that do not sit cleanly in one place.

These four rules will be applied consistently throughout the model. If anything changes as we gather data, we update the Assumptions Register and note the version.

Let us work through them one at a time."

---

## Slide 9: Rule 1 — Shared Platform Costs

**Layout:** Title at top, three options clearly laid out with space to record the decision

### Content

```
Some costs serve multiple platforms or teams.

Option A    Allocate proportionally by usage
            Best if tagging and labels exist

Option B    Allocate equally across platforms
            Simpler but less precise

Option C    Hold in a shared unallocated bucket
            Acceptable for v1 — refine in Workshop 3

Decision:
```

### Speaker Notes

"Shared costs are things like shared tooling, shared infrastructure, or shared services that sit across more than one platform or team.

For the first pass, Option C is usually the right call; it is honest about what we know and does not introduce false precision. We can refine allocation in Workshop 3 once we have better data.

What feels right for your environment?"

Record the decision and the reason in the Assumptions Register.

---

## Slide 10: Rule 2 — Non-Production Environments

**Layout:** Title at top, three options clearly laid out with space
to record the decision

### Content

```
How do we treat non-production cost?

Option A    Include in total — separate line item
            Most transparent

Option B    Include in total — not separated
            Simpler, less visible

Option C    Exclude from unit economics — include in total
            Useful if non-prod is structurally very different

Decision:
```

### Speaker Notes

"Non-production environments can account for a significant portion of platform cost, sometimes more than production, depending on how they are managed.

Option A tends to surface the most insight, particularly around cluster sprawl and overprovisioning in non-production environments. But if the data is hard to separate, Option B is a reasonable starting point."

Record the decision and the reason in the Assumptions Register.

---

## Slide 11: Rule 3 — Operating Effort

**Layout:** Title at top, three options clearly laid out with space to record the decision

### Content

```
How do we capture platform team operating effort?

Option A    Percentage split of team time across activities
            e.g. 30% upgrades, 20% incidents, 20% onboarding

Option B    Rough hours per activity per month
            More granular but requires more input

Option C    Exclude — note as a gap with confidence impact
            Only if truly impossible to estimate

Decision:
```

### Speaker Notes

"Operating effort is often the highest hidden cost in a platform team. If we exclude it, we risk making decisions on an incomplete picture.

Option A is usually the most practical starting point; a rough percentage split is enough to put a cost on it without requiring a full-time tracking exercise.

Even a range is useful. ‘The team spends roughly a third of its time on upgrades and patching’ is a number we can work with."

Record the decision and the reason in the Assumptions Register.

---

## Slide 12: Rule 4 — Tooling Duplication

**Layout:** Title at top, two options clearly laid out with space to record the decision

### Content

```
Where the same capability exists across multiple platforms, do we model duplication explicitly?

Option A    Yes — model as a separate line
            Surfaces consolidation opportunity and estimated saving

Option B    No — include in platform tooling without separating
            Simpler, less visible as a lever

Decision:
```

### Speaker Notes

"Running separate observability stacks, security tooling, and CI/CD pipelines across multiple platforms is a real cost in money, in people time, and in cognitive overhead.

If we model it explicitly, it becomes a visible lever in the scenario modelling in Workshop 5. That tends to make consolidation options look more compelling, not because we have steered the outcome, but
because the duplication cost is visible and real.

My recommendation is Option A. But it is your call."

Record the decision and the reason in the Assumptions Register.

---

## Slide 13: Unit Metrics Shortlist

**Layout:** Title at top, table of metrics with what each one tells you, to be shortlisted live

### Content

```
Unit metric                          What it tells you

Cost per production app per month    What it costs to run one app

Cost per tenant or namespace         What it costs to serve one team
per month                            or product

Cost per environment                 Prod versus non-prod cost split

Effective cost per vCPU-hour used    How efficiently capacity is used

Ops cost per cluster per month       Operational overhead per cluster

Cost per deployment or release       What it costs to ship a change

Pick three to five.
```

### Speaker Notes

"Total spend is a number. Unit economics is what that number means.

Instead of ‘we spend X on Kubernetes, ’ we want to say ' a production application costs Y per month.’ That is the number leadership, and Finance can act on.

I want to agree on a shortlist of three to five metrics now, the ones that make sense for your environment and connect to how you talk about the platform internally. We will define them properly and build the model in Workshop 3."

Work through the table live. Note any data dependencies that are already obvious; these feed into the data request list.

---

## Slide 14: Data Request and Owners

**Layout:** Title at top, table with data needed, why, owner, and due date columns, to be populated live

### Content

```
Data needed                  Why we need it               Owner   Due date

Cluster inventory            Defines scope
Cloud billing exports        Source of truth for spend
Platform subscription        Fixed vs variable cost
Tooling list and costs       Duplication and consolidation
Ops effort estimate          Cost not on invoices
Production app list          Unit economics foundation
Namespace or team mapping    Allocation rules
Utilisation data             Effective cost per vCPU
```

### Speaker Notes

"Now that we have agreed on the scope and unit metrics, let us finalise the data request list and make sure everything has a name against it.

I am not looking for perfect data by Workshop 2. I am looking for the best available first pass, something we can build the baseline skeleton from and refine as better data comes in.

Let us work through each item. Who owns it and what is a realistic due date, not the ideal date, the realistic one?"

Do not close this slide until every item has a named owner.

---

## Slide 15: What We Have Agreed Today

**Layout:** Title at top, clean summary of five outputs confirmed

### Content

```
Scope locked — [brief summary]

Cost treatment rules agreed — in the Assumptions Register

Unit metrics shortlist confirmed — [list agreed metrics]

Data request list finalised — every item has an owner

Workshop 2 confirmed — [DATE] | [TIME]
```

### Speaker Notes

"Here is where we have landed."

Read through the list and confirm each item is genuinely agreed upon. If anything is still open, name it and confirm who is closing it and when.

Then ask the final question and mean it:

"Is there anything we have not resolved today that would make you less confident going into Workshop 2?"

Listen. Address anything that comes up before closing the session.

---

## Slide 16: See You in Workshop 2

**Layout:** Clean closing slide — next session details centred, plenty of white space

### Content

```
Workshop 2 — Cost Taxonomy and Baseline Model

[DATE] | [TIME] | [LOCATION / LINK]

Pre-read coming your way before the session.

Data request list is live — please action your items before Workshop 2.
```

### Speaker Notes

"Thanks for the work today. Workshop 2 is where we build the cost taxonomy and baseline model skeleton. We will use the data coming in between now and then to start filling it in.

You will get a short pre-read before the session. And the data request list is live from today; the sooner we can get those inputs in, the stronger the baseline will be."

Close the session cleanly.
