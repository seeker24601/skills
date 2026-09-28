---
name: debug
description: Reproduce failures, establish their cause, repair the owning code, and verify regressions.
version: 0.1.4
classes: ENGINEER
metadata:
  hermes:
    tags: [debugging, diagnosis, regression]
    category: development
---

# Debug

Use for bugs, regressions, crashes, unexpected behavior, and failing checks. Use `build` if the investigation reveals a request for new behavior, or for browser verification when relevant.

For an explicit speed-first workaround, use `quick-fix` instead of the investigation and systemic repair sequence below.

## Investigate

Load `diagnose` before choosing a repair. It owns read-only evidence gathering, the three investigation scales, competing hypotheses, and confidence. Preserve its distinction between observed facts and suspected causes. For an investigation-only request, return the diagnosis and stop without editing.

## Repair

When repair is authorized and the cause is sufficiently established, load `systemic-fix`. It owns producer-level correction, sibling-path coverage, restart/state failures, and regression proof. Use `build` for implementation and web-interface verification. Return to diagnosis if repair evidence contradicts the causal model.

## Deliver

Report the cause, repair, and evidence briefly. Distinguish a workaround from a verified fix and state remaining uncertainty. Save reusable debugging lessons through Hermes skill management when useful, keeping private data and secrets out of reusable skills.
