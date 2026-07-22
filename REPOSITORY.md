# REPOSITORY.md

# Repository Standards

This document describes repository-level standards used by the AGIT Dev Template.

It focuses on repository organization, Git usage, versioning, release handling and repository-ready delivery for projects created from the template.

---

# Repository Naming

Repository names should be clear, descriptive and stable.

For new AGIT repositories, prefer kebab-case names, for example:

```text
agit-project-template
agit-dev-template
agit-windows-deployment-kit
```

Repository names should describe the project without unnecessary marketing language.

A repository name should remain useful even if the project grows over time.

---

# Repository Description

The repository description should briefly explain what the project is.

Prefer precise technical language.

Avoid promotional wording, exaggerated claims or vague statements.

A good repository description helps a visitor quickly understand the scope of the project.

---

# README Badge Policy

Template repositories use a compact badge block directly below the README
title and before the AI Collaboration Note. The standard semantic order is
status, version and license, followed only by badges for real build, test or
documentation automation.

Status links to `VERSION`, version links to `CHANGELOG.md` and license links to
`LICENSE`. Public repositories may use dynamic GitHub metadata; private or
proprietary repositories may use static badges updated during milestone
closure. Avoid a last-commit badge because recent activity is not a quality,
validation or release signal.

Derived projects adapt the badges to their own documented status, completed
version, actual license and available automation. They do not retain the AGIT
Dev Template version as the project version and do not advertise checks or
releases that do not exist. English and German badge blocks remain identical
when both READMEs are maintained.

---

# Repository as Source of Truth

The repository is the authoritative project state.

Project decisions, current status and reusable knowledge should be captured in repository files and records rather than relying on chat history.

When AI assistance is used, work should begin from a clearly identified repository baseline:

- the local repository working tree, if accessible to the assistant and intended as the source of truth
- the current public repository state, if accessible
- a ZIP archive supplied by the maintainer
- a previously generated file explicitly accepted as the new baseline

If the baseline is unclear, do not prepare repository-ready changes until it is clarified.

Use `CONTINUATION_PROMPT.md` at the start of a new context window or assistant
session to reconcile `PROJECT_CONTEXT.md` with current read-only Git evidence.

---

# Git Client

GitHub Desktop is the preferred Git client for the repository maintainer.

Repository guidance should avoid assuming command-line Git usage whenever practical.

Command-line Git may still be used when needed, but documentation should not depend on it unless there is a clear reason.

When Codex is used locally, `CODEX.md` defines the allowed Git usage. By
default, Codex may inspect Git state. Specifically requested staging and
unstaging do not require a control word; protected Git actions do.

This is a hard collaboration rule, not only a Codex implementation detail.
Assistants may prepare working tree changes, propose commit boundaries and
suggest commit summaries and descriptions. Staging and unstaging require a
specific maintainer request or authorization of the corresponding commit, but
no control word; existing staged selections and unrelated changes must be
preserved. Assistants must not create commits, amend commits, rebase, reset,
revert, create or delete branches, create
or delete tags, push, pull, merge, manipulate stashes or perform another
protected Git action unless the
maintainer instructs the assistant to perform that specific action and uses a
recognized control word: `explicit` or `explicitly` in English, or the German
word family `explizit`, including `explizite`, `expliziten`, `expliziter` and
`explizites`.

Approval for file edits is not approval for protected Git actions. Approval for
one protected action is not approval for another. Requests such as "commit this",
"create the commit", "tag this" or "push this" do not authorize the assistant to
run protected Git commands unless they contain a recognized control word.

---

# Branching Strategy

For small projects maintained primarily by a single repository owner, commit directly to `main`.

Feature branches and pull requests are optional and should only be introduced when they provide practical value.

For projects with multiple active human contributors, branches and pull requests may be used to support review and coordination.

The workflow should remain as simple as possible while preserving a clean and understandable project history.

---

# Commit Messages

Every commit should have:

- a concise summary
- a meaningful description

The summary should describe the primary purpose of the change.

