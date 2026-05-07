# Workshop 2 — Facilitator Guide
## Cost Taxonomy and Baseline Model

**Version:** 1.0  
**Duration:** 2 hours  
**Audience:** Product Owner, Platform Lead, Platform Engineers and SREs  
**Facilitator:** [FACILITATOR]  

---

## Version history

| Version | Date | Changes |
|---------|------|---------|
| 1.0 | [DATE] | Initial version |

---

## Purpose

Workshop 2 marks the start of the cost model. The goal is to agree on a cost taxonomy and build a baseline model skeleton, a structured view of where spend goes across the Kubernetes estate.

You will not have complete data at this stage. That is expected. The baseline skeleton is a framework to populate progressively, not a finished model. What matters is that the structure is right and every cost has a home.

By the end of this session, you will have:

- A cost taxonomy agreed and understood by the room.
- Known spend is mapped into the taxonomy.
- A fixed versus variable cost split, even if partial
- A clear view of which buckets are well understood and which need more data
- An updated data gaps list with owners and revised due dates
- An initial view of where spending concentrates across the estate

---

## Before the session

### Review what data has come in

Before the session, review any data shared since Workshop 1.

For each data item received:
- Has it been mapped to the right cost bucket in the taxonomy?
- Are there obvious gaps or anomalies worth flagging in the session?
- Does the data raise new questions about scope or cost treatment rules?

For each data item still outstanding:
- Has the owner been reminded?
- Is the due date still realistic?
- Do you need to agree on an estimate or a workaround for Workshop 2?

### Prepare the baseline model skeleton

Before the session, set up the baseline model with the taxonomy structure in place, even if all cells are empty. Having the structure visible on-screen during the session makes the exercise concrete and avoids spending time on formatting.

The skeleton should include:

- Six cost bucket tabs or sections matching the taxonomy
- Columns for: cost item, platform, source, monthly amount, annual amount, fixed or variable, confidence rating, notes
- A summary tab showing totals by bucket and by platform

### Check the Assumptions Register

Review the Assumptions Register from Workshop 1. Confirm that:

- Scope decisions are still accurate.
- Cost treatment rules are still being agreed upon.
- Any decisions that need revisiting are flagged before the session.

---

## Session agenda

| Time | Section | Duration |
|------|---------|----------|
| 0:00 | Welcome, recap, and outcomes | 10 minutes |
| 0:10 | Introduce the cost taxonomy | 15 minutes |
| 0:25 | Map known spend into the taxonomy | 40 minutes |
| 1:05 | Fixed versus variable cost split | 15 minutes |
| 1:20 | Data gaps review and owners | 15 minutes |
| 1:35 | Close and next steps | 10 minutes |

---

## Section-by-section guidance

---

### Welcome, recap, and outcomes (10 minutes)

**What you are doing**

Opening the session, recapping Workshop 1, acknowledging data that has come in, and setting clear expectations for what this session produces.

**Talk track**

*"Welcome back. In Workshop 1, we locked in scope, agreed on cost treatment rules, and built the data request list. Since then, [DATA ITEMS RECEIVED] have come in — thank you to [NAMES] for getting those across.

*Today, we use that data and the agreed structure to start building the cost model. We will agree on a cost taxonomy, map known spend to it, and identify gaps. By the end of this session, we will have a baseline skeleton that is ready to populate as the remaining data comes in.*

*We will not have a complete model today. That is fine and expected. What we need is the right structure and a clear view of what we know, what we are estimating, and what we still need."*

Check in:

*"Anything from Workshop 1 that needs clearing up before we get started? Any surprises in the data that came in?"*

**Facilitation notes**

- Acknowledge data that has come in by name, which encourages the people who have not yet delivered their items.
- If no data has come in at all, address it directly but without blame:
*“We will work with estimates today and update the model as data comes in. That is a normal part of the process.”*
- If surprising data has come in unexpectedly high spend, anomalies, gaps, note it and come back to it during the mapping exercise rather than derailing the opening.

---

### Introduce the cost taxonomy (15 minutes)

**What you are doing**

Walking the group through the six cost buckets, making sure everyone understands what sits where, and why the structure matters.

**Why this matters**

The taxonomy is the backbone of the entire model. If people do not understand the structure, spending ends up in the wrong buckets, the model becomes unreliable, and the output is contested rather than trusted.

Spend fifteen minutes here. It is worth it.

**Talk track**

*"Before we start mapping spend, I want to walk you through the cost taxonomy we are going to use because the structure matters as much as the numbers.*

*We are using a TBM-aligned taxonomy. TBM (Technology Business Management) is an industry standard for classifying technology costs. Finance will recognise this structure. That is the point.*

*There are six buckets. Let me walk you through them."*

Walk through each bucket with an example or two:

**Cloud infrastructure**
*"Raw compute, storage, and network. Virtual machines, node pools, block storage, load balancers, egress. This is what shows up most obviously on a cloud bill."*

**Managed service fees**
*"The fees cloud providers charge for managed Kubernetes services, EKS cluster management, and AKS management. These are separate from the compute cost of running the nodes."*

