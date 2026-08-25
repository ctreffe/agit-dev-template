---
name: start-task
description: Start a new bounded repository task with lean context reconstruction. Use for ordinary objective changes, not comprehensive project or governance reviews.
---

# Start Task

Establish only the context needed for the requested objective.

1. Read the closest repository instructions and current `TASK_HANDOFF.md` when
   present. Treat a stale or unrelated handoff as non-authoritative.
2. Inspect branch, working tree and staged state without changing them.
3. State the outcome, repository scope and important non-goals.
4. Read the target files and only directly applicable authority, domain,
   decision and validation material. Identify targeted checks, the repository's
   full validation gate and any reason that gate must run early.
5. Perform the bounded work and run targeted checks for the affected behavior.
   Do not run a full repository or family validator merely because the task
   started. When validation itself changes, exercise the affected validator in
   the narrowest useful scope. Escalate to the complete gate before commit
   preparation only when the local completion contract or an explicit risk
   decision requires it.
6. Report targeted evidence and every full gate as passed, failed, pending or
   not applicable without implying that a deferred gate passed.

Escalate to the repository's review skill only when identity, authority or
current state cannot be established safely through this route.
