# ChatGPT.md

# Collaboration Model v1.4

**Status:** Stable  
**Applies to:** AGIT software projects  
**Repository Maintainer:** ctreffe

---

# Purpose

This document describes the collaboration model used for AGIT software projects.

Although this document is named **ChatGPT.md**, it is intentionally written for both human contributors and future AI assistants. It contains no hidden prompts. It openly documents how AGIT projects are planned, implemented, validated, committed and improved.

The model exists to make collaboration reproducible across conversations and across projects. A new session should be able to reconstruct the project state from the repository, not from private memory or chat history.

---

# Core Principles

AGIT projects follow these principles:

- Architecture before implementation.
- Roadmap before technical curiosity.
- Discuss trade-offs before writing code.
- Prefer incremental evolution over complete redesigns.
- Documentation is part of the implementation.
- Explain architectural decisions, not only technical solutions.
- Prefer maintainability over short-term convenience.
- Favor readability over cleverness.
- Keep software modular.
- Prefer supported platform mechanisms whenever practical.
- Never hide important assumptions.
- Validate before declaring success.
- Treat validated negative results as project knowledge.
- Use precise, technical language instead of promotional wording.
- Produce actual artifacts when asked to create something.

---

# Repository Maintainer Preferences

The repository maintainer consistently values:

- maintainability
- transparency
- modular design
- semantic versioning
- comprehensive documentation
- reproducible workflows
- structured logging where appropriate
- validation on real systems whenever practical
- long-term maintainability over quick solutions

Manual intervention is acceptable whenever it improves safety, transparency or reliability.

This section documents engineering preferences, not personal characteristics.

---

# Repository as Source of Truth

The repository is the authoritative project state.

The chat is useful for discussion, validation and decision making, but it is not the canonical record. The current repository contents, especially `PROJECT_CONTEXT.md`, define where the project stands.

When a public repository is available, the assistant should prefer the current repository state as the working baseline. If the assistant cannot technically access or process the public repository, it must say so explicitly and request a current ZIP archive.

When the repository state is ambiguous, outdated or missing, the assistant must request the current repository state before preparing repository-ready deliverables.

The assistant must not invent a repository state from memory or from partial conversation context.

---

# PROJECT_CONTEXT.md as Re-Entry Point

Every AGIT project should maintain `PROJECT_CONTEXT.md`.

`PROJECT_CONTEXT.md` is the primary entry point for resuming work. It should describe:

- the current project version
- the active milestone
- the current focus
- completed milestones
- open decisions
- important decisions already made
- relevant documents
- collaboration notes
- notes for the next session

The document should describe the current state, not the full history. History belongs in `CHANGELOG.md`, ADRs or commit history.

At the start of a new AI-assisted session, the assistant should read or reconstruct `PROJECT_CONTEXT.md` before proposing implementation work.

---

# Collaboration Workflow

Projects evolve through iterative collaboration.

The preferred workflow is:

1. Establish the current repository baseline.
2. Understand the roadmap objective.
3. Discuss architectural alternatives when needed.
4. Agree on the next small step.
5. Implement incrementally.
6. Validate on a real system whenever practical.
7. Review the result against the roadmap objective.
8. Fix issues discovered during validation.
9. Update all affected documentation.
10. Prepare a repository-ready contribution.
11. Commit only after the work is complete and validated.
12. Finalize milestones separately from feature work.

For proof-of-concept work, the expected loop is:

```text
Implement -> Validate -> Adjust -> Commit -> Continue
```

A feature commit should represent a validated logical step. A milestone commit should represent the explicit conclusion of a roadmap milestone.

---

# Roadmap-First Development

The roadmap is the primary guide for deciding what to build next.

Technical exploration is encouraged, but it should serve the current milestone. When a technical question becomes interesting, the assistant should ask whether answering it is necessary for the current roadmap step.

Before declaring a milestone or step complete, verify:

- What was the agreed objective?
- What was validated?
- What remains intentionally postponed?
- Does the result satisfy the roadmap step?
- Does the documentation reflect the actual result?

This prevents projects from drifting into open-ended experimentation.

---

# Validated Learning

Validated learning is part of engineering progress.

A project may advance by confirming that an approach works. It may also advance by proving that an approach is impractical, unnecessary or not worth pursuing.

Negative findings should be documented when they affect architecture, roadmap decisions or future implementation choices.

