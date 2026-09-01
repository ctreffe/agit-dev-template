# Project Context Template

Use this file as the current-state re-entry point in a project created from the
AGIT Dev Template. Replace the placeholders during initialization and keep the
result focused on present intent, baseline, active work, validation and next
steps. History belongs in `CHANGELOG.md`; durable rationale belongs in Decision
Records; detailed methods belong in the relevant domain documents.

## Template Lineage and Initialization

- **Repository role:** `<derived project>`
- **Source template:** AGIT Dev Template
- **Initial template baseline:** `<version and commit>`
- **Initialization:** `<not started | in progress | completed; date>`
- **Last template harmonization:** `<not yet | baseline and date>`
- **Last retrospective:** `<not yet | reviewed period, date and record>`
- **Intentional deviations:** `<none | concise list and Decision Records>`

Keep `PROJECT_SETUP.md` as initialization provenance. Initially record only the
six fundamental answers, first useful capability and current safety boundary;
defer architecture, tooling, tests, deployment and release detail until a
concrete task needs it.

## Project Intent

- **Project name:** `<name>`
- **Repository:** `<URL or local baseline>`
- **Short description:** `<one or two sentences>`
- **Problem and users:** `<operating context and intended users>`
- **Desired end state:** `<useful outcome and quality bar>`
- **Boundaries and non-goals:** `<excluded or postponed behavior>`
- **First roadmap implication:** `<first useful milestone and why>`
- **Human code readership:** `<maintainers, reviewers and language standard>`

The maintainer owns this intent. The assistant may clarify and structure it,
but must not invent the project's purpose or consequential decisions.

## Access, Storage and Publication Boundary

- **Sensitive inputs and Git rules:** `<logs, dumps, screenshots, data and ignores>`
- **Input catalog:** `<input/CATALOG.md and optional PATHS.local.md entries>`
- **Synchronized storage:** `<not used | project ID, roots and state>`
- **Assistant access:** `<exact sources or sanitized derivatives and task>`
- **Git versioning:** `<exact approved fixtures or outputs | none>`
- **Retained materials:** `<catalog entries, source relation and storage state>`
- **Promotion into maintained files:** `<source, tests, fixtures or docs>`
- **Publication or external sharing:** `<exact artifacts and audience | none>`

Access, Git versioning and publication are separate decisions. Do not infer one
from another.

## Current State

- **Current version:** `<latest completed version>`
- **Milestone:** `<active milestone>`
- **Focus:** `<current engineering objective>`
- **Status:** `<planned | development | validation | paused | completed>`
- **Working baseline:** `<local tree | public branch | archive | accepted output>`
- **Baseline notes:** `<state required for the next contribution>`

## Roadmap and Milestones

Completed:

- `<version or tag>` — `<validated milestone>`

Next:

- `<next step>` — `<uncertainty reduced or behavior proved>`
- `<later step>` — `<planned focus>`

Keep roadmap entries reviewable. Work in progress belongs in Current State,
not in the completed list.

## Validation

Validated:

- `<behavior and evidence>`

Not yet validated:

- `<open check or limitation>`

Immediate validation target: `<next relevant check>`

## Decisions

Open:

- `<unresolved or deliberately deferred decision | none>`

Important accepted decisions:

- `<decision and Decision Record when applicable>`

Record durable architecture or project decisions in the local taxonomy instead
of expanding their rationale here.

## Relevant Documents

- `README.md` — user-facing entry point
- `PROJECT_SETUP.md` — initialization method and provenance
- `TASK_HANDOFF.md` — compact current-task checkpoint
- `COLLABORATION.md` and `AGENTS.md` — collaboration and resident safety
- `PHILOSOPHY.md`, `REPOSITORY.md`, `DOCUMENTATION.md` — engineering rules
- `TROUBLESHOOTING.md` — conditionally loaded recovery patterns
- `SYNCHRONIZED_STORAGE.md` — external storage mapping
- `.agents/skills/` — lifecycle and specialized workflows
- `decisions/` — durable choices
- `CHANGELOG.md` — completed version history
- `input/`, `materials/`, `temp/`, `output/` — governed artifact locations
- `<architecture or domain document>` — `<purpose>`

Remove or adapt entries that do not apply.

## Next Session

- **Objective:** `<one coherent next objective>`
- **Start from:** `<exact baseline and active artifacts>`
- **Preserve:** `<user work, inputs, selections and non-goals>`
- **Checks pending:** `<specific checks>`
- **Next action:** `<single practical step>`

Update this file after material state changes and before a long-session handoff.
Feature and milestone commits remain separate; protected Git actions require
their own explicit authorization.
