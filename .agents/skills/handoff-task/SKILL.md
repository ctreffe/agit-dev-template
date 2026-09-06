---
name: handoff-task
description: Close or pause a repository task by writing a compact versioned handoff for later continuation, including cross-device continuation.
---

# Handoff Task

This skill does not authorize a commit, push or broader cleanup.

1. Classify the task as `completed`, `paused` or `blocked`.
2. Review the changed hunks, staged state and current evidence. Repeat Git-state
   inspection only when relevant state changed or the handoff is a new boundary.
3. Ensure the affected behavior or text has proportionate evidence. Record
   ordinary-commit and milestone checks as deferred when they were not needed.
4. Update durable project or decision documents only when the authorized work
   made them stale.
5. Replace `TASK_HANDOFF.md` with status, outcome, decisions, change scope,
   checks, deferred ordinary or milestone evidence, preserved unrelated state,
   substantive open points, the smallest useful continuation and a versioning
   boundary.
6. Keep a completed handoff commit-stable when it is intended for the same
   scoped commit as the work it describes. Do not assert that tracked changes
   remain uncommitted or unstaged, and do not make review, commit or push the
   task's next step. State that no task work remains when applicable and that
   later versioning decisions use live Git state.
7. Record exact working-tree or staging state only when a `paused` or `blocked`
   task genuinely depends on preserving it. Label that state as observed at
   handoff creation and require live reconciliation on resume.
8. Do not run a whitespace, targeted or full check merely because the handoff
   changed. Rerun only when it changed a governed input or covers a stated risk.
9. Exclude chat history, full tool output and facts already held by an
   authoritative document.

The handoff step authorizes no commit or push. Report already completed,
separately authorized Git actions as historical facts; otherwise keep
versioning as a boundary rather than a pending task or substantive open point.
