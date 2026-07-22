# AGIT Dev Template

[![Status](https://img.shields.io/badge/status-stable-green)](VERSION)
[![Version](https://img.shields.io/github/v/tag/ctreffe/agit-dev-template?label=version)](CHANGELOG.md)
[![License](https://img.shields.io/github/license/ctreffe/agit-dev-template)](LICENSE)

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

<br>

**[Link zur deutschen README](README.de.md)**

<br>

## Contents

- [Overview](#overview)
- [Core Principle](#core-principle)
- [AGIT Templateverse](#agit-templateverse)
- [When to Use This Template](#when-to-use-this-template)
- [Project Initialization](#project-initialization)
- [External Files and Sources](#external-files-and-sources)
- [Recommended Workflow](#recommended-workflow)
- [Git Index and Protected Git Actions](#git-index-and-protected-git-actions)
- [Decision Records](#decision-records)
- [Repository Structure](#repository-structure)
- [Template and Derived Project Files](#template-and-derived-project-files)
- [How to Use This Template](#how-to-use-this-template)
- [Maintainer Tool Setup](#maintainer-tool-setup)
- [Continuous Improvement](#continuous-improvement)
- [License](#license)

## Overview

The AGIT Dev Template is the starting point for development-oriented projects involving code, scripts, automation, technical architecture, validation, releases and user-facing technical documentation. It provides a reusable repository foundation and collaboration method rather than a programming framework or application scaffold.

The template combines maintainer-owned intent with roadmap-first implementation, small reviewable changes, explicit validation, durable project context, documented technical decisions and repository-ready delivery. It builds on the generic AGIT Project Template and adds engineering-specific expectations for code readability, sensitive inputs, generated outputs and release discipline.

## Core Principle

The maintainer owns the project direction, architecture and release decisions. The assistant may help design, implement, test, document and review changes, but must preserve maintainer authority, make assumptions and limitations visible and never simulate completed code, validation, commits or files.

The repository is the authoritative engineering state. Code and documentation should be understandable to future maintainers without private chat history, and a change is not complete merely because it worked once.

## AGIT Templateverse

The public AGIT templates form a small templateverse: a family of related templates that share a repository-first, maintainer-led Human-AI collaboration model while specializing it for different project types.

- [AGIT Project Template](https://github.com/ctreffe/agit-project-template) is the generic starting point for structured project work, research, planning, concept work, process design and mixed projects.
- [AGIT Dev Template](https://github.com/ctreffe/agit-dev-template) is for development-oriented projects where code, scripts, automation, validation, architecture or release workflows are central.
- [AGIT Documentation Template](https://github.com/ctreffe/agit-docs-template) is for technical documentation projects such as user guides, admin guides, operating procedures, tutorials, migration guides and documentation sites.

## When to Use This Template

Use the Dev Template when implementation lifecycle, validation and release discipline are central from the beginning. Typical projects include command-line tools, scripts, automation, integration utilities, deployment tooling, libraries, prototypes that must produce validated learning and repositories that expose technical configuration or operational workflows.

Use the generic Project Template when the project is still primarily discovery, planning or mixed non-development work. A generic project may deliberately migrate toward this template when code, tests, architecture or releases become central.

## Project Initialization

After creating the repository, the maintainer needs to invoke only [INITIAL_PROMPT.md](INITIAL_PROMPT.md). The agent reads the repository and its setup guidance, then leads the complete initialization. The maintainer does not need to open or execute `PROJECT_SETUP.md` separately.

The simplest instruction to the agent is:

> Read `INITIAL_PROMPT.md` in full and carry out the initialization prompt it contains.

There is no need to open the file and copy its prompt into the conversation.

The agent then:

1. reads the collaboration, engineering, setup, documentation, repository and decision rules;
2. inspects the repository baseline without altering Git history;
3. presents concise questions about the problem, desired end state, users, environment, boundaries, roadmap, validation model and code readership;
4. asks for maintainer-owned architecture, sensitive-input and project decisions instead of inventing them;
5. adapts the README files, project context, repository rules and project structure after the maintainer answers;
6. establishes rules for secrets, logs, dumps, screenshots, fixtures, external files and generated outputs;
7. validates the initial technical baseline and prepares the first small project-specific change; and
8. hands back the initialized state with checks, unresolved decisions and suggested commit metadata.

`PROJECT_SETUP.md` remains the agent's detailed checklist and a provenance record of the initialization method. `INITIAL_PROMPT.md` is the single user-facing entry point that activates it.

## External Files and Sources

Place newly received files in `input/intake/` before deciding how they may be used. Record safe metadata, provenance and the resulting classification in `input/INVENTORY.md`; use the ignored `input/INVENTORY.local.md` when filenames, paths or other details are themselves sensitive.

- **`input/intake/`** is the ignored arrival area for files that have not yet been classified. Presence never authorizes assistant access.
- **`input/restricted/`** is ignored and reserved for files that only the maintainer, or explicitly approved local checks, may inspect.
- **`input/local/`** is ignored and holds files the assistant may process locally but that must not enter Git.
- **`input/versioned/`** contains reviewed external files that may be committed. Move files from here into a project-specific source, fixture or configuration location when that location communicates their durable role more clearly, while preserving provenance in the inventory.

Assistant access, Git versioning and external sharing are three separate decisions. A move between folders documents classification; it does not grant broader permission. Fixed runtime locations such as `.env`, application log directories or local databases may remain where the software requires them, but their classification and ignore rules should still be documented.

## Recommended Workflow

Development proceeds through small, validated loops:

```text
Intent -> Roadmap -> Implement -> Validate -> Adjust -> Document -> Prepare commit -> Continue
```

1. Establish the current repository and working-tree baseline.
2. Confirm the active roadmap step and what it should prove or deliver.
3. Implement one logical, reviewable change.
4. Run relevant tests, scripts, linters, renderers or maintainer-local validation.
5. Fix issues found before presenting the step as ready.
6. Update code comments, technical documentation and user-facing guidance affected by the behavior.
7. Record consequential architecture, project or documentation decisions.
8. Prepare a regular working commit with an appropriate Conventional Commit prefix.
9. Close a satisfied milestone separately by harmonizing version, changelog, project context and validated status.

Use [CONTINUATION_PROMPT.md](CONTINUATION_PROMPT.md) for reproducible re-entry, [HARMONIZATION_PROMPT.md](HARMONIZATION_PROMPT.md) for project-content and roadmap alignment and [RETROSPECTIVE_PROMPT.md](RETROSPECTIVE_PROMPT.md) for a separate evaluation of Maintainer-Agent collaboration.

## Git Index and Protected Git Actions

The maintainer controls Git history, normally through GitHub Desktop. Assistants may inspect status, diffs and logs, prepare working-tree changes, propose commit boundaries and provide commit summaries and descriptions.

Staging and unstaging are index operations. They do not require a control word, but they may be performed only after a specific maintainer request or authorization of the corresponding commit. Existing staged selections and unrelated changes must be preserved.

Protected actions include commits, amendments, tags, pushes, pulls, merges, rebases, resets, branch changes, stash manipulation and other Git history operations. An assistant may perform a specific protected action only when the instruction for that action contains `explicit` or `explicitly` in English, or the German word family `explizit`. File-edit approval does not authorize Git history changes, and approval for one protected action does not authorize another.

Regular engineering commits use prefixes such as `feat:`, `fix:`, `docs:`, `refactor:` or `test:`. Milestone commits omit the prefix, name the completed version and close work already implemented and validated through regular commits.

## Decision Records

Choose the record type by decision subject:

- **ADR — Architecture Decision Record:** architecture, interfaces, configuration formats, lifecycle behavior, deployment, security boundaries, sensitive-input handling, fixture versioning or generated-output policy.
- **PDR — Project Decision Record:** scope, roadmap, collaboration, privacy, repository structure, release model or governance.
- **DDR — Documentation Decision Record:** user documentation, reference structure, terminology, examples, screenshots or documentation QA.

Templates live in [decisions/](decisions/). Create a record when future maintainers will need the context, rationale and consequences; routine implementation details belong in code, tests or ordinary documentation instead.

## Repository Structure

### Entry Points and Project Memory

- **`README.md` and `README.de.md`** introduce the software project and explain setup, configuration, use and navigation in English and German.
- **`PROJECT_CONTEXT.md`** is the primary re-entry point for current intent, status, roadmap, baseline, validation and next steps. It should describe the present engineering state, not duplicate the changelog or architecture history.
- **`CHANGELOG.md` and `VERSION`** record completed changes and the latest completed version. They are milestone records and should not imply a release state that has not been validated.

### Collaboration and Engineering Rules

- **`AGENTS.md`** is the concise, automatically loaded entry point for AI agents. It routes them to the complete engineering, collaboration and validation guidance without duplicating it.
- **`ChatGPT.md`** defines the development collaboration model, roadmap rhythm, validation partnership and repository-ready delivery expectations.
- **`CODEX.md`** defines local tool, network, disclosure, multi-repository and Git rules for Codex on the maintainer machine.
- **`PHILOSOPHY.md`** records the engineering values behind the template, including simplicity, maintainability, transparency, validated learning and integrity.
- **`DOCUMENTATION.md`** defines the roles and quality requirements of project, code-level and user-facing documentation. It treats documentation as part of the software.
- **`REPOSITORY.md`** defines naming, Git workflow, commits, versioning, releases, sensitive inputs and repository-ready delivery. It remains an active project rule after setup.

### Setup, Continuation and Review

- **`PROJECT_SETUP.md` and `INITIAL_PROMPT.md`** guide the first initialization and preserve its methodological baseline. Derived projects normally keep them under their original names.
- **`CONTINUATION_PROMPT.md`** reconstructs Git, implementation, validation and documentation state before work continues in a new session.
- **`HARMONIZATION_PROMPT.md`** compares a derived project with its recorded source-template baseline and reconciles code, tests, documentation and roadmap without copying changes blindly.
- **`RETROSPECTIVE_PROMPT.md`** evaluates collaboration practices separately from project content and produces controlled candidates for project or template improvement.

### Decisions, External Inputs and Project-Specific Code

- **`decisions/`** contains reusable ADR, PDR and DDR templates and, in derived projects, accepted durable decisions. The folder should not become a log of every minor implementation choice.
- **`input/`** provides the inventory-based intake and classification workflow for external files and sources. Ignored zones keep unreviewed, restricted and local-only inputs out of Git.
- **Project-specific source, tests, scripts and configuration** are added during initialization according to the technology and architecture chosen by the maintainer. Their layout should be documented when names and structure alone are insufficient for a new contributor.
- **Project-local environments and generated outputs** normally use ignored locations such as `.venv/`, `node_modules/`, `generated/` or `deliverables/`. Document whether generated outputs are reproducible local files, review files or release deliverables.

## Template and Derived Project Files

In a derived development project:

- replace template identity and placeholder content with the concrete project name, purpose, setup and usage;
- fill and continuously maintain `PROJECT_CONTEXT.md`;
- adapt `DOCUMENTATION.md` and `REPOSITORY.md` as ongoing rules;
- normally retain and adapt `AGENTS.md`, `ChatGPT.md`, `CODEX.md` and `PHILOSOPHY.md`;
- retain `PROJECT_SETUP.md`, `INITIAL_PROMPT.md` and the three later-session prompts as provenance and repeatable operating tools;
- add the source, test, configuration and documentation structure required by the project;
- create real Decision Records only for consequential decisions;
- keep the standardized AI Collaboration Note visible and factually accurate.

Record the source-template version and commit, initialization status, last harmonization baseline and intentional deviations in `PROJECT_CONTEXT.md`. A derived project's tested behavior and accepted decisions remain authoritative over later generic template changes.

## How to Use This Template

1. Create a repository from the template and give the agent the instruction in `INITIAL_PROMPT.md`.
2. Answer the numbered questions the agent presents; it reads and applies `PROJECT_SETUP.md` and the remaining setup guidance automatically.
3. Review the initialized repository state, validation results and proposed first commit.
4. Let the agent capture maintainer intent and derive a validation-oriented roadmap.
5. Establish the code, test, documentation and local-tool structure needed by the concrete project.
6. Classify external files through `input/`, keep restricted and local-only inputs outside Git and prefer sanitized fixtures that reproduce behavior without unnecessary disclosure.
7. Implement one logical change at a time and validate it before recommending a commit.
8. Document public behavior, configuration, commands, risks and troubleshooting when they affect use.
9. Record durable decisions, keep `PROJECT_CONTEXT.md` current and use the continuation, harmonization and retrospective prompts when appropriate.
10. Close milestones only after implementation, validation, documentation and version metadata form one coherent state.

## Maintainer Tool Setup

Install only the tools required by the derived project. A practical baseline for local Codex-supported development is:

- [Git for Windows](https://gitforwindows.org/) and [GitHub Desktop](https://desktop.github.com/download/);
- [PowerShell](https://learn.microsoft.com/powershell/scripting/install/installing-powershell-on-windows);
- [ripgrep (`rg`)](https://github.com/BurntSushi/ripgrep/releases) or another fast local search tool;
- [Python](https://www.python.org/downloads/) with a project-local virtual environment when needed;
- [Node.js](https://nodejs.org/en/download/) with project-local dependencies when needed;
- project-specific test, lint, render or build tools.

Prefer local environments such as `.venv/` and `node_modules/` over global installation. Keep environment files, caches, logs, unreviewed inputs and generated working files ignored unless the project deliberately versions a reviewed file or output.

## Continuous Improvement

Development projects should retain practices that have proven useful and remove unnecessary complexity. Validated negative results, recurring validation problems and maintainability lessons are legitimate project knowledge.

Use harmonization to reconcile project content, implementation, tests, documentation and roadmap. Use retrospectives separately to evaluate collaboration, engineering handoffs, validation strategy and work rhythm. A finding becomes a template candidate only after its transferability, maintenance cost and effect on different development projects have been considered.

The maintainer coordinates cross-template evolution in a private governance repository named `agit-templateverse`. It records shared conventions, deliberate specializations and evidence from derived projects. The repository is intentionally not linked because template users do not need access to it.

Governance coordination does not create hidden engineering requirements. Every change that affects this template must be represented here through maintained guidance, Decision Records where appropriate, the changelog and release history. Reusable improvements must keep code, tests, configuration and user-facing documentation aligned and must not overfit one implementation experience.

## License

This project is licensed under the [MIT License](LICENSE).
