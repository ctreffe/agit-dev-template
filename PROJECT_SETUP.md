# PROJECT_SETUP.md

# Project Setup Guide

This document describes how to initialize a new project from the AGIT Project Template.

It is primarily useful during project creation. Many derived projects may remove this file after setup is complete.

---

# 1. Create the Repository

Create a new repository from the AGIT Project Template.

After creating the repository, establish the first working baseline:

- use the local repository working tree if it is accessible to the assistant and intended as the source of truth,
- use the public repository `main` branch if it is accessible and intended as the source of truth, or
- download the repository as a ZIP archive and use that ZIP as the working baseline.

When using AI assistance, make the baseline explicit before requesting repository-ready changes.

---

# 2. Review Repository Metadata

Update the repository metadata on GitHub:

- repository name
- repository description
- topics
- visibility
- license

Use precise technical language.

Avoid promotional or marketing-oriented wording.

---

# 3. Review Project Documentation

Review and adapt the user-facing documentation:

- `README.md`
- `README.de.md`, if useful

The English README is the primary project documentation.

The German README may be kept, updated or removed depending on the target audience of the derived project.

If both are kept, maintain them as structurally aligned translations.

## Required AI Collaboration Note

Every AGIT project README should include an AI Collaboration Note directly below the badges.

The note is a standardized disclosure artifact. It should preserve the purpose, position and level of visibility of the template note, but the wording must remain factually correct for the derived project.

For the AGIT Project Template itself, the note states that the repository maintains the AGIT Collaboration Model. For derived projects, adapt that project-specific sentence so it accurately describes the collaboration in the derived repository, while still pointing readers to `ChatGPT.md`.

Before completing project setup, verify that:

- `README.md` contains an English AI Collaboration Note below the badges
- `README.de.md`, if kept, contains a German AI Collaboration Note below the badges
- both notes point to `ChatGPT.md`
- no generated project update has replaced the note with a shortened variant

---

# 4. Create or Adapt PROJECT_CONTEXT.md

Create or adapt `PROJECT_CONTEXT.md` for the derived project.

This document is the primary entry point for resuming work on the project. It should describe the current state rather than the full history.

At minimum, review and update:

- project name and repository
- current version or initial milestone
- current status
- current focus
- repository baseline
- completed milestones, if any
- roadmap
- validation status
- open decisions
- relevant documents
- Collaboration Model version
- AGIT Project Template version

Keep this document concise. Its purpose is to help a maintainer, contributor or AI assistant quickly understand where the project stands today.

---

# 5. Establish the Initial Roadmap

Before implementation accelerates, establish an initial roadmap for the derived project.

The roadmap should identify the first meaningful milestones and explain what each milestone is meant to prove, decide or deliver. It should also name important non-goals and validation expectations.

The roadmap may evolve as the project learns, but starting with an explicit roadmap helps keep AI-assisted development focused and comparable across sessions.

Record the roadmap in `PROJECT_CONTEXT.md` or a dedicated roadmap document if the project needs more detail.

---

# 6. Review Core Project Documents

The following documents usually remain in the derived project:

- `PROJECT_CONTEXT.md`
- `README.md`
- `README.de.md` where useful
- `CHANGELOG.md`
- `ChatGPT.md`
- `CODEX.md` when Codex will be used for local project work
- `PHILOSOPHY.md`
- `LICENSE`

These documents define the current project state, user documentation, version history, collaboration model, local Codex operating policy, engineering philosophy and license of the project.

---

# 7. Review Template-Only Documents

The following documents are primarily useful during project initialization:

- `PROJECT_SETUP.md`
- `DOCUMENTATION.md`
- `REPOSITORY.md`

After completing the initial project setup, these files may be removed from the derived project.

They are part of the template workflow rather than the long-term documentation of most derived projects.

If a derived project has a practical reason to keep one of these documents, it may do so.

---

# 8. Update Project-Specific Content

Replace template-specific wording with project-specific content.

Typical updates include:

- project name
- repository description
- README overview
- setup instructions
- usage instructions
- badges
- version references
- links to related repositories

Keep documentation focused on the users and contributors of the derived project.

