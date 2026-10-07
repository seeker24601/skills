---
name: acceptance-criteria
description: Turn goals and constraints into observable completion criteria and proportionate verification checks.
version: 0.1.0
classes: PLANNER
metadata:
  hermes:
    tags: [planning, review, verification]
    category: development
---

# Acceptance criteria

Use when a request or plan needs a clear definition of done.

1. Identify the user-visible outcome, inputs, affected users or consumers, explicit constraints, and exclusions. Separate requirements from suggested implementations.
2. Give each material requirement a stable label. Describe the starting condition, action or input, observable result, and boundary where the result matters. Use numerical thresholds only when supplied or justified; label proposed thresholds for agreement.
3. Pair each requirement with a feasible check and evidence source. Include important failure, cancellation, persistence, permissions, and compatibility cases where the change touches them. Prefer a few decisive checks to a large checklist of implementation details.
4. Separate pre-acceptance gates from observations available only after deployment. Assign an owner and timing to deferred evidence; never silently waive a required check.
5. Check for contradictions, untestable claims, hidden scope, and requirements with no owner. Return the criteria and only the open decisions that affect completion.

A criterion must permit failure. “Works correctly” and a screenshot of a data-producing screen cannot establish that another consumer received or persisted the data. Select evidence at the claimed boundary.