**Platform tooling**
*"Everything that makes the platforms operable above and beyond raw infrastructure. Observability, security scanning, CI/CD, backup and DR. This is where duplication across platforms tends to show up most
clearly."*

**Subscriptions**
*"Platform licences, support agreements, recurring software fees. These are typically fixed costs; they do not change with usage in the short term."*

**Operating effort**
*"The time your team spends running, maintaining, and improving the platforms. Upgrades, patching, incidents, onboarding, building golden paths. This is often the highest hidden cost, and the one most commonly left out of cost reviews."*

**Shared services**
*"Costs that sit beneath the platforms and serve them without being attributable to one platform alone. IAM, shared network infrastructure, shared logging platforms."*

Then check understanding:

*"Before we start mapping — any questions about what sits where? Are there any costs in your environment that you are not sure where to put?"*

**Facilitation notes**

- Operating effort is often the concept that gets the most pushback. If someone challenges it, hold the line:
  *"We know it is an estimate. A rough split is enough. If we leave it out, we are missing a significant part of the true cost picture."*
- If there are costs that genuinely do not fit the six buckets, create an "other" bucket rather than forcing a bad fit. Note it in the Assumptions Register.
- Tooling duplication often surfaces here for the first time. If it does, note it and come back to it; this is a finding, not a problem to solve in Workshop 2.

---

### Map known spend into the taxonomy (40 minutes)

**What you are doing**

Working through each cost bucket together, mapping known spend into the model, and identifying gaps. This is the core exercise of Workshop 2.

**How to run it**

Work through the taxonomy bucket by bucket. For each one:

1. Ask what spending is known as and what its source is
2. Enter the amount with a confidence rating.
3. Note any gaps or questions.
4. Move on, do not get stuck on any single line item.

Keep the pace steady. Forty minutes for six buckets means roughly six to seven minutes per bucket on average, but cloud infrastructure typically takes longer, and shared services shorter.

**Bucket by bucket prompts**

**Cloud infrastructure**

*"Let us start with cloud infrastructure, the biggest bucket for most Kubernetes estates.*

*For compute, do we have the AWS CUR or Azure export available? What are the main instance types or VM sizes running the node pools across each platform?"*

*"For storage, what storage classes are in use? Any significant object storage consumption?"*

*"For the network, are there significant load balancer costs? Data egress? Any NAT gateway costs worth capturing?"*

Things to look for:
- Idle or oversized node pools (compute cost with low utilisation)
- Egress costs that suggest inefficient data movement
- Load balancer proliferation (one per service is a common anti-pattern)

**Managed service fees**

*"For managed service fees, are EKS and AKS cluster management fees visible in the billing exports? How many clusters are we paying management fees on?"*

Things to look for:
- Cluster counts are higher than expected.
- Management fees on clusters that appear low-utilisation

**Platform tooling**

*"Platform tooling is often where the most interesting findings sit, particularly if the same capability exists across multiple platforms.*

*What observability tooling is running and across which platforms? Is it the same stack or different stacks per platform?"*

*"Same question for security scanning, CI/CD, and backup, are these consistent across platforms, or do we have separate implementations?"*

Things to look for:
- Separate observability stacks per platform (duplication cost)
- SaaS tooling costs that are not on the cloud bill
- Tooling that was set up and never reviewed for value

**Subscriptions**

*"What platform licences or support agreements are in scope? Do we have the renewal dates and current terms available?"*

Things to look for:
- Subscriptions that predate current platform usage patterns
- Support tiers that may be higher than current needs
- Licences that cover more capacity than is being used

**Operating effort**

*"This one is an estimate, and that is fine.*

*If I asked you to split your team's time across the last quarter, what would the rough percentages look like? Upgrades and patching? Incident response? Onboarding new teams? Building and maintaining standards?"*

If the group is uncomfortable with percentages, try this instead:

*"Think about the last month. What took most of the team's time? What would you say was the single biggest time sink?"*

Things to look for:
- High proportion of time on upgrades and patching (often a sign of platform fragmentation or deferred maintenance)
- High incident volume (reliability signal)
- Significant onboarding overhead (platform friction signal)

**Shared services**

*"Finally, shared services. IAM, shared network infrastructure, shared logging platforms. Are any of these costs visible and attributable to the Kubernetes estate, even roughly?"*

This bucket is often the least complete in the first pass. Note gaps and move on.

**Facilitation notes**

- Keep the model visible on screen throughout. Update it live as decisions are made.
- Use confidence ratings consistently. If someone gives a number without a source, it is Low confidence until a source is confirmed.
- If a number surprises people, note it, but do not investigate it in the session. The finding is the finding; analysis comes later.
- If a bucket is completely empty because data has not come in, note it as a gap, confirm the owner, and move on.

---

### Fixed versus variable cost split (15 minutes)

**What you are doing**

Working through the populated taxonomy and tagging each line item as fixed or variable. This does not need to be perfect; a first-pass classification is enough for Workshop 2.

**Talk track**

*"Now that we have spent some time mapping it out, I want to work through a simple but important distinction: which of these costs are fixed and which are variable.*

