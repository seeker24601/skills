---
name: double-check
description: Review completed or proposed work against current sources to catch missed requirements, unsupported claims, and regressions.
version: 0.1.0
classes: ENGINEER
metadata:
  hermes:
    tags: [review, verification, regression]
    category: development
---

# Double check

Use when asked to double check, review work again, or verify a result before handoff. Reconstruct expectations from current sources instead of trusting the first-pass summary. Default to review-only; repair only when the parent task authorizes edits. Scale the review to the changed behavior and its risk. An explicitly temporary workaround is judged against its stated purpose and limits.

## Bind the target

Identify the requested outcome, acceptance criteria, exact files or change set, baseline, claimed checks, and exclusions. State missing baselines or inaccessible evidence. Read the governing instructions and actual implementation; turn important claims into observable checks. Review code, documents, plans, configuration, or data as appropriate to the request.

## Inspect and challenge

Inspect the change and its direct producers, consumers, and shared owners. Look for omitted requirements, contradictions, renamed contracts with stale callers, and locally correct parts that fail together. Check combined states, errors, retries, cancellation, persistence, and lifecycle transitions where relevant.

Start with the cheapest decisive check at the highest-risk boundary. Exercise the real public path and an affected older behavior. Prefer focused existing tests or probes over broad suites. A mock, helper test, label, or successful build cannot prove a different boundary. Inspect rendered UI to establish visibility.

For a regression test central to the claim, confirm it fails with the original defect present when feasible. Use an isolated scratch copy for deliberate mutations. If authorized mutation requires touching working files, preserve their exact current contents and guarantee restoration on failure or interruption. Never restore uncommitted work from the committed version. Report mutations not performed and the resulting evidence limit.

Use the same repeatable checks after a repair. Verify that the evidence belongs to the final reviewed candidate. If another edit changes the target, review that candidate again before issuing a verdict. Separate introduced regressions, baseline failures, intended changes, and unverified behavior. Timeouts and skipped checks are not passes.

## Report or repair

Lead with PASS, REVISE, or BLOCKED, followed by a short explanation. PASS means no material regression found within the reviewed scope; REVISE means an actionable defect or unsupported claim; BLOCKED means decisive evidence is unavailable.

For each finding, give its severity, failed expectation, concrete evidence, affected boundary, and smallest appropriate correction. Summarize checks and remaining limits; state whether anything changed. Keep a clean review brief and do not claim untested behavior is safe.

When repair is authorized, use `diagnose` if the cause remains uncertain and `systemic-fix` for durable correction, then rerun the review. Preserve an explicitly requested `quick-fix` scope. Do not widen the task or change external state merely to complete the review.
