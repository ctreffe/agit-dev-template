---
name: commit-changes
description: Finalize an ordinary reviewed change as a scoped Git commit and optionally push it. Do not use for version or milestone closure.
---

# Commit Changes

Confirm repository scope, working-tree state, staged selection and changed
hunks. Preserve unrelated and pre-existing changes. Reuse current evidence
while governed inputs have not changed.

An ordinary commit needs a good, targeted and reviewable state, not a complete
repository gate. Select the smallest check or review that materially increases
confidence in the changed behavior, text or contract. Automated tests,
whitespace checks, broad renders, builds and full suites are optional unless
affected or required by a stated material risk. A failed relevant check must be
diagnosed and rerun after an in-scope fix. Keep success output concise and
retain focused failure diagnostics. Member repositories do not run the family
validator; possible shared consequences become a Governance follow-up.

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
