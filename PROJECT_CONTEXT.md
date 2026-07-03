# PROJECT_CONTEXT.md

# Project Context Template

This document is a project-context template for repositories created from the AGIT Dev Template.

In a derived project, this file should be adapted to capture the current state of that project.

After adaptation, it becomes the primary entry point for resuming work after a pause, when starting a new AI-assisted collaboration session or when onboarding another contributor.

It should describe where the derived project stands today. It should not provide the complete project history.

The placeholders in this file are intentional. Replace them during project setup.

---

# Project

Project name:

```text
<project name>
```

Repository:

```text
<repository URL>
```

Short description:

```text
<one or two sentences describing the project>
```

---

# Maintainer Project Intent

Maintainer-owned initial context:

```text
<problem space, operating context, target users or environment>
```

Desired end state:

```text
<what the project should enable, feel like or technically achieve when successful>
```

Initial boundaries and non-goals:

```text
<what the project should not do, should avoid or should intentionally postpone>
```

Roadmap implications:

```text
<how the context and desired end state shape the first milestones>
```

The maintainer should provide this section at project start. It should guide the initial roadmap and help future sessions understand why the roadmap has its current shape.

---

# Current Status

Current project version:

```text
<latest completed version>
```

Current phase or milestone:

```text
<current milestone name>
```

Current focus:

```text
<what the project is currently working on>
```

Status:

```text
<planned | in development | validation | completed | paused>
```

---

# Repository Baseline

Current working baseline:

```text
<local working tree | public repository main branch | uploaded ZIP filename | accepted generated artifact>
```

Baseline notes:

```text
<notes about the repository state that should be used for the next contribution>
```

This section should make it clear which repository state is authoritative for the next work session.

---

# Completed Milestones

- `<version or tag>` — `<milestone summary>`
- `<version or tag>` — `<milestone summary>`

Only include completed milestones. Work in progress belongs in the current status and roadmap sections.

---

# Current Roadmap

- `<next step>` — `<planned focus>`
- `<later step>` — `<planned focus>`

Roadmap entries should be small enough to validate.

For proof-of-concept work, phrase roadmap entries around the uncertainty they reduce or the behavior they prove.

---

# Validation Status

Document what has been validated and what has not.

Validated:

- `<validated behavior>`

Not yet validated:

- `<open validation item>`

Validation notes:

```text
<important observations from real-system tests or reviews>
```

---

# Open Decisions

List decisions that are unresolved or intentionally postponed.

- `<decision>`
- `<decision>`

If there are no open decisions, state that explicitly.

---

# Important Decisions Already Made

Summarize decisions that are important for continuing the project.

Detailed reasoning should remain in ADRs where applicable.

- `<decision>`
- `<decision>`

Include validated negative findings here when they affect future work.

---

# Relevant Documents

Use this section as a navigation aid.

- `README.md` — project overview and user-facing entry point
- `INITIAL_PROMPT.md` — first prompt for reproducible project initialization, if kept after setup
- `CHANGELOG.md` — version history
- `PHILOSOPHY.md` — shared AGIT engineering philosophy
- `ChatGPT.md` — AGIT Collaboration Model
- `CODEX.md` — local Codex operating policy, if Codex is used
- `<architecture document>` — system structure, if applicable
- `<ADR directory>` — architectural decisions, if applicable

Remove or adapt entries that do not apply to the derived project.

---

# Collaboration Context

AGIT Dev Template version:

```text
<template version>
```

Collaboration Model version:

```text
v1.16
```

Current collaboration notes:

- The repository is the authoritative project state.
- A local repository working tree may be used as the working baseline when accessible to the assistant.
- A public repository may be used as the working baseline when accessible.
- A current ZIP archive should be provided when the assistant cannot reliably access the repository state.
- Explicit create or commit requests require actual repository-ready deliverables.
- Integrity has priority over apparent helpfulness: artifacts must exist before they are reported as delivered.
- Capability limitations should be stated directly instead of hidden behind simulated completion.
- Required template artifacts such as the AI Collaboration Note should remain visible and factually accurate unless intentionally modified.
- Template-only initialization files may be removed or retained after setup depending on project needs; retained files should keep their original names.
- If Codex is used locally, `CODEX.md` defines the local operating policy.
- Long-running sessions should update `PROJECT_CONTEXT.md` before context exhaustion becomes likely.
- When a change is approaching commit readiness, the assistant should provide concise numbered next steps for decisions, validation, review and commit actions whenever practical.
- Projects should establish an explicit initial roadmap before implementation accelerates, including early milestones, purpose, intended validation and intentional non-goals.
- Initial roadmaps should be derived from maintainer-owned project intent, context, desired end state and boundaries.
- Active milestones should progress through small implement-validate-adjust-prepare loops, with feature commit guidance kept separate from milestone commit guidance.
- Commit recommendations should include both a concise summary and a meaningful description.
- Assistant-written code should be documented and structured so maintainers and future contributors can understand it without private chat history.
- User-facing documentation should explain setup, configuration, productive usage, reference surfaces and troubleshooting where relevant.
- Substantial modules, integrations or workflows should use dedicated documentation instead of overloading the README.
- Substantial production components should include a demonstration, example configuration or validation path when applicable.
- Before preparing a milestone commit, documentation should be checked for version, status, roadmap, changelog, README, dedicated-documentation links, setup guidance and validation freshness.
- When validation requires maintainer-local or elevated execution, the assistant should provide exact steps, interpret the output and document relevant validation results.
- Feature commits and milestone commits should remain separate.
- Git history actions are maintainer-controlled. Assistants may prepare changes and commit metadata, but must not stage, commit, tag or push without explicit maintainer instruction for that specific action.
- Validation should happen before declaring a step complete.

Adapt this section when the project intentionally uses different collaboration rules.

---

# Notes for the Next Session

Use this section to make restarting work easy.

Examples:

- what to do next
- what not to change yet
- what information needs to be verified
- what repository state should be used
- what was validated in the previous session

```text
<notes>
```


