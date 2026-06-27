# PROJECT_CONTEXT.md

# Project Context

This document captures the current state of a project created from the AGIT Project Template.

It is the primary entry point for resuming work after a pause, when starting a new AI-assisted collaboration session or when onboarding another contributor.

It should describe where the project stands today. It should not provide the complete project history.

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
<public repository main branch | uploaded ZIP filename | accepted generated artifact>
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
- `CHANGELOG.md` — version history
- `PHILOSOPHY.md` — shared AGIT engineering philosophy
- `ChatGPT.md` — AGIT Collaboration Model
- `<architecture document>` — system structure, if applicable
- `<ADR directory>` — architectural decisions, if applicable

Remove or adapt entries that do not apply to the derived project.

---

# Collaboration Context

AGIT Project Template version:

```text
<template version>
```

Collaboration Model version:

```text
<collaboration model version>
```

Current collaboration notes:

- The repository is the authoritative project state.
- A public repository may be used as the working baseline when accessible.
- A current ZIP archive should be provided when the assistant cannot reliably access the repository state.
- Explicit create or commit requests require actual repository-ready deliverables.
- Feature commits and milestone commits should remain separate.
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
