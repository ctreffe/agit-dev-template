# DOCUMENTATION.md

# Documentation Standards

This document describes documentation standards used by the AGIT Dev Template.

Documentation is treated as part of the software. It should be maintained with the same care as implementation code.

Assistant-written implementation work must be understandable from the repository itself. When code contains non-obvious behavior, assumptions, constraints, integration points or architectural decisions, those details should be documented close to the code or in the appropriate project document.

Prefer clear names, small modules and purposeful comments over lengthy explanations of obvious code. Comments should explain intent, trade-offs and constraints, not restate what the code already says.

---

# Document Roles

Each document should have a clear role.

## README.md

The primary user-facing entry point.

It explains what the project is, who it is for, how to get started and where to find more information.

## README.de.md

A German translation of the README where useful.

It should follow the structure of `README.md` and should not drift into a separate document.

## PROJECT_CONTEXT.md

The current-state entry point for resuming work.

It describes where the project stands today, the active milestone, the current baseline and the next steps.

For active milestone work, it should also capture validation notes, immediate validation targets and the next recommended step when those details are needed to resume efficiently.

For new projects, it should capture the maintainer's project intent, problem context, desired end state and boundaries before the initial roadmap. The roadmap should be clear enough that future sessions can understand the intended milestone sequence and why the next step matters.

## CHANGELOG.md

The version history.

It records completed changes by version. It should not replace `PROJECT_CONTEXT.md` or the roadmap.

## ChatGPT.md

The AGIT Collaboration Model.

It describes how the maintainer and AI assistant collaborate, including repository-ready delivery, roadmap-first work and validation expectations.

## CODEX.md

The local Codex operating policy.

It describes what Codex may do on the maintainer's machine, including local tool usage, read-only Git access, approval-required actions, data disclosure rules and delivery expectations.

## PHILOSOPHY.md

The shared engineering philosophy.

It describes the values behind technical decisions, such as maintainability, transparency and validated learning.

## ADRs

Architecture Decision Records may be used when a decision is important enough that its reasoning should remain available later.

Use an ADR checkpoint when a decision affects architecture, configuration formats, lifecycle behavior, deployment, security boundaries or another durable part of the project structure.

ADRs should explain the context, decision, rationale and consequences. They should not be used for every small implementation choice.

---

# Current State vs. History

Keep current state and history separate.

- Current state belongs in `PROJECT_CONTEXT.md`.
- Version history belongs in `CHANGELOG.md`.
- Durable decision reasoning belongs in ADRs, when used.
- User-facing overview belongs in `README.md`.

Do not force one document to serve all purposes.

---

# Dedicated Component Documentation

READMEs should remain concise entry points and navigation aids.

When a module, integration, component or workflow becomes too substantial for the README, move the detailed documentation into a dedicated document such as:

- `docs/modules/<name>.md`
- `docs/integrations/<name>.md`
- another project-specific documentation area

The README should briefly explain what the component is, link to the dedicated document and avoid duplicating long configuration, lifecycle, warning or troubleshooting sections.

If a substantial production component is exposed to users, include a demonstration, example configuration or validation path when applicable. This does not need to be the same shape in every project. Depending on the project, it may be:

- an installable demo
- a sample configuration
- a reproducible command sequence
- a fixture
- a validation checklist

The goal is to make the component understandable and verifiable without requiring private maintainer explanations.

---

# Repository-Ready Documentation

Documentation changes are repository-ready only when they are consistent across affected documents.

For example, if the collaboration workflow changes, review at least:

- `ChatGPT.md`
- `CODEX.md`, if local Codex operating rules are affected
- `PHILOSOPHY.md`
- `PROJECT_CONTEXT.md`
- `README.md`
- `README.de.md`, if present
- `DOCUMENTATION.md`
- `REPOSITORY.md`, if repository behavior is affected

Do not append isolated notes when the change affects the structure or meaning of existing documentation.

Rewrite affected sections so the final documents read as one coherent version.

Before a milestone commit, perform a documentation freshness pass. Review whether the milestone state is reflected in:

- version and status wording
- roadmap and current-focus notes
- `CHANGELOG.md`
- `README.md`
- `README.de.md`, if present
- links to new dedicated documentation
- setup, demo or usage instructions
- validation results and known limitations

The milestone commit should contain the coherent completed state. Avoid relying on a follow-up cleanup commit for documentation that should have been current at the milestone.


---

# Standard Documentation Artifacts

Some documentation elements are standardized template artifacts. They should be reused consistently in derived projects rather than removed during setup.

The AI Collaboration Note in `README.md` and `README.de.md` is such an artifact. It should appear directly below the README badges and preserve the template note's disclosure purpose, structure and visibility. Derived projects should adapt project-specific wording when the literal template wording would be inaccurate, while still linking to `ChatGPT.md`.

When repository documentation is updated with AI assistance, the assistant should preserve standardized artifacts unless explicitly instructed to change them.

---

# Local Operating Policy Documentation

Keep the general collaboration model and local execution rules separate.

- `ChatGPT.md` documents the general AGIT Collaboration Model.
- `CODEX.md` documents how Codex may operate locally.
- `PROJECT_SETUP.md` explains how to prepare a local project environment.
- `PROJECT_CONTEXT.md` describes the current state of a derived project after setup.

Do not move local tool rules, Git command restrictions or machine-specific execution guidance into `ChatGPT.md` unless the rule is part of the general collaboration model.

---

# User-Facing Documentation

User-facing documentation should make the project practically usable.

For projects with setup, configuration, commands, scripts, profiles, modules or operational workflows, document the relevant user surface clearly enough that a user can proceed without asking the maintainer for missing context.

Depending on the project, useful user documentation may include:

- prerequisites and supported platforms
- installation, setup and update steps
- configuration files, settings, defaults and valid values
- command, script, flag or profile reference material
- examples for common workflows
- expected outputs, logs, generated files or system changes
- permissions, safety notes, rollback or uninstall steps
- troubleshooting guidance for common failures
- current maturity, limitations and intentionally unsupported scenarios

Reference material should be kept accurate and easy to verify. If a project exposes many commands or settings, prefer a concise generated or generated-like reference over scattered prose.

---

# Language and Tone

Use precise, technical language.

Avoid promotional, exaggerated or marketing-oriented wording.

Prefer clarity over persuasion.

Documentation should explain what is true, what is supported and what remains intentionally out of scope.

---

# German Documentation

When a German README or other translation is maintained, it should be a complete translation of the corresponding English document.

Project names, repository names and established technical terms may remain in English when translation would reduce clarity.

Do not mix languages within one document unless there is a clear technical reason.

---

# Documentation During Proofs of Concept

Proof-of-concept documentation should describe:

- the hypothesis or objective
- the implementation boundaries
- what was tested
- what was validated
- what did not work, if relevant
- what remains out of scope

Validated negative results should be documented when they influence the roadmap or architecture.

For milestone-driven implementation, document the final validated state rather than every chat turn. Use `PROJECT_CONTEXT.md` for current status and next validation targets, `CHANGELOG.md` for version history, and ADRs for durable decision reasoning.

---

# Retrospective Updates

Template updates should be made through retrospectives based on real project experience.

A retrospective update should not simply add a new section to every document.

Instead, review the role of each document and integrate the new guidance where it belongs.

Remove outdated or redundant wording when necessary.

---

# Minimal Useful Documentation

Documentation should remain useful and lightweight.

Do not create documents only because a template exists.

Do create documentation when it improves:

- onboarding
- validation
- maintainability
- decision traceability
- release confidence
- the ability to resume work later