The description should describe the actual diff introduced by the commit and explain the reason for the change when it is not obvious.

Commit descriptions should not repeat unrelated project history or describe future plans.

Each commit should represent one logical engineering step.

Unrelated changes should be split into separate commits whenever practical.

---

# External Files, Fixtures and Generated Outputs

Use `input/intake/`, `input/restricted/`, `input/local/` and
`input/versioned/` to classify external files and sources. Record safe
provenance and handling decisions in `input/INVENTORY.md`; use the ignored
`input/INVENTORY.local.md` for sensitive names, paths or details.

Logs, database dumps, API responses, screenshots, crash reports and customer
or user data may be private, confidential or personal. Their presence does not
authorize assistant inspection. Sanitized fixtures or reviewed derivatives are
preferred when they reproduce behavior without unnecessary disclosure.

Generated files should be clearly treated as outputs. Document whether they
are versioned review files, release deliverables or regenerated locally. Review
logs, reports, screenshots, archives, embedded resources and file metadata for
disclosure risks before versioning or sharing them.

Assistant access, Git versioning and publication or external sharing are
separate approval decisions. A reviewed file may be suitable for one purpose
without being suitable for the others. Moving a file between input zones
records classification but does not grant broader authorization.

`.gitignore` rules, the input inventory and documentation should be updated
together. Fixed runtime locations such as `.env`, application log directories
or local databases may remain where the software requires them, but their
classification and ignore rules should still be documented.

Before a commit is prepared, review new and untracked files for secrets,
personal data, confidential content and accidental input inclusion. Prefer
sanitized fixtures or reviewed derivatives whenever they reproduce the
required behavior.

Automated secret, privacy or content checks may identify risks, but a clean
result does not authorize access, versioning or publication.

---

# Feature Commits and Milestone Commits

Feature commits implement or improve a specific logical step.

Regular working commits must use Conventional Commit prefixes such as:

```text
feat:
fix:
docs:
chore:
refactor:
test:
ci:
build:
```

Choose the prefix that matches the actual change. Documentation-only changes should normally use `docs:`.

Milestone commits are the exception. A milestone commit should not use a Conventional Commit prefix. It should use a human-readable summary that includes the completed version number, for example:

```text
Finalize proof-of-concept milestone (v0.3.0)
```

Milestone commits finalize a completed roadmap milestone.

Milestone commits are separate from feature commits and usually update:

- `VERSION`
- `CHANGELOG.md`
- `PROJECT_CONTEXT.md`
- README files or milestone documentation, if needed

A milestone commit should not be used to hide unvalidated feature work or to
bundle an entire separable milestone into one oversized change. Meaningful
implementation, validation, fixes and documentation should normally be
recorded in regular commits before the milestone closure commit.

---

# Documentation Commits

Documentation changes are first-class engineering work.

Updates to README files, CHANGELOG.md, PHILOSOPHY.md, ChatGPT.md, CODEX.md, DOCUMENTATION.md or other project documentation should receive clear commits.

Documentation-only commits are acceptable when they improve clarity, usability or maintainability.

Documentation changes that alter the collaboration model or project philosophy should be harmonized across affected documents.

---

# Repository-Ready Delivery

When repository changes are prepared with AI assistance, they should be delivered as complete, reviewable change sets.

Whenever practical, this includes:

- the changed repository state in the agreed delivery form
- a commit summary
- a commit description
- a concise numbered maintainer checklist for review, validation, commit and tag actions when useful
- code-level documentation or project documentation updates needed to make the implementation understandable without chat context
- user-facing setup, usage, reference or troubleshooting documentation updates when behavior, commands, configuration or operational workflows change
- tag or release guidance when relevant

Repository-ready deliverables should represent the final agreed state of the change and should not require additional manual editing before commit.

The delivery form may be local working tree changes, a patch, explicit file contents or a ZIP archive, depending on the assistant environment and the maintainer's request.

If an archive is used, it must actually contain the stated changes. File existence and contents are part of repository integrity, not optional presentation details.

If no files changed, the assistant should say so instead of returning an unchanged archive as a completed deliverable.

