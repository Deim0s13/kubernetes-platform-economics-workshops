# Templates

This folder contains the reusable templates for the Kubernetes Platform Economics Workshops. They fall into three categories: working documents, the decision brief, and the 90-day plan.

---

## An important note on how these templates work

These templates are designed to be completed alongside the workshops, not instead of them.

Every section that requires workshop output is marked clearly with the session it comes from and a pointer to the relevant workshop materials. If you find yourself unable to complete a section, that is by design.
It means a workshop has not been run yet, and the output you are trying to produce is not ready.

The templates do not replace the workshops. They are the place where workshop outputs are recorded, consolidated, and shaped into something decision-ready.

Trying to complete these templates without running the workshops will produce outputs that look complete but are not trusted, because the assumptions were never agreed upon in the room, the rules were never challenged, and the numbers were never validated by the people who own them.

Run the workshops. Use the templates to capture what emerges.

---

## The dependency chain

Each template depends on outputs from specific workshops. The chain
works in this order:

```
Workshop 1  →  Assumptions Register
               Data Request List

Workshop 2  →  Cost Taxonomy and Baseline Model

Workshop 3  →  Unit Metrics Definition
               Showback View

Workshop 4  →  Value and Risk Scorecard

Workshop 5  →  Workload Placement Matrix
               Scenario Comparison
               90-Day Plan

All workshops  →  Decision Brief
```

The decision brief cannot be completed until all five workshops have been held and all working documents have been populated.

---

## Placeholder conventions

Throughout these templates, the following conventions are used:

| Convention | What it means |
|------------|--------------|
| `[ORGANISATION]` | The customer or organisation name |
| `[FACILITATOR]` | The person who ran the workshops |
| `[DATE]` | A specific date — session, version, or due date |
| `[VERSION]` | Document version number — e.g. v1.0 |
| `> Completed in Workshop N` | This field requires workshop output |
| `[CARRY FORWARD FROM X]` | Pull this value from the named template |
| `H / M / L` | Confidence rating — High, Medium, or Low |

---

## Versioning

Every template carries a version number and a date at the top. When a document is updated, because new data has come in, an assumption has changed, or a decision has been revised, bump the version number and note what changed.

The Assumptions Register is the most important document to version carefully. When Finance or Procurement asks which version of the model was used in the final recommendation, the answer lives there.

---

## Template index

### Working documents

| Template | Populated in | Depends on |
|----------|-------------|------------|
| assumptions-register.md | Workshops 1 through 5 | All workshops |
| data-request-list.md | Workshops 1 and 2 | Workshop 1 |
| cost-taxonomy-baseline.md | Workshop 2 | Workshop 1 |
| unit-metrics-definition.md | Workshop 3 | Workshops 1 and 2 |
| showback-view.md | Workshop 3 | Workshops 2 and 3 |
| value-risk-scorecard.md | Workshop 4 | Workshop 4 |
| workload-placement-matrix.md | Workshop 5 | Workshops 1 through 4 |
| scenario-comparison.md | Workshop 5 | All workshops |

### Decision brief

| Template | Populated after | Depends on |
|----------|----------------|------------|
| decision-brief-template.md | Workshop 5 | All working documents |

### 90-day plan

| Template | Populated in | Depends on |
|----------|-------------|------------|
| 90-day-plan-template.md | Workshop 5 | Scenario comparison |

---

## For facilitators

If you are running these workshops with a customer, the working documents should be shared with the platform team after each session, not held centrally and revealed at the end. Shared ownership of the documents throughout the process creates shared ownership of the outputs.

The decision brief and 90-day plan are produced by the facilitator after Workshop 5 and reviewed with the platform team before being shared with the leadership audience.

---

## For platform teams running the workshops independently

If your team is running the workshops without an external facilitator, the templates work the same way. Assign a document owner for each template, someone who is responsible for keeping it current between
sessions.

The Assumptions Register in particular should be updated after every workshop and shared with all attendees within 24 hours of each session.
