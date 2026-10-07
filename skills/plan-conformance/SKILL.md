---
name: plan-conformance
description: Trace an identified implementation to plan requirements and evidence, exposing omissions, deviations, and unverified claims.
version: 0.1.0
classes: PLANNER
metadata:
  hermes:
    tags: [planning, review, verification]
    category: development
---

# Plan conformance

Use to compare completed or partial work with an identified plan.

Bind the plan version and approved amendments to the exact candidate: commit IDs or an equivalent artifact snapshot, including local changes. Read the actual implementation and checks. A task checkbox or author summary is a pointer to evidence.

Build a compact trace for each material requirement: requirement label, implementation location, evidence, and status. Use SATISFIED when relevant evidence supports the requirement, UNMET when observed behavior contradicts it or implementation is absent, and UNVERIFIED when decisive evidence is missing. Record PARTIAL only with the specific satisfied and remaining portions.

Trace through the affected producers, consumers, shared owners, and persistence boundaries. Check omissions, conflicting requirements, unauthorized additions, changed assumptions, and deviations from agreed constraints. Equivalent implementation choices may satisfy the outcome; do not reject them solely for differing from an illustrative plan sketch.

Check that evidence applies to the same bytes, configuration, and integration composition. Reuse credible current results. Run authorized focused checks where a consequential claim remains unsettled, and describe any access or environment limit.

Return the material gaps and the trace needed to locate them. Propose a correction or an explicit plan amendment where appropriate; never silently rewrite the plan to match the implementation. This conformance record supplies evidence to an acceptance decision and does not authorize changes or release.
