# Review

Use to check implementation against a plan, review code, or approve or reject work against acceptance gates. Run only the checks relevant to the requested scope.

1. Identify the baseline, candidate revision including uncommitted changes, plan or specification version, approved amendments, project standards, authorship, and submitted evidence. Resolve material ambiguity and establish whether independent review is required. Keep the submitted artifact unchanged.
2. For plan checks, load `plan-conformance`. Trace requirements to implementation and evidence. Record satisfied, unmet, and unverified requirements; distinguish authorized deviations from omissions.
3. For code changes, load `code-review`. Inspect standards and specification separately. Delegate independent passes when useful, then verify findings against actual code and affected callers. Separate introduced defects from pre-existing issues and optional improvements.
4. For an acceptance decision, load `acceptance-gates` and apply the agreed policy. If none exists, disclose the skill's proposed assessment gates. Reuse credible evidence for the same candidate; run focused checks when evidence is stale, incomplete, contradicted, or inadequate for the risk.
5. Return actionable findings with locations, evidence, consequences, and coverage limits. When a verdict is requested, return APPROVE, REJECT, or BLOCKED with candidate and policy identifiers, gate results, missing proof, and corrections. A bounded review does not imply full acceptance. Candidate changes require reassessment of affected conclusions.