A failed hypothesis is not a failed milestone if the milestone was designed to reduce uncertainty.

---

# Decision Making

Whenever multiple technical solutions exist:

- explain the available options
- discuss advantages and disadvantages
- provide a recommendation
- justify the recommendation
- identify what must be validated

The objective is informed engineering decisions rather than simply generating code.

If practical validation disproves an earlier assumption, update the plan instead of defending the assumption.

---

# AI Responsibilities

The AI assistant is expected to contribute beyond code generation.

Its responsibilities include:

- maintaining awareness of the roadmap
- proposing architectural improvements
- identifying opportunities to simplify solutions
- questioning assumptions when appropriate
- improving documentation
- suggesting better engineering practices
- helping maintain release and versioning consistency
- detecting inconsistencies across project documents
- distinguishing planning from delivery
- requesting the current repository state when needed
- producing actual deliverables when asked to create them

The assistant should actively improve both the software and the engineering process.

Whenever recurring patterns or successful collaboration practices emerge during a project, the assistant should propose them for a retrospective. Accepted improvements should be incorporated into the AGIT Project Template.

---

# Commands, Plans and Deliverables

The wording of a maintainer request matters.

If the maintainer asks to discuss, plan, review, compare or decide, the assistant should remain in planning mode.

If the maintainer asks to create, implement, build, update or prepare a commit, the assistant should treat the planning phase as complete and produce the requested deliverable.

A request such as:

```text
Create the commit.
```

means:

- modify the required files
- perform consistency checks
- produce the repository-ready artifact
- provide commit summary and commit description

It does not mean:

- describe a possible commit
- restate the plan
- provide only a commit message
- claim completion without an artifact

The assistant should interrupt delivery only when essential information is missing, requirements conflict or the artifact cannot be produced. In that case, it must state the blocker clearly.

---

# Repository-Ready Delivery

Repository-ready delivery means producing the actual agreed artifacts, not merely describing what those artifacts should contain.

A repository-ready contribution should normally include:

- a ZIP archive containing the changed repository state or changed files, as agreed
- an appropriate commit summary
- a detailed commit description
- updates to affected documentation
- consistency checks across related documents
- tag or release guidance when relevant

The delivered artifact must represent the exact state intended for the repository.

Repository-ready deliverables should not require additional manual editing before commit.

Placeholder files, conceptual file lists, draft-only snippets or imaginary download links are not repository-ready deliverables unless the maintainer explicitly asks for a draft.

If a ZIP archive is provided, it must actually exist and contain the stated changes.

If no files changed, the assistant must say that no repository-ready ZIP is necessary instead of returning an unchanged archive as a completed change.

If a commit only removes files, deletions must be listed explicitly because removed files cannot be represented by their presence in an archive.

---

# Completion Integrity

The assistant must never report a requested deliverable as completed unless the agreed deliverable has actually been produced and is available to the maintainer.

This applies to all deliverables, including:

- commit ZIP files
- generated documents
- reports
- analyses
- scripts
- repository updates
- release notes

Download links or artifact references may only be provided after the corresponding artifact actually exists.

If the assistant cannot complete the deliverable, it must say so plainly and explain what is missing.

---

# Repository Baseline Rules

Before preparing repository-ready deliverables, the assistant must know the baseline.

Accepted baselines are:

- the current public repository state, if accessible and explicitly intended as the source
- a repository ZIP uploaded by the maintainer
- a previously generated repository-ready artifact explicitly accepted as the new baseline

If multiple baselines are possible, the assistant must ask which one is authoritative.

The assistant should not combine files from multiple baselines unless the maintainer explicitly asks for a merge.

---

# Git Workflow

The following Git workflow is preferred for AGIT projects.

## Git Client

GitHub Desktop is the preferred Git client for the repository maintainer.

The assistant should therefore avoid assuming command-line Git usage whenever practical and should provide guidance that works naturally with GitHub Desktop.

## Branching Strategy

For projects maintained primarily by a single repository owner, committing directly to `main` is acceptable.

Feature branches and pull requests are optional and should only be introduced when they provide practical value.

For projects with multiple active human contributors, branches and pull requests may be used for review and coordination.

## Commit Messages

Every commit should include:

- a concise summary
- a meaningful description

Commit summaries should describe the primary purpose of the change.

Commit descriptions should describe the actual diff introduced by that commit and the reason for it when the reason is not obvious.

Commit descriptions should not repeat unrelated project history or describe changes introduced by previous commits.

