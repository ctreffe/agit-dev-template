# AGENTS.md

Resident contract.

## Safety

- Inspect repository, branch, worktree and staging; preserve changes and
  selections.
- Maintainers own intent, architecture, roadmap and consequential decisions.
- Authorized reads and edits are allowed. Commits, tags, pushes, pulls, merges,
  rebases, resets, reverts, branches, stashes, destructive restores and direct
  `.git/` changes each require an instruction containing `explicit`,
  `explicitly` or German `explizit`.
- When such a control-word instruction is needed, propose one minimal copy-ready
  wording that names the exact action, repository and material consequence;
  the proposal is not authorization.
- Ask before dependencies, installation, privilege, external operations,
  outside writes or transmission; access, versioning and publication differ.
- Retry once if plausibly transient. On recurrence or setup/policy error, pause;
  use `troubleshoot-environment`; authorize, repair, verify and resume.
- `input/intake/` grants no access; keep `input/` unchanged. Registered
  `materials/` and unrestricted `temp/` are readable; never version temporary
  content or inspect `temp/restricted/`. Keep secrets, logs and dumps out of
  Git. Synchronization grants no access.

## Routing

- Bounded work uses `start-task`, `TASK_HANDOFF.md`, targets and checks. Load
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

Scale evidence by stage: a bounded change needs the smallest useful behavioral
or source review, an ordinary commit needs targeted evidence for a good
reviewable state, and a milestone commit owns comprehensive engineering and
release checks. Tests, linters, formatters, builds, whitespace, links and
bilingual scans are not defaults before the milestone unless affected or
required by a stated material risk. Report limits and deferred checks truthfully.
