---
name: systemic-fix
description: Repair the evidenced cause at its owning producer and cover equivalent failing paths instead of patching symptoms.
version: 0.1.3
classes: ENGINEER
metadata:
  hermes:
    tags: [debugging, root-cause, repair]
    category: development
---

# Systemic fix

Use for bug repairs, recurring failures, and proposed fixes that address only one instance. Establish the cause with `diagnose` before editing. Repair the code responsible for the failure and verify other paths affected by the same cause. Follow the Build workflow routed by `AGENTS.md` for implementation.

For an explicitly requested temporary patch or immediate unblock, use `quick-fix` instead. Return here when a durable repair is requested.

## Establish the owner

Reproduce the failure or identify a bounded substitute and its limits. Follow the input until decisive state is first lost, misinterpreted, or never committed. Corroborate the causal chain with a distinct observation. State what would disprove it. Do not turn a plausible diagnosis into a confident patch.

Identify the existing owner that should enforce the missing invariant. Before editing, enumerate affected writers, callers, consumers, and rendering paths. Check sibling inputs and transitions for the same cause. Repair all evidenced equivalent paths within scope; keep unrelated defects separate. Preserve one source of truth and existing system boundaries rather than adding a competing manager or store.

## Repair the cause

Make the smallest complete correction at the responsible producer or boundary. A guard is appropriate when it enforces the actual contract; a guard that only conceals lost state leaves the bug intact. Do not silence errors, weaken tests, add unsupported retries, or make consumers compensate for a broken producer. Remove obsolete workarounds once the invariant holds.

For failures after restart, inspect persisted configuration, caches, locks, serialization, and rehydration before assuming code changed. If a state reset changes the result, investigate state validation and migration. Do not delete user state to manufacture a passing result. For unresolved causes, use bounded instrumentation without secrets or destructive side effects during an authorized repair, or return to read-only diagnosis.

## Prove the repair

Keep a regression check that fails on the original defect and passes on the correction when feasible. Exercise the reported path, sibling cases sharing the cause, and relevant lifecycle transitions. Verify visible UI behavior in the actual interface when tools permit; unit tests alone do not prove it. Report unavailable checks and remaining uncertainty. A workaround must be labeled as such.

Review the final diff for duplicate ownership, unrelated edits, and new compatibility assumptions. Explain the cause, repair, and evidence briefly. Do not claim completion until the repaired invariant holds at the reported boundary, or clearly state the verification limit.
