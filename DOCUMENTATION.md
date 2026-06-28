# DOCUMENTATION.md

# Documentation Standards

This document describes documentation standards used by the AGIT Project Template.

Documentation is treated as part of the software. It should be maintained with the same care as implementation code.

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

For new projects, it should capture the initial roadmap clearly enough that future sessions can understand the intended milestone sequence and why the next step matters.

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

---

# Current State vs. History

Keep current state and history separate.

- Current state belongs in `PROJECT_CONTEXT.md`.
- Version history belongs in `CHANGELOG.md`.
- Decision reasoning belongs in ADRs, when used.
- User-facing overview belongs in `README.md`.

Do not force one document to serve all purposes.

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
