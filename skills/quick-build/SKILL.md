---
name: quick-build
description: Build a small working prototype quickly when the user wants a demo, experiment, proof of concept, or fast first version.
version: 0.1.0
classes: ENGINEER
metadata:
  hermes:
    tags: [engineering, prototyping, implementation]
    category: development
---

# Quick Build

Optimize time to a useful working result. Use for new prototypes and fast first versions. Follow `AGENTS.md` for scope, ownership, and authority. Use `quick-fix` for an urgent patch to broken behavior; use `workflows/build.md` when the requested result needs broader engineering rigor.

## Cut the scope

Identify the one interaction or uncertainty the prototype must prove. Choose the smallest complete path a user can try. Inspect the existing project, reuse its stack and components, and make reversible choices without a design committee. Ask only for missing information that would change the result.

Prefer a familiar dependency already installed, a direct implementation, and a small amount of explicit code. Delay frameworks, configurable systems, speculative abstractions, broad refactors, and infrastructure the experiment does not need. Avoid dependency shopping when a workable option exists. Set a short implementation target when useful; do not promise a deadline without evidence.

## Build the useful part first

Implement the main path end to end before optional polish. Use fixtures or local data where they answer the question faster, clearly label simulated behavior, and keep it replaceable. A stubbed integration must not appear connected. Never invent customer evidence, successful payments, saved data, or completed actions.

Check uncertain assumptions with the cheapest decisive experiment. If the approach stalls, inspect the failure and change it rather than piling on workarounds. Parallelize only independent work whose coordination cost is lower than the time saved. Keep the blocking interaction with the lead and verify the assembled result.

Speed comes from limiting scope. Preserve user data, secret handling, authorization, and explicit requirements. Keep necessary input validation and basic error feedback. Avoid adding public deployment, paid services, or destructive migrations to a local prototype without authorization. If the requested shortcuts would undermine the stated use, surface the conflict and use the appropriate Build process.

## Check and hand over

Exercise the main interaction in its actual interface, one likely failure, and relevant existing checks. Follow required repository checks. Add a focused test when it catches a consequential regression; skip broad test scaffolding for disposable presentation experiments. If execution is unavailable, state what remains unverified.

Deliver the runnable artifact or preview with brief run instructions, simulated pieces, and the few shortcuts that matter. Identify what must change before production use without turning delivery into a long backlog. Stop when the agreed experiment works; expand only for a requested next step. Never present a successful demo as proof of production readiness.
