# DOCUMENTATION.md

# Documentation Standards

This document describes the purpose and responsibility of the core documents used by the AGIT Project Template.

It does not define project-specific content. Instead, it explains which document should contain which type of information.

---


# PROJECT_CONTEXT.md

Within the AGIT Project Template, `PROJECT_CONTEXT.md` is the primary entry point for resuming work on a project.

It should describe the current project state, current focus, completed milestones, open decisions, relevant repository versions and the most important documents for continuing work.

It should answer:

- where the project stands today
- what the current development focus is
- what has already been completed
- what decisions are still open
- which documents should be read next

`PROJECT_CONTEXT.md` should not become a full project history. Historical changes belong in `CHANGELOG.md`; decision rationale belongs in ADRs; general project explanation belongs in the README.

For AGIT projects, `PROJECT_CONTEXT.md` should usually remain in the repository and be kept current whenever a milestone is completed, a retrospective changes the working model or the project is about to be resumed in a new collaboration session.

---

# README.md

Within the AGIT Project Template, `README.md` is the primary user-facing entry point.

It should explain:

- what the project is
- what problem it solves
- how to get started
- where to find additional documentation
- important usage notes

The README should remain focused on users of the project.

It should not become a general archive for engineering philosophy, collaboration practices or internal development process details.

---

# README.de.md

Within the AGIT Project Template, `README.de.md` is the German translation of the user-facing README.

It should follow the structure and intent of `README.md`.

The English README remains the primary project documentation.

The German README is provided to make the project easier to use for German-speaking users.

Translated documents should be complete translations, not partially localized documents. Headings, explanatory text and lists should be translated consistently. Established technical terms and proper names may remain unchanged when that improves clarity.

---

# CHANGELOG.md

Within the AGIT Project Template, `CHANGELOG.md` documents notable changes between project versions.

It should describe changes that are relevant to users, maintainers or contributors.

The changelog should be updated whenever a versioned project milestone is prepared.

---

# PHILOSOPHY.md

Within the AGIT Project Template, `PHILOSOPHY.md` documents the engineering philosophy shared by derived projects.

It should describe long-term principles and values, not project-specific implementation details.

This document should change less frequently than workflow-oriented documentation.

---

# ChatGPT.md

Within the AGIT Project Template, `ChatGPT.md` contains the AGIT Collaboration Model.

It documents the collaboration workflow, AI-assisted engineering practices, repository-ready delivery process and related development conventions.

Although the file is named `ChatGPT.md`, it is intended to be useful for future AI assistants as well as human contributors.

---

---

# PROJECT_SETUP.md

Within the AGIT Project Template, `PROJECT_SETUP.md` guides the initial setup of derived repositories.

It is a template-only document.

After a derived project has been initialized, this file may be removed unless it remains useful for that project.

---

# Architecture Documentation

Architecture documentation describes how a project is structured.

It should explain the major components, responsibilities and relationships of the system. It should not replace Architecture Decision Records.

---

# Architecture Decision Records

Architecture Decision Records document why a specific architectural decision was made.

An ADR should document a decision, not merely describe the current state of the project.

For AGIT projects, ADR numbering should normally start with `ADR-0001`. A special `ADR-0000` should be avoided unless there is a clear project-specific reason.

---

# Retrospective Documentation

Retrospectives are used to identify improvements to the AGIT Project Template based on practical project experience.

They normally occur at the end of a project, but they may also be held during a project when enough findings have accumulated.

Template improvements should be made only as part of a retrospective. This keeps the template stable during normal project work while still allowing it to evolve.

---

# Additional Documentation

Additional documentation should be added only when it has a clear purpose and audience.

Examples may include:

- architecture documentation
- configuration reference
- release documentation
- developer documentation
- API documentation

New documents should not duplicate existing documentation.

Each document should have one clearly defined responsibility.

A useful distinction for AGIT projects is:

- `PROJECT_CONTEXT.md` explains where the project stands today and is the primary re-entry point.
- `README.md` explains what the project is.
- Architecture documentation explains how the system is structured.
- ADRs explain why specific architecture decisions were made.
- `PHILOSOPHY.md` explains the shared AGIT engineering philosophy.

---

# General Guidance

Documentation should be precise, useful and maintainable.

Prefer factual descriptions over promotional language.

Keep user documentation focused on using the project.

Keep engineering standards and collaboration practices in their dedicated documents.
