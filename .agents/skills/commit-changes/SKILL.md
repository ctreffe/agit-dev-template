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
failure diagnostics.

Then present and check the complete proposed message. An ordinary summary uses
one exact direct prefix from `feat:`, `fix:`, `docs:`, `chore:`, `refactor:`,
`test:`, `ci:` or `build:` followed by a concise imperative summary. Scoped
forms such as `feat(scope):` do not satisfy this repository-family convention.
Provide a meaningful body that explains purpose, material changes, important
boundaries and relevant validation without merely repeating the summary. Use
real line breaks and reject literal `\n` escape text. Milestone metadata is
handled only by `commit-milestone`.

Create the commit only after action-specific authorization required by the
repository. Verify the resulting commit, including its complete message, and
the remaining working tree. A push is a
separate protected action: perform it only when separately authorized, then
verify local HEAD and the intended upstream revision.

Stop instead of silently widening scope, repairing unrelated failures or
including files that were not reviewed.
