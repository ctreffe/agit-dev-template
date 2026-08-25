---
name: commit-changes
description: Finalize an ordinary reviewed change as a scoped Git commit and optionally push it. Do not use for version or milestone closure.
---

# Commit Changes

Confirm repository scope, working-tree state, staged selection and diff.
Preserve unrelated and pre-existing changes. Classify the semantic scope, not
only the changed paths, and select the repository's complete validation gate.
That gate is mandatory at ordinary commit preparation. In Templateverse
governance, use the focused governance validator for governance-local changes;
use selected-repository checks and the family validator for coordinated or
shared-family changes. Domain validation remains additive.

Run the selected full gate after the last relevant correction. A failure must
be diagnosed and rerun after an in-scope fix; do not replace it with targeted
checks or `git diff --check`. Keep successful output concise while retaining
failure diagnostics. Then propose an appropriate Conventional Commit summary
and a concise body explaining the meaningful change and validation.

Create the commit only after action-specific authorization required by the
repository. Verify the resulting commit and remaining working tree. A push is a
separate protected action: perform it only when separately authorized, then
verify local HEAD and the intended upstream revision.

Stop instead of silently widening scope, repairing unrelated failures or
including files that were not reviewed.