---

# 9. Review the Collaboration Model

Review `ChatGPT.md`.

The file should usually be kept unchanged unless the derived project has a specific reason to adjust the Collaboration Model.

If the AGIT Project Template contains a newer version of the Collaboration Model, prefer adopting the newer version.

---

# 10. Review the Codex Operating Policy

Review `CODEX.md` if Codex will be used for local project work.

`CODEX.md` defines local execution rules for Codex, including:

- allowed local tools
- read-only Git usage
- approval-required actions
- forbidden actions
- local tool environments
- internet and data disclosure rules
- multi-repository safety
- delivery expectations

Keep `CODEX.md` in the derived project when Codex will continue to assist with local repository work.

If the project does not use Codex locally, the file may be removed during setup.

---

# 11. Prepare Local Tooling

Install or verify the local tools that are useful for the derived project.

Common tools include:

- Git for Windows
- GitHub Desktop
- PowerShell
- Python with project-local virtual environments
- Node.js where needed
- `rg` or another fast local search tool
- ZIP/archive tooling

Codex should prefer project-local tool environments over global tool changes.

Typical local tool artifacts include:

```text
.venv/
node_modules/
.codex-input/
.codex-cache/
.codex-tmp/
.codex-output/
artifacts/
deliverables/
```

These should normally remain ignored by Git unless the derived project intentionally uses a different structure.

---

# 12. Review the Project Philosophy

Review `PHILOSOPHY.md`.

The file should usually remain stable across AGIT projects.

Only change it if the derived project intentionally follows different engineering principles.

---

# 13. Initialize Versioning

Set the initial project version.

For most derived projects, the first meaningful project milestone should be:

```text
0.1.0
```

Future AGIT projects should use version tags with a leading `v`, for example:

```text
v0.1.0
v1.0.0
```

Do not increase the version merely because a milestone begins. Increase version metadata when the milestone is completed.

---

# 14. Prepare the First Project Commit

The first project-specific commit should describe the repository initialization.

Use a concise summary and a meaningful description.

Example summary:

```text
chore: initialize project from AGIT template
```

Example description:

```text
Initialize the project from the AGIT Project Template.

Review and adapt the README files, core project documents and repository
metadata for the new project. Establish PROJECT_CONTEXT.md as the current
state entry point for future development sessions.
```

---

# 15. Remove Template-Only Setup Files

After completing setup, remove the files that are no longer needed:

- `PROJECT_SETUP.md`
- `DOCUMENTATION.md`
- `REPOSITORY.md`

Remove template-only setup files in a dedicated commit.

This keeps project history clear by showing when the initial setup was completed.

`PROJECT_CONTEXT.md` should remain because it documents the current project state and supports future project resumption.

---

# 16. Start Development

After the initial setup commit, continue development according to the Collaboration Model in `ChatGPT.md`.

When using Codex locally, also follow `CODEX.md`.

Keep `PROJECT_CONTEXT.md` current when completing milestones, changing the roadmap, resolving important decisions or preparing to resume the project in a new collaboration session.

When working with AI assistance:

- establish the current repository baseline
- establish or review the current roadmap
- agree on the next roadmap step
- implement small changes
- validate before commit whenever practical
- use small implement-validate-adjust-commit loops during active milestones
- request repository-ready deliverables only after the plan is clear
- require actual artifacts, not simulated completion
- commit with a clear summary and description
- keep feature commits separate from milestone commits
- document assistant-written code well enough that maintainers and future contributors can understand it without chat history
- tag meaningful completed milestones intentionally
- expect numbered maintainer next steps when validation, review, commit or tag actions are needed

---

# 17. Retrospectives and Template Feedback

During project work, collect findings that may improve the AGIT Project Template.

Template changes should not be made casually during normal project work. Instead, review collected findings in a retrospective.

Retrospectives normally take place at the end of a project, but they may also be held during a project when enough practical experience has accumulated.

Only changes that have proven useful in real project work should be considered for inclusion in the AGIT Project Template.

When a retrospective changes core process guidance, update all affected template documents consistently instead of appending isolated notes.
