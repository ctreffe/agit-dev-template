# Create Local Project Prompt

Use this prompt from a local Template repository to create a new, locally
versioned project without a GitHub or other remote repository.

## Prompt

```text
Create a new local project by cloning this checked-out Template repository.

Apply AGENTS.md and CODEX.md as the source repository's operating baseline.
This is a project-creation workflow, not a Templateverse membership or derived-
project registration workflow. Do not add the new project to a governance
registry or modify the source template.

First ask me for the absolute target directory if I have not supplied one.
It may be a new directory, an existing empty directory, or a directory that
contains only an empty Git repository with no commits and no project files.

Before changing anything, verify that:

- the source is this local checked-out Git repository with a valid HEAD;
- the target is an absolute path, differs from the source, and is not inside
  this template, the Templateverse governance repository, or a registered
  Templateverse member repository;
- the target either does not exist, is empty, or contains only `.git` for an
  unborn repository with no commits and no other files;
- no existing files, commits, remotes, or nested repository would be replaced.

If the target contains only an unborn `.git` directory, explain that removing
it is required before cloning and ask for my explicit confirmation. If the
target contains anything else, stop without changing it and ask how to proceed.

After the checks, show me the exact target path and ask for confirmation before
creating the new local project. On confirmation, clone only from this local
source path using `git clone --no-local`. Do not contact GitHub or another
network service. Remove the clone's `origin` remote immediately after a
successful clone; do not add any replacement remote, push, publish, or change
the source template.

Verify and report the target path, active branch, inherited HEAD, clean or
dirty working-tree state, and that no remotes remain.

Then read the new project's AGENTS.md and CODEX.md before any further work.
Find its unambiguous `INITIAL_PROMPT.md`, report that you found it, and execute
its initialization workflow. If it is missing or ambiguous, stop and ask me
which initialization instruction to use. Preserve all local access, privacy,
source, Git-index and protected-Git-action rules of the new project.
```
