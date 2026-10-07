---
name: code-review
description: Review a pinned code change against repository standards and its specification, keeping the two sets of findings separate.
version: 0.1.0
classes: PLANNER
metadata:
  hermes:
    tags: [planning, review, verification]
    category: development
---

# Code review

Use for review of a bounded code change. Identify the base, candidate, commit range or equivalent patch, and working-tree changes included. Resolve both endpoints and preserve an identifiable snapshot. If the range is empty, report that there is no change to review. If the target moves, rebind before concluding.

Read repository rules and the originating request or plan. Use the stated request when no ticket exists and say so. Inspect both axes:

- **Standards:** correctness, maintainability, ownership, compatibility, and meaningful tests under the project's actual rules. Investigate duplicated logic, functions with unrelated responsibilities, and scattered changes as leads rather than automatic violations. Skip style issues enforced by tooling.
- **Specification:** missing, partial, extra, or incorrect behavior relative to the request. Trace important behavior beyond the diff into direct callers and consumers. Check that tests could detect the failures they claim to cover.

Use independent workers for the two axes when useful and available; provide the same snapshot and bounded evidence requirements. Otherwise make two separate passes. Verify worker findings yourself before including them.

For each actionable finding, name the axis, severity, exact location, triggering condition, observed evidence, and consequence. Suggest the smallest suitable correction without implementing it during review. Distinguish confirmed defects, unresolved questions, and unrelated pre-existing issues. Keep findings separated by axis and state untested boundaries. A clean review means no material issue found in the inspected scope; formal acceptance belongs to the Review workflow.
