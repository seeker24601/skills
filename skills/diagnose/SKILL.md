---
name: diagnose
description: Investigate failures read-only across the failing boundary, surrounding interactions, and architecture before choosing a repair.
version: 0.1.2
classes: ENGINEER
metadata:
  hermes:
    tags: [debugging, diagnosis, investigation]
    category: development
---

# Diagnose

Use when a cause is unclear, a failure crosses components, or the user requests investigation without changes. Gather evidence without modifying the system. When repair is authorized and the cause is established, continue with `systemic-fix`.

## Read-only boundary

Do not edit source, tests, configuration, documents, data, branches, or runtime state. Do not install dependencies, restart services, clear caches, or call mutating interfaces. Run an existing probe only when known to be self-contained and non-mutating; otherwise inspect it and state what remains untested. Preserve concurrent work. Capture the source reference and working-tree state without exposing secrets.

## Establish the evidence

Record the symptom, expected and observed behavior, input, environment, timing, relevant artifacts, project root, and constraints. Find the smallest reproducible boundary or explain why reproduction is unsafe or unavailable. Keep facts separate from hypotheses. If your recent change might have caused the failure, examine it early.

## Inspect three scales

Use available delegation for independent passes when warranted. If unavailable, run the passes yourself in sequence and note that independence is limited. Do not invent worker results or spend the task repairing delegation. Give workers the same factual evidence and artifact paths, without a leading causal conclusion. Unless the task needs a different bound, limit each pass to 12 files, 8 targeted read-only commands, and 5 minutes. Avoid broad suites, builds, and open-ended searches.

1. Failure boundary: trace the input, state transition, producer, consumer, and output. Find the earliest observed divergence. Identify plausible competing causes and evidence that would disprove each.
2. Surrounding interactions: inspect callers, sibling paths, shared state, ordering, retries, caches, subscriptions, identity, and lifecycle transitions. Check whether locally correct components impose incompatible contracts. Inspect at least one sibling path.
3. Architecture: independently identify the intended source of truth and mutation authority. Trace process, persistence, and public boundaries. Look for duplicated ownership, hidden coupling, stale contracts, or a local fix that would violate an invariant.

With delegation, run the boundary pass first, then the other two in parallel using factual path discoveries only. Each pass returns its scope, budget, cited observations, hypotheses, falsifiers, contradictions, unknowns, and read-only confirmation. Keep partial evidence when a pass fails or times out.

## Reconcile and hand off

Recheck that evidence describes the same source state. Separate agreement from unsupported claims and unresolved contradictions. Prefer the earliest evidenced divergence. Classify the leading cause as a local defect, interaction conflict, architectural mismatch, environment/data issue, or unresolved. State the causal chain, responsible owner, confidence, viable alternatives, and cheapest decisive next proof. Use high confidence only when the chain is established and viable alternatives are ruled out. At most one targeted follow-up should resolve a material disagreement; otherwise preserve the uncertainty.

Compare the final working-tree state with the baseline. Report differences without reverting concurrent work or assuming you caused them. Keep detailed evidence in working notes or an explicitly requested report; give the user a brief conclusion and material uncertainty. Never say a diagnosis fixed anything. For an authorized repair, load `systemic-fix` with these findings. An investigation-only request ends here.
