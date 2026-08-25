---
name: handoff-task
description: Close or pause a repository task by writing a compact versioned handoff for later continuation, including cross-device continuation.
---

# Handoff Task

This skill does not authorize a commit, push or broader cleanup.

1. Classify the task as `completed`, `paused` or `blocked`.
2. Review the exact diff, staged state and validation evidence.
3. Ensure affected behavior has targeted evidence. Keep the full repository
   gate pending for commit preparation unless the local completion contract or
   an explicit risk decision requires it earlier.
4. Update durable project or decision documents only when the authorized work
   made them stale.
5. Replace `TASK_HANDOFF.md` with status, outcome, decisions, changed files,
   checks, full-gate state, preserved unrelated state, open points and the
   smallest useful next step.
6. Run `git diff --check` after the handoff update. Rerun a targeted or full
   check only when that update changed an input governed by the check.
7. Exclude chat history, full tool output and facts already held by an
   authoritative document.

Report separately authorized Git actions as completed and all others as pending.