The assistant must not claim that a ZIP, patch, commit or generated file exists unless it has actually been produced and is available for review. If the current environment cannot produce the requested deliverable, the limitation should be stated before offering an alternative delivery mode.

If the current repository state is unclear, the assistant should request an explicit repository baseline before preparing repository-ready deliverables.

---

# Validation Before Commit

Validation should happen before a logical step is committed whenever practical.

Validation may include:

- running scripts or tests
- testing on a real system
- reviewing generated outputs
- verifying documentation consistency
- checking whether the roadmap objective has been met

Bugs found during validation should be fixed before the feature commit if the feature has not yet been committed.

If a bug is found after a feature commit, fix it in a separate commit with an appropriate summary.

When validation requires maintainer-local execution, the assistant should provide exact commands or steps and should interpret the maintainer's output before recommending a commit.

---

# Milestone Closure

Milestones should be finalized intentionally.

A typical milestone closure includes:

- confirming that the milestone objective has been satisfied
- confirming that validation results are documented where needed
- moving changelog entries from `Unreleased` to the completed version
- updating `VERSION`
- updating `PROJECT_CONTEXT.md`
- updating README files, reference documentation or milestone documentation when user-facing status, setup, usage or configuration changes
- preparing a milestone commit with summary and description
- refreshing `PROJECT_CONTEXT.md` after the commit or tag exists if it previously described a pre-commit or pre-tag state
- creating a version tag when the commit represents a meaningful completed state

Feature work should not be hidden inside a milestone commit. A milestone commit should primarily record and summarize an already validated milestone.

---

# Version Tags

Version tags should mark meaningful completed project states.

For future AGIT projects, version tags should use a leading `v`, for example:

```text
v0.1.0
v1.0.0
```

Existing repositories may keep their established tag style for consistency.

Tags should be created intentionally and should not be added after every commit by default.

---

# Releases

GitHub Releases should be created for selected user-facing milestones.

Not every tag requires a release.

For small projects, it is usually sufficient to create releases for:

- first stable releases
- release candidates when useful
- versions with meaningful user-facing changes

Release notes should describe the actual changes included in the release.

---

# Version Metadata

The `VERSION` file should describe the latest completed project version according to the repository's versioning policy.

Do not update `VERSION` merely because a new roadmap step begins.

Update version metadata when a versioned milestone is completed.

---

# Repository Metadata

Repository metadata should be accurate and concise.

This includes:

- repository description
- topics
- license
- README badges

Metadata should help users understand the project without overstating its scope.

---

# Language

English is the primary project language.

Translated documentation may be provided where useful.

Non-English documentation should be clearly identified and should follow the structure of the primary English documentation whenever practical.

Translations should be complete and consistent, not partially localized copies.


---

# Standard Template Elements

Derived repositories should preserve required template elements unless intentionally changed.

The AI Collaboration Note in `README.md` and `README.de.md` is a required repository-visible element for AGIT projects. It should remain directly below the README badges and preserve the original disclosure purpose. Derived projects may adapt project-specific wording when the literal template wording would be inaccurate, but the note should still clearly disclose AI collaboration and point readers to `ChatGPT.md`.

---

# Derived Projects

Repositories created from the AGIT Dev Template should preserve their
initialization provenance and maintain their project rules after setup.

Keep these initialization files under their original names unless the
maintainer documents a deliberate exception:

- `PROJECT_SETUP.md`
- `INITIAL_PROMPT.md`

Record the source-template baseline, initialization status, later harmonization
baselines and intentional deviations in `PROJECT_CONTEXT.md`.

The following documents usually remain part of the derived project:

- `PROJECT_CONTEXT.md`
- `README.md`
- `README.de.md` where useful
- `CHANGELOG.md`
- `AGENTS.md` as the automatic agent entry point
- `ChatGPT.md`
- `CODEX.md` when Codex is used for local project work
- `PHILOSOPHY.md`
- `DOCUMENTATION.md`
- `REPOSITORY.md`
- `LICENSE`