*Fixed costs do not change with usage in the short term. A subscription fee is the same whether you run ten workloads or a hundred. Changing a fixed cost requires a structural decision, renegotiating a contract, consolidating platforms, or moving to a different model.*

*Variable costs scale with usage. Compute, storage, and egress go up and down with demand. Changing a variable cost requires an operational decision, rightsizing, autoscaling, and better utilisation.*

*The reason this matters is that it tells us which levers are available and how quickly we can pull them."*

Work through the taxonomy and tag each line item. Where something is genuinely mixed, split it or note it as partially fixed, partially variable.

**Facilitation notes**

- Do not let this become a lengthy debate. First-pass classification is enough; refine in later workshops if needed.
- Operating effort is typically variable, but with a fixed floor, the team remains in place regardless of workload volume. Note this nuance if it comes up.
- Subscriptions are almost always fixed. Managed service fees can vary if the number of clusters changes. Tooling SaaS costs can be either, check the contract model.

---

### Data gaps review and owners (15 minutes)

**What you are doing**

Reviewing what remains missing, confirming owners, and deciding whether to estimate, defer, or close each gap before Workshop 3.

**Talk track**

*"Let us look at what we still need. For each gap, I want to agree on one of three things: we estimate it with a confidence rating and move on, we wait for the data with a firm date, or we agree to
exclude it and note why."*

Work through the gaps list:

| Gap | Approach | Owner | Date |
|-----|----------|-------|------|
| [ITEM] | Estimate / Wait / Exclude | | |

For each gap where the owner is present:

*"Is [DATE] still realistic? If not, what is?"*

For each gap where the owner is not present:

*"Who can follow up with [OWNER] today and confirm the date?"*

**Facilitation notes**

- Be direct about gaps that are blocking the model. If operating effort is missing and the owner is in the room, agree on an estimate now rather than waiting.
- If a gap has no realistic path to resolution, agree to exclude it with a note explaining the impact on confidence. Do not let an unresolvable gap block progress.
- Update the Assumptions Register with every gap decision, approach, owner, and date.

---

### Close and next steps (10 minutes)

**What you are doing**

Summarising what was produced, confirming the baseline skeleton is saved and shared, and making Workshop 3 completely clear.

**Talk track**

*"Here is what we have built today. We have a cost taxonomy agreed and a baseline model skeleton with [SUMMARY OF WHAT IS POPULATED]. We have a clear view of which buckets are well understood and which
still need data.*

*The model will continue to populate as the remaining data comes in. I will update it and share a revised version before Workshop 3.*

*Workshop 3 is [DATE/TIME]. That is where we move from total cost to unit economics, cost per app, and cost per tenant, cost per environment. That is the number that will land with leadership and Finance.*

*You will get a short recap from me within 24 hours, decisions made, actions, and the Workshop 3 pre-read."*

Then ask the final question:

*"Is there anything in what we have built today that concerns you, or anything that looks wrong before we go further?"*

If something looks wrong, address it now. A flawed baseline that goes unchallenged in Workshop 2 will cause bigger problems in Workshop 5.

---

## Handling difficult moments

### "That number looks too high — something must be wrong"

Do not dismiss the concern, but do not investigate it in the session.

*"Good catch, let us note it and flag the confidence as Low until we can verify the source. We will not hold up the session on one line item, but we will make sure it gets checked before Workshop 3."*

### "We do not have the cloud billing exports yet"

*"That is okay. We will build the skeleton with what we have and use estimates with Low confidence ratings where needed. The structure is what matters today; the numbers will fill in as data comes in."*

### "Our tooling costs are spread across a dozen different invoices
and nobody knows the total"

*"That is actually a finding in itself; it tells us something about how platform cost is currently managed. Let us note what we know, estimate what we can, and flag tooling cost visibility as an improvement in the output."*

### "Why are we including operating effort? We cannot really
put a number on that"

*"We do not need a precise number. A rough estimate, even a range, is enough to include it in the model. If we leave it out entirely, we risk making decisions based on an incomplete picture. A platform that looks cheap on the cloud bill can be very expensive when you factor in the team time it consumes."*

### The session starts running over time

If you are running short on time, prioritise the taxonomy mapping over the fixed-versus-variable split and gaps review; both can be completed asynchronously before Workshop 3. The taxonomy structure and initial mapping are what must be agreed upon in the room.

---

## Output checklist

Before you close the session, confirm these are in place:

- [ ] Cost taxonomy agreed and understood by the room.
- [ ] Baseline model skeleton populated with known spend.
- [ ] Confidence ratings applied to every line item.
- [ ] Fixed versus variable split completed, at least first pass
- [ ] Data gaps list updated, approach, owner, and date for every gap
- [ ] Assumptions Register updated with any new decisions.
- [ ] Workshop 3 date and time confirmed

---

## Post-session actions (within 24 hours)

- [ ] Send recap email, decisions made, actions, Workshop 3 confirmed.
- [ ] Save and share the baseline model, clearly versioned.
- [ ] Update the Assumptions Register, version bumped with today's date.
- [ ] Send Workshop 3 pre-read and calendar invite.
- [ ] Follow up individually with outstanding data owners.
- [ ] Update the model with any data that comes in before Workshop 3 and share a revised version.