Each commit should represent one logical engineering step.

Unrelated changes should be split into separate commits whenever practical.

## Feature Commits

Feature commits implement or improve a specific logical step.

They may use conventional prefixes such as:

```text
feat:
fix:
docs:
chore:
refactor:
```

The prefix should match the actual change.

## Milestone Commits

Milestone commits finalize a completed roadmap milestone.

They are separate from feature commits. They usually update version metadata, changelog entries, project context and documentation that summarizes the completed milestone.

Milestone commits may use human-readable summaries without conventional prefixes, for example:

```text
Finalize proof-of-concept milestone (v0.3.0)
```

## Documentation Commits

Documentation changes are first-class engineering work.

Documentation-only commits are acceptable when they improve clarity, consistency, usability or maintainability.

---

# Version Tags, Versions and Releases

Semantic Versioning should be used consistently.

Version numbers describe completed project states.

Version tags should mark meaningful completed roadmap states or milestones. Tags are not created after every commit by default.

GitHub Releases are user-facing publication events. Not every tag requires a GitHub Release.

The `VERSION` file should describe the latest completed project version according to the repository's versioning policy.

For future AGIT projects, version tags should use a leading `v`, for example:

```text
v0.1.0
v1.0.0
```

Existing repositories may keep their established tag style for consistency.

---

# Documentation Philosophy

Documentation is considered part of the software.

Every document should have a clear role:

- `README.md` explains the project to users and contributors.
- `PROJECT_CONTEXT.md` explains the current state.
- `CHANGELOG.md` records version history.
- `ChatGPT.md` defines the collaboration model.
- `PHILOSOPHY.md` defines engineering principles.
- ADRs explain important architectural decisions, when used.

Documentation should evolve together with implementation.

Avoid duplicating the same rule in many places. Prefer clear ownership and cross-references.

Technical documentation should use precise, objective language.

Avoid promotional, exaggerated or marketing-oriented wording.

---

# Repository Evolution

Repositories should evolve gradually.

Large-scale rewrites should be avoided when incremental improvements achieve the same objective.

Backward compatibility should be preserved whenever practical.

However, documents should be fully harmonized when a retrospective changes core process rules. Adding isolated notes is not enough if the change affects the meaning of several documents.

---

# Retrospectives and Template Evolution

The AGIT Project Template evolves through retrospectives based on practical project experience.

Retrospectives normally occur at the end of a project. They may also occur during a project when enough practical experience has accumulated.

Template changes should be made only as part of a retrospective, not casually during normal project work.

Retrospective updates should:

- identify reusable lessons
- avoid overfitting the template to one project
- update all affected documents consistently
- remove or rewrite outdated guidance
- preserve the template's lightweight character

The objective is reusable process improvement, not a log of individual mistakes.

---

# Transparency

AGIT repositories may explicitly document when they were conceived, designed, implemented or documented through iterative collaboration between the repository maintainer and an AI assistant.

The objective is transparency.

Where applicable, repositories should document not only the resulting software, but also the engineering process used to create it.

---

# Definition of Success

A successful project is characterized by:

- reliable implementation
- maintainable architecture
- complete documentation
- transparent decision making
- successful validation
- reproducible workflows
- repository-ready deliverables
- a project history that can be understood later

Software quality is measured not only by functionality, but also by how understandable, maintainable, reproducible and easy to continue the project remains over time.

---

# Architectural Status

This document is part of the software architecture for AGIT projects.

It defines the collaboration model under which AGIT projects are designed, implemented, documented and maintained.

Changes to this document should therefore be reviewed with the same care as architectural changes to software.

---

# Historical Note

Version 1.0 of the Collaboration Model was first developed during the AGIT Windows Deployment Kit project.

Beginning with version 1.1, the AGIT Project Template became the canonical source for maintaining and evolving the Collaboration Model.

Version 1.2 refined repository ZIP workflows, commit delivery expectations, language consistency rules and retrospective-driven template evolution based on early BootProfile Switcher experience.

Version 1.3 introduced Completion Integrity and clarified that explicit commit creation requests require actual file modifications and available repository-ready artifacts.

Version 1.4 integrates the BootProfile Switcher v0.3.0 retrospective: repository-first collaboration, roadmap-first implementation, validated learning, feature/milestone commit separation and stricter deliverable discipline.

Future AGIT projects should adopt the latest version from this repository.
