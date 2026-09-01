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
5. Replace `TASK_HANDOFF.md` with status, outcome, decisions, changed files,
   checks, deferred ordinary or milestone evidence, preserved unrelated state,
   open points and the
   smallest useful next step.
6. Do not run a whitespace, targeted or full check merely because the handoff
   changed. Rerun only when it changed a governed input or covers a stated risk.
7. Exclude chat history, full tool output and facts already held by an
   authoritative document.

Report separately authorized Git actions as completed and all others as pending.
