---
name: quick-fix
description: Ship the smallest workable temporary patch when speed matters more than completeness or long-term design.
version: 0.1.0
classes: ENGINEER
metadata:
  hermes:
    tags: [repair, workaround, delivery]
    category: development
---

# Quick fix

Use when the user requests a quick fix, bandaid, duct tape, temporary workaround, or an immediate unblock. Optimize time to a usable result. Accept technical debt, narrow coverage, duplication, and inelegant code when they shorten delivery. This mode replaces the normal root-cause repair workflow for the requested patch. Follow the Debug workflow routed by `AGENTS.md` for an ordinary bug report without a speed-first request.

## Patch and ship

1. Identify the immediate outcome and inspect only enough of the failing path to choose a bounded patch. Root-cause certainty is optional; distinguish what you observed from what you suspect. Ask only when missing information prevents a usable patch.
2. Choose the fastest plausible workaround: a local guard, fallback, narrow special case, rollback, or disabling an optional broken feature. Prefer changes that are easy to undo. Preserve user data, access controls, secrets, and unrelated work; speed does not expand permissions.
3. Implement immediately. Skip architecture work, broad investigation, refactoring, cleanup, useful extras, and speculative edge cases. Use a subagent only when an independent task will shorten delivery more than coordination costs.
4. Run the cheapest decisive check of the requested path and any mandatory project checks. Do not run broad suites by default. A patch must actually unblock the stated use case; if you cannot check that, say it is unverified.
5. If the patch fails its check, correct it or try the next bounded option. Stop widening the patch when it becomes a larger repair; explain the blocker and the fastest viable next step.

## Handoff

Keep the reply short: what works now, what remains fragile, and how to undo the patch. Label a workaround as temporary and name its known limitation. Identify the durable follow-up in one sentence when useful, then stop. Do not automatically begin `systemic-fix`, create a backlog, or claim the underlying cause is repaired.
