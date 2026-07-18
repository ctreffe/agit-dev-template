# AGIT Dev Template

![License](https://img.shields.io/github/license/ctreffe/agit-dev-template)
![Release](https://img.shields.io/github/v/tag/ctreffe/agit-dev-template)
![Last Commit](https://img.shields.io/github/last-commit/ctreffe/agit-dev-template)

[Deutsche Dokumentation](README.de.md)

> [!NOTE]
> **AI Collaboration**
>
> This repository maintains the AGIT Dev Template.
>
> The AGIT Dev Template is the development-oriented specialization of the generic AGIT Project Template.
>
> The collaboration model documents engineering practices, AI-assisted development workflows and repository conventions used by development-oriented AGIT projects.
>
> Its collaboration model is maintained in [ChatGPT.md](ChatGPT.md).

## Overview

The AGIT Dev Template is the starting point for development-oriented AGIT projects.

It provides a reusable repository foundation for projects involving code, scripts, automation, technical documentation, validation, releases, repository standards and retrospective-driven process improvement.

This repository is not a code framework. It is a development project template.

The AGIT Dev Template builds on the generic [AGIT Project Template](https://github.com/ctreffe/agit-project-template). Use the generic template for non-development projects, and use this template when software, scripts, automation, validation, technical architecture or release workflows are central to the project.

## AGIT Templateverse

The public AGIT templates form a small templateverse: a family of related templates that share a repository-first, maintainer-led Human-AI collaboration model while specializing it for different project types.

- [AGIT Project Template](https://github.com/ctreffe/agit-project-template) is the generic starting point for structured project work, research, planning, concept work, process design and mixed projects.
- [AGIT Dev Template](https://github.com/ctreffe/agit-dev-template) is for development-oriented projects where code, scripts, automation, validation, architecture or release workflows are central.
- [AGIT Documentation Template](https://github.com/ctreffe/agit-docs-template) is for technical documentation projects such as user guides, admin guides, operating procedures, tutorials, migration guides and documentation sites.

Start from the Dev Template when implementation lifecycle, validation and release discipline are part of the project from the beginning. Start from the generic Project Template when those needs may emerge later.

## What the Template Provides

The template defines:

- a collaboration model for AI-assisted software development
- a local Codex operating policy
- an initial prompt for reproducible project setup
- a current-state project context document
- maintainer-owned project intent and target-state guidance
- roadmap-first milestone guidance
- documentation and repository standards for maintainers, contributors and users
- guidance for sensitive local inputs, sanitized fixtures and generated artifacts
- a shared engineering philosophy
- versioning and release guidance
- a retrospective process for improving the template from real project experience

## Project Context

Every AGIT project should maintain `PROJECT_CONTEXT.md`.

`PROJECT_CONTEXT.md` is the primary entry point for resuming a project. It captures the current project state, current focus, repository baseline, completed milestones, validation status, open decisions and relevant documentation links.

The file does not replace the README, changelog, architecture documentation or decision records. Instead, it helps readers understand where the project stands today and which documents are currently relevant.

At project start, `PROJECT_CONTEXT.md` should also capture the maintainer's project intent: the problem context, desired end state, important boundaries and roadmap implications. This maintainer-owned context gives the roadmap direction before implementation accelerates.

## Development Workflow

AGIT projects follow a repository-first workflow.

The repository is the authoritative project state. When AI assistance is used, work should start from a clear repository baseline, such as an accessible local working tree, a public repository state or a current ZIP archive.

The preferred workflow is:

1. Establish the current repository baseline.
2. Establish or review maintainer project intent and desired end state.
3. Establish or review the roadmap and agree on the next milestone step.
4. Implement a small, reviewable change.
5. Validate the change whenever practical.
6. Fix issues found during validation.
7. Update affected code, user-facing and project documentation.
8. Prepare a repository-ready contribution in the agreed delivery form.
9. Commit the validated step.
10. Finalize milestones separately from feature work.

Requests such as "create the commit" mean that the requested repository-ready result should be produced, not merely described. They do not authorize the assistant to run Git history commands unless the request contains a recognized control word. Artifact integrity is part of the workflow: local working tree changes, generated archives and repository updates must actually exist before they are reported as complete.

## Git History Control Words

AI assistants must not perform Git history actions such as staging, committing, tagging, pushing, pulling, merging, rebasing, resetting or switching branches unless the maintainer instruction for that specific action contains a recognized control word.

Recognized control words are `explicit` and `explicitly` in English-language instructions, and the German word family `explizit`, including inflected forms such as `explizite`, `expliziten`, `expliziter` and `explizites`, in German-language instructions. Requests without one of these control words authorize preparation and guidance only.

## How to Use This Template

1. Create a new repository from this template.
2. Establish the initial repository baseline from the local working tree, public repository state or a ZIP archive.
3. Review `PROJECT_SETUP.md`.
4. Adapt the README files and repository metadata to the new project.
5. Preserve an AI Collaboration Note directly below the README badges and adapt project-specific wording when needed for factual accuracy.
6. Capture the maintainer's project intent, context, desired end state and boundaries.
7. Create or adapt `PROJECT_CONTEXT.md` as the current-state entry point for the project.
8. Establish the initial roadmap from the maintainer intent and record it in `PROJECT_CONTEXT.md` or a dedicated roadmap document.
9. Review the core project documents.
10. Review `CODEX.md` if Codex will be used for local project work.
11. Record initialization provenance and the source-template baseline.
12. Continue development according to `ChatGPT.md`.

## Documents That Usually Remain

The following documents usually remain part of a derived project:

- `PROJECT_CONTEXT.md`
- `README.md`
- `README.de.md`, where useful
- `CHANGELOG.md`
- `ChatGPT.md`
- `CODEX.md`, when Codex is used for local project work
- `PHILOSOPHY.md`
- `LICENSE`

## Initialization Provenance

The following documents primarily support project initialization and should
normally remain in a derived repository as a record of its methodological
starting point:

- `PROJECT_SETUP.md`
- `INITIAL_PROMPT.md`

Record initialization status, initial template version and commit, later
harmonization baselines and intentional deviations in `PROJECT_CONTEXT.md`.
Remove either initialization document only as a deliberate, documented
maintainer exception.

`DOCUMENTATION.md` and `REPOSITORY.md` are ongoing project rules. Adapt and
maintain them in the derived project.

Keep `CONTINUATION_PROMPT.md` in the derived project for repeatable
context-window and session handoffs.

## Continuous Improvement

The AGIT Dev Template evolves through project retrospectives.

Retrospectives normally take place at the end of a project, but they may also be held during a project when enough practical findings have accumulated.

Template changes should be made only as part of such a retrospective. When a retrospective changes core process guidance, affected documents should be harmonized instead of receiving isolated notes.

## Core Template Documents

- [PROJECT_CONTEXT.md](PROJECT_CONTEXT.md) - project context template and derived-project re-entry point
- [PROJECT_SETUP.md](PROJECT_SETUP.md) – initial setup guide for new projects
- [INITIAL_PROMPT.md](INITIAL_PROMPT.md) – first prompt for reproducible project initialization
- [CONTINUATION_PROMPT.md](CONTINUATION_PROMPT.md) – re-entry prompt for a new context window or assistant session
- [ChatGPT.md](ChatGPT.md) – Collaboration Model
- [CODEX.md](CODEX.md) – local Codex operating policy
- [PHILOSOPHY.md](PHILOSOPHY.md) – project philosophy
- [DOCUMENTATION.md](DOCUMENTATION.md) – documentation standards
- [REPOSITORY.md](REPOSITORY.md) – repository standards
- [decisions/](decisions/) – Decision Record templates for ADRs, PDRs and DDRs
- [CHANGELOG.md](CHANGELOG.md) – version history
- [README.de.md](README.de.md) – German documentation
- [LICENSE](LICENSE) – MIT License

## License

This project is licensed under the MIT License.
