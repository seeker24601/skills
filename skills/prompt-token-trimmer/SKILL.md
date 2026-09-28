---
name: prompt-token-trimmer
description: Shorten eligible synthesized or LLM-facing notes while preserving evidence, constraints, and useful meaning.
version: 0.1.0
classes: ARCHIVIST
metadata:
  hermes:
    tags: [archive, records, knowledge, maintenance]
    category: productivity
---

# Prompt Token Trimmer

Use to reduce repetition and context cost in synthesized or LLM-facing notes. Optimize readability and precision together with length; do not impose arbitrary word limits.

## Eligibility and authority

Do not trim or split raw transcripts, logs, original source documents, append-only or historical records, generated or protected content for size. User-facing prose, including creative writing, is exempt. Preserve these whole and shorten a separate synthesis when appropriate. Changing agent instructions or skill semantics is outside this archive method.

A direct request to shorten a specified eligible note authorizes that edit within its stated constraints. When shortening is only a suggested improvement outside the request, show a compact proposal with meaningful before/after wording and obtain approval before editing. Never discard unique evidence or alter a decision to save tokens. Respect narrower local preservation rules.

## Method

1. Read the complete target and enough linked context to identify its purpose, canonical owner, and consumers. If content is truncated, retrieve the missing scope before rewriting.
2. Identify duplicate statements, process narration, empty introductions, redundant examples, and explanations already owned by a linked page. Remove repetition; preserve exceptions and examples that prevent a known misunderstanding.
3. Keep requirements, prohibitions, scope, authority, negations, ordering, schemas, field names, paths, IDs, commands, citations, dates, uncertainty, correction history, and verification criteria. Do not replace precise instructions with vague advice or opaque abbreviations.
4. Write direct, readable statements. Link to canonical detail when the shortened note remains useful on its own. Do not delete useful context solely because another reader could search for it.
5. Compare the revision against the original for lost claims, qualifications, evidence, and relationships. Save using the latest content hash; reconcile concurrent changes rather than overwriting them. Read back and check links.

Report what changed and where, with any unresolved trade-off. Claim token savings only when measured with an appropriate tokenizer; word or character counts are not token counts.
