# PROJECT_SETUP.md

# Project Setup Guide

This document guides the initial setup of a new project created from the AGIT Project Template.

It is intended to be used immediately after creating a new repository from the template.

After the setup is complete, this file should be removed from the derived project.

---

# 1. Create the Derived Repository

Create the new repository from the AGIT Project Template.

After the repository has been created, download the complete repository state as a ZIP file.

When working with AI assistance, upload this ZIP file before project-specific initialization begins. The uploaded repository ZIP is the shared working baseline for the next set of changes.

This avoids relying on incomplete or inaccessible remote repository content.

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
- `README.de.md`

The English README is the primary project documentation.

The German README may be kept, updated or removed depending on the target audience of the derived project.

---

# 4. Review Core Project Documents

The following documents should usually remain in the derived project:

- `PROJECT_CONTEXT.md`
- `README.md`
- `README.de.md` where useful
- `CHANGELOG.md`
- `ChatGPT.md`
- `PHILOSOPHY.md`
- `LICENSE`

These documents define the current project state, user documentation, version history, collaboration model, engineering philosophy and license of the project.

---


# 5. Create or Adapt PROJECT_CONTEXT.md

Create or adapt `PROJECT_CONTEXT.md` for the derived project.

This document is the primary entry point for resuming work on the project. It should describe the current state of the project rather than the full history of how the project reached that state.

At minimum, review and update:

- project name and repository
- current version or initial milestone
- current status
- current focus
- completed milestones, if any
- open decisions
- relevant documents
- Collaboration Model version
- AGIT Project Template version

Keep this document concise. Its purpose is to help a maintainer, contributor or AI assistant quickly understand where the project stands today.

---

# 6. Review Template-Only Documents

The following documents are primarily useful during project initialization:

- `PROJECT_SETUP.md`
- `DOCUMENTATION.md`
- `REPOSITORY.md`

After completing the initial project setup, these files may be removed from the derived project.

They are part of the template workflow rather than the long-term documentation of most derived projects.

If a derived project has a practical reason to keep one of these documents, it may do so.

---

# 7. Update Project-Specific Content

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

Keep the documentation focused on the users of the derived project.

---

# 8. Review the Collaboration Model

Review `ChatGPT.md`.

The file should usually be kept unchanged unless the derived project has a specific reason to adjust the Collaboration Model.

If the AGIT Project Template contains a newer version of the Collaboration Model, prefer adopting the newer version.

---

# 9. Review the Project Philosophy

Review `PHILOSOPHY.md`.

The file should usually remain stable across AGIT projects.

Only change it if the derived project intentionally follows different engineering principles.

---

# 10. Initialize Versioning

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

---

# 11. Prepare the First Project Commit

The first project-specific commit should describe the repository initialization.

Use a concise summary and a meaningful description.

Example summary:

```text
Establish project foundation
```

Example description:

```text
Initialize the project from the AGIT Project Template.

Review and adapt the README files, core project documents and repository
metadata for the new project.

Remove template-only setup documentation after completing the initial
project setup.
```

---

# 12. Remove Template-Only Setup Files

After completing the setup, remove the files that are no longer needed:

- `PROJECT_SETUP.md`
- `DOCUMENTATION.md`
- `REPOSITORY.md`

Remove template-only setup files in a dedicated commit.

This keeps the project history clear by showing when the initial setup was completed.

The resulting repository should contain only the documents that are useful for the ongoing project. `PROJECT_CONTEXT.md` should remain because it documents the current project state and supports future project resumption.

---

# 13. Start Development

After the initial setup commit, continue development according to the Collaboration Model in `ChatGPT.md`. Keep `PROJECT_CONTEXT.md` current when completing milestones, changing the roadmap, resolving important decisions or preparing to resume the project in a new collaboration session.

When working with AI assistance, use repository-ready delivery:

- provide the current repository state as a ZIP file when needed
- receive complete change sets
- ensure commit ZIP files contain only new or changed files
- review the changes
- commit with a clear summary and description
- tag meaningful milestones intentionally

---

# 14. Retrospectives and Template Feedback

During project work, collect findings that may improve the AGIT Project Template.

Template changes should not be made casually during normal project work. Instead, review collected findings in a retrospective.

Retrospectives normally take place at the end of a project, but they may also be held during a project when enough practical experience has accumulated.

Only changes that have proven useful in real project work should be considered for inclusion in the AGIT Project Template.
