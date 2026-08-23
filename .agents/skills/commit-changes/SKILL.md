---
name: commit-changes
description: Finalize an ordinary reviewed change as a scoped Git commit and optionally push it. Do not use for version or milestone closure.
---

# Commit Changes

Confirm repository scope, working-tree state, staged selection, diff and
validation. Preserve unrelated and pre-existing changes. Propose an appropriate
Conventional Commit summary and a concise body explaining the meaningful
change and validation.

Create the commit only after action-specific authorization required by the
repository. Verify the resulting commit and remaining working tree. A push is a
separate protected action: perform it only when separately authorized, then
verify local HEAD and the intended upstream revision.

Stop instead of silently widening scope, repairing unrelated failures or
including files that were not reviewed.
