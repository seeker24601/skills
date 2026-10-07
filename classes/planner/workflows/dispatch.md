# Dispatch

Use when asked to assign, route, resume, or check authorized work across companions. A request to dispatch authorizes its necessary assignment messages and board updates; use that authorization without asking again. A plan or backlog entry alone does not authorize sending work.

## Prepare the assignment

1. Read the identified plan and current board. Bind each card to a project, plan version, requested outcome, acceptance criteria, owner, dependencies, scope, and return route. Preserve existing work IDs and history when resuming.
2. Use the installed board tool to read current cards and a live contact lookup if the host exposes one. Select the exact registered target by role, relevant skills, access, and current assignment. User-facing names can change; retain the routing handle. The host-provided teammate roster is a fallback if contact lookup is unavailable. Never inspect another companion's private files or conversations to discover availability.
3. Check dependencies and shared writes. Dispatch independent assignments in parallel only when the user authorized distributing work to multiple companions. Serialize overlapping files, branches, mutable records, and producer/consumer work. Unknown overlap remains a scheduling conflict until resolved.
4. Record the assignment intent before sending. Include a concise composed handoff: work ID, plan version, goal, allowed scope, relevant source pointers, required checks, dependencies, restrictions, and expected reply. Share only task-relevant authorized material. Keep the destination's model and execution settings unchanged.

## Send and track

Use the host's `message_agent` tool with the registered `target` and composed `message`. This tool validates its target against the live roster and is available in a canonical Bot Chat. If it is missing or rejects the target, record the blocker and explain the missing route; do not invent a reply, switch to unrelated external messaging, or bypass the host through private state.

Record the returned delivery ID and exact acknowledgement state. A queued acknowledgement establishes a dispatch attempt only. It proves neither delivery nor acceptance. Follow the tool's reply-delivery instructions: ordinarily finish the turn and handle the asynchronous completion notification; use `process` to wait only when the acknowledgement explicitly requests polling. Do not repeatedly poll or resend while the outcome is unknown.

Record delivery only from actual transport confirmation or a recipient reply. Record acceptance only from the recipient accepting the assignment or observed work attributable to that card. Keep declines, delivery failures, and missing replies visible. Before retrying, inspect the existing receipt and confirm that retrying will not duplicate a live assignment. Reuse the work ID and unchanged scope; resolve ambiguous delivery before resending.

## Returns and continuation

Bind every return to its card, assigned target, candidate revision, result, evidence, and remaining work. A worker's completion claim moves work to review. Use `workflows/review.md` for the requested conformance or gate decision; mark completed only when the agreed acceptance evidence supports it. Preserve an independent reviewer requirement.

Record blocked work with its reason, dependency or missing decision, and next action. Record paused work when the user or owner pauses it; elapsed time never counts as permission to resume. Release dependent work only after its prerequisite is accepted or its acceptance contract explicitly permits the required intermediate handoff. Recheck scope, destination, conflicts, and authorization before each new send.

Board status records coordination; moving a card does not start, pause, cancel, or stop a recipient's running task. Use the host's supported control or an authorized message when execution must change, and distinguish the request from its confirmation. Reassignment must account for the previous worker and shared writes.

End with a short account of what was sent, which receipts are confirmed, what is awaiting acceptance or review, and any blocker. Do not promise background monitoring unless a real supported mechanism has been configured.
