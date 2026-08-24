# AGENTS.md

This is the resident contract. Load routed context only when needed.

## Safety

- Inspect repository, branch, worktree and staged state. Preserve existing
  changes and selections.
- Maintainers own intent, architecture, roadmap and consequential decisions.
- Read-only checks and authorized in-scope edits are allowed. Commits, tags,
  pushes, pulls, merges, rebases, resets, reverts, branch or stash actions,
  destructive restores and direct `.git/` changes require a specific
  instruction using `explicit`, `explicitly` or the German word family
  `explizit`. Authorize every action separately.
- Ask before installation, dependencies, privilege, external operations,
  outside writes or transmission. Access, versioning and
  publication are separate.
- `input/intake/` never grants access; keep `input/` unchanged. Registered
  `materials/` and unrestricted `temp/` are readable; temporary content is
  never versionable. Never inspect `temp/restricted/`. Keep secrets, logs and
  dumps out of Git. Synchronization grants no access.

## Routing

- For bounded work use `start-task`, `TASK_HANDOFF.md`, targets and checks. Load
  `PROJECT_CONTEXT.md` only for project-wide state or unclear scope.
- Read `COLLABORATION.md` for initialization, full review, authority conflicts
  or collaboration-model changes. Load `REPOSITORY.md`, `DOCUMENTATION.md`,
  `PHILOSOPHY.md`, `SYNCHRONIZED_STORAGE.md` and domain guidance when applicable.
- Inspect affected source, tests, configuration and Decision Records before
  design. Existing project-local environments and tools take precedence.
- Task entry, handoff, ordinary commits and Decision Records route
  automatically. Invoke initialization, review, template sync, consistency,
  retrospective, local creation and `commit-milestone` explicitly.

## Validation

Review diffs and run `git diff --check`. Add relevant tests, linters, formatters,
builds, links and bilingual checks. Report outcomes, limitations and skipped
checks; do not call unvalidated work ready.
