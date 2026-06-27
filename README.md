# AGIT Project Template

![License](https://img.shields.io/github/license/ctreffe/agit-project-template)
![Release](https://img.shields.io/github/v/tag/ctreffe/agit-project-template)
![Last Commit](https://img.shields.io/github/last-commit/ctreffe/agit-project-template)

[Deutsche Dokumentation](README.de.md)

> [!NOTE]
> **AI Collaboration**
>
> This repository maintains the current AGIT Collaboration Model.
>
> The Collaboration Model documents engineering practices, collaboration workflows and repository conventions used across AGIT projects.
>
> It is maintained in [ChatGPT.md](ChatGPT.md).

## Overview

The AGIT Project Template is the starting point for new AGIT software projects.

It provides a reusable repository foundation with documentation, collaboration and repository standards.

This repository is not a code framework. It is an engineering template.


## Project Context

Every AGIT project should maintain a `PROJECT_CONTEXT.md` file.

`PROJECT_CONTEXT.md` is the primary entry point for resuming a project. It captures the current project state, current focus, completed milestones, open decisions and relevant documentation links.

The file is not intended to replace the README, changelog, architecture documentation or ADRs. Instead, it helps readers understand where the project stands today and which documents are currently relevant.

## How to Use This Template

1. Create a new repository from this template.
2. Download the newly created repository as a ZIP file.
3. Upload the ZIP file when working with AI assistance so the full repository state is available.
4. Review `PROJECT_SETUP.md`.
5. Adapt the README files and repository metadata to the new project.
6. Create or adapt `PROJECT_CONTEXT.md` as the current-state entry point for the project.
7. Review the core project documents.
8. Remove template-only setup documents when the project setup is complete.

## Documents That Usually Remain

The following documents usually remain part of a derived project:

- `PROJECT_CONTEXT.md`
- `README.md`
- `README.de.md`, where useful
- `CHANGELOG.md`
- `ChatGPT.md`
- `PHILOSOPHY.md`
- `LICENSE`

## Template-Only Documents

The following documents primarily support project initialization:

- `PROJECT_SETUP.md`
- `DOCUMENTATION.md`
- `REPOSITORY.md`

After the initial setup is complete, these documents may be removed from the derived project unless they remain useful there.

## Continuous Improvement

The AGIT Project Template evolves through project retrospectives.

Retrospectives normally take place at the end of a project, but they may also be held during a project when enough practical findings have accumulated. Template changes should be made only as part of such a retrospective, not casually during normal project work.

## Core Template Documents

- [PROJECT_CONTEXT.md](PROJECT_CONTEXT.md) – current project state and primary re-entry point
- [PROJECT_SETUP.md](PROJECT_SETUP.md) – initial setup guide for new projects
- [ChatGPT.md](ChatGPT.md) – Collaboration Model
- [PHILOSOPHY.md](PHILOSOPHY.md) – project philosophy
- [DOCUMENTATION.md](DOCUMENTATION.md) – documentation standards
- [REPOSITORY.md](REPOSITORY.md) – repository standards
- [CHANGELOG.md](CHANGELOG.md) – version history
- [README.de.md](README.de.md) – German documentation
- [LICENSE](LICENSE) – MIT License

## License

This project is licensed under the MIT License.
