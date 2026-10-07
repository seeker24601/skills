---
name: acceptance-gates
description: Issue a scoped acceptance verdict from explicit gates and inspected evidence tied to the submitted revision.
version: 0.1.0
classes: PLANNER
metadata:
  hermes:
    tags: [planning, review, verification]
    category: development
---

# Acceptance gates

Use for an acceptance decision on completed work. Bind the candidate snapshot, baseline, requirements or plan version, applicable gate policy, and authorship. An independent gate requires a reviewer who did not implement the submitted change. Disclose participation; if independence is required and unavailable, return BLOCKED and request a separate reviewer.

Use the project's explicit gates. In their absence, disclose these assessment gates before applying them:

1. **Scope and structure:** the change fulfills the agreed outcome and constraints, reuses appropriate owners, and accounts for material additions or deviations. Apply actual project limits rather than inventing numeric thresholds.
2. **Evidence:** material claims have credible inspected checks on the submitted bytes and integration composition. Skipped, stale, or missing results remain unverified. Reuse current evidence; repeat checks when there is a concrete reason to doubt applicability or coverage.
3. **Affected boundaries:** inspect relevant permissions, secrets, data handling, recovery, public interfaces, and consumer behavior. Require persistence evidence across reload when persistence is claimed. Keep checks proportional to changed surfaces.
4. **Handoff:** the artifact is available in the agreed destination, changed instructions or documentation remain accurate, and the completion claim matches the candidate. Local delivery is sufficient when that is the requested destination.

Evaluate in order. At a failed gate, report its material findings and mark later gates UNRUN unless additional inspection is useful and explicitly reported. A later success cannot cancel a required gate failure. Post-release observations may remain deferred only when the acceptance contract permits it; name the owner and timing. Missing access to mandatory evidence blocks a verdict rather than converting it into a pass.

Return **APPROVE** only when all required gates are supported. Return **REJECT** for an established gate failure, with the requirement, evidence, and correction needed. Return **BLOCKED** when a required decision, independence, access, or evidence is unavailable. If a known failure coexists with missing evidence, return REJECT and disclose the unverified gates.

Include the candidate and policy identifiers, gate statuses, inspected evidence, and limits. Approval covers that scope and revision only. Repairs change the candidate and require reassessment. Do not modify the submitted work, invent checks, grant tool permissions, or merge or deploy as part of this verdict.
