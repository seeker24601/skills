---
name: build
description: Build and refine software and websites, from implementation through tests and browser verification.
version: 0.2.1
classes: ENGINEER
metadata:
  hermes:
    tags: [engineering, implementation, verification]
    category: development
---

# Build

Use for building or changing software, websites, and web interfaces. Use `debug` when existing behavior fails. Use the web workflow below when the task includes a browser interface. These instructions grant no additional tools or permissions.

## Orient

Read project instructions, inspect the working tree, and identify the requested outcome and observable acceptance criteria. Trace the existing implementation and its callers before choosing where to edit. Preserve unrelated user changes. Find the normal run, build, and test commands. Ask only for consequential missing information; choose and state reasonable assumptions for reversible details.

## Choose and implement

1. Extend the existing owner of the behavior. Reuse suitable functions, components, and dependencies. Compare alternatives when the choice matters; prefer the simplest design that meets the actual requirements.
2. Break uncertain work into small experiments with a concrete observation that will decide the next step. Try another supported approach when one fails. Avoid repeating a failed attempt without new evidence. Report a real blocker with its evidence and the smallest missing prerequisite.
3. Build a complete usable path in verifiable increments. Keep data flow and state ownership clear. Consider invalid inputs, errors, partial results, and cleanup. For persistence or concurrent work, consider retries, duplicate actions, interrupted writes, and ownership of shared state.
4. Keep edits tied to the requested outcome. Avoid speculative frameworks, unnecessary dependencies, or unrelated rewrites. Prototype uncertain ideas cheaply, then integrate or remove the experiment rather than leaving competing implementations.
5. Proceed autonomously within authorized scope. Respect host approval rules, secrets, and release boundaries. A blocked permission is not a reason to find a bypass. Do not publish, deploy, delete unrelated work, or make external commitments without the required authorization.

## Parallelize useful work

Use available subagents when independent work can finish sooner in parallel. Before delegating, identify dependencies and keep the next blocking step with the lead. Delegate bounded tasks such as separate components, focused research, or independent verification while continuing useful work yourself. Handle small or tightly coupled edits locally when coordination would take longer.

Give each subagent the outcome, relevant context, acceptance checks, allowed files, and required return evidence. Assign non-overlapping write ownership; agree shared interfaces before parallel implementation. Serialize edits to shared files or use supported isolated worktrees. Never assume isolation or tools the host does not provide.

Use only as many workers as the task and available capacity justify. Avoid duplicate investigations, speculative work, and delegation chains without a concrete benefit. Check progress at dependencies, unblock workers, and stop obsolete tasks when scope changes.

Review returned changes, resolve conflicts, and verify the integrated result before reporting completion. A subagent's success report is not proof. If delegation is unavailable, continue locally without claiming parallel execution. Delegation does not expand permissions or the user's scope.

## Websites and web interfaces

- Identify the audience, page purpose, and main action. Give a brief design direction before editing. Reuse the existing design system and stack. Personal taste must not silently decide the user's branding.
- Connect real navigation and the main interaction. Label placeholders and unavailable integrations. Never invent testimonials, results, or business facts.
- Support narrow and wide screens with semantic controls, labeled inputs, readable contrast, visible keyboard focus, and useful validation. Respect reduced motion. Keep essential content readable through decorative effects.
- Start the project's local preview. In an available browser, exercise the main path, error and empty states, keyboard access, narrow-screen overflow, image framing, links, and forms. If browser tools are unavailable, report visual and interaction checks as unverified.
- A working form needs a destination. Explain what happens to submitted data. A polished mockup still needs working controls or explicit limitations.
- Deliver the local preview and identify unfinished integrations. Keep the site local unless the specific publishing action is authorized. Report browser checks separately from build checks.

## Add a useful extra

Always look for one small improvement beyond the literal request. Finish the requested behavior first, then include a relevant finishing touch: a helpful empty state, a keyboard shortcut that fits the existing controls, a clearer error, or a nearby edge case handled properly. Choose something the user will benefit from immediately and verify it alongside the requested change. Keep the extra proportionate; do not add features merely to show off.

Respect explicit scope limits. Extras must not introduce dependencies, ongoing costs, external actions, destructive changes, or substantial maintenance without authorization. If no useful extra fits, give one brief, concrete observation or optional suggestion instead of changing more code. Mention a shipped extra in a short clause.

## Verify and deliver

Exercise the requested behavior at its actual boundary. Run relevant existing checks and inspect the final diff for omissions or regressions. Add meaningful tests for new logic and failure behavior where warranted; avoid tests that merely repeat implementation details. Use the project's required checks. A passing build alone does not verify a user interaction.

Fix failures introduced by the change. Separate pre-existing failures and unavailable checks from verified results. Deliver the working artifact or local preview with a short account of what changed and the material limit. Do not claim a test, deployment, or review that did not happen.

Use Hermes skill management to retain reusable procedures, corrections, and pitfalls when useful. Keep task-specific learning in the relevant skill and private project details in their authorized home; never copy secrets into reusable instructions.
