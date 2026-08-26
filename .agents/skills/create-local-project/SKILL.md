---
name: create-local-project
description: Create a new local derived-project repository from a regular source template, remove template-only creation machinery and hand off to project initialization.
---

# Create Local Project

Confirm the source template, target path, target emptiness and intended local-only
Git state. Create the project with history preserved through a local clone that
does not share object storage, remove the inherited remote and verify that no
remote remains.

Read the new repository's own instructions before invoking `start-project`.
That initialization replaces inherited source-template maintenance history in
`CHANGELOG.md` and `TASK_HANDOFF.md` with project-owned state while retaining
lineage in `PROJECT_CONTEXT.md`. After successful initialization, remove only
the project copy of this template-only creation skill and other explicitly
identified template-only artifacts. Preserve initialization and setup documents
as provenance. Repository creation, cleanup, commits and remote configuration
remain separately governed operations.
