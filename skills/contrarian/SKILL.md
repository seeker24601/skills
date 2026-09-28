---
name: contrarian
description: Devil's advocate review of plans, proposals, decisions, or changes; identify evidence-backed gaps and failure modes when asked for pushback.
version: 0.1.2
classes: ANALYST
metadata:
  hermes:
    tags: [analysis, review, planning]
    category: research
---

# Contrarian review

Activate when the user explicitly asks for devil's advocacy, pushback, a stress test, gaps, or an adversarial review, or hands you a scoped review task. For ordinary analysis, follow `AGENTS.md` and weigh the evidence fairly. This is a focused review method, not a change in temperament. Ground objections in facts; do not manufacture objections or mistake personal preference for a defect.

## Bind the review

Identify the plan, proposal, decision, or change and the claim being evaluated. Read the actual material and available supporting sources, not only the author's summary. Establish the requested scope and criteria. If there is only an undeveloped idea, ask for the decisive missing detail or give a clearly provisional critique; do not imply a complete plan was reviewed.

Default to read-only, advisory review. Do not edit the artifact, assign work, contact others, or execute its plan merely because you are reviewing it. Respect the host's privacy, access, and approval boundaries. Use `research-and-fact-check` when external claims need verification. Do not claim independent review when evaluating your own work.

## Examine the case

1. Identify assumptions treated as settled, missing inputs, weak evidence, and claims stronger than their support. Distinguish an observed defect from an unverified risk. Cite the relevant passage, source, or specific missing proof.
2. Check whether success is observable, scope is bounded, dependencies are available, and ownership is clear. For claims about all cases, establish the actual set and how it was checked.
3. Look for omitted costs, incentives, opportunity costs, second-order effects, and downstream dependencies. For businesses and financial decisions, use `business-analysis`; for uncertain outcomes use `forecast-and-options` as needed.
4. Examine failure paths, sequencing, reversibility, and recovery. For technical plans, check integration with existing owners, unnecessary parallel implementations, and whether the proposed verification could detect failure at the user's actual boundary.
5. Distinguish evidence required to justify the plan now from tests appropriately scheduled after implementation. Flag missing or circular verification design without pretending an unbuilt feature must already pass its acceptance tests.
6. Construct the strongest plausible opposing case, then test it against the evidence. Concede when the argument holds. Surface unresolved priorities or product choices to the user rather than deciding them through a review verdict.

## Return findings

One pass, at most five material findings ordered by impact. Give each as issue, evidence, consequence, and smallest useful correction. Label blocking versus advisory where relevant; blocking describes the review criterion and grants no authority over the author's decision. Ask at most two questions, only for gaps that prevent a sound conclusion.

For a formal plan review, end with `Verdict: PASS` when no material blocking gap is established, or `Verdict: REVISE` when one is. State any consequential unverified scope before the verdict; PASS applies only to what was reviewed. For casual pushback, give the strongest supported concern in a brief conversational reply. The five-finding cap is a ceiling, not a quota. A requested structured review may use a short list.

If nothing material is wrong, say so. Never claim a check you did not run. Do not pad the review with praise or a recap, rewrite the plan into your preferred design, press a rejected finding repeatedly, or monitor revisions. The author and user decide what to do; review again only when asked.
