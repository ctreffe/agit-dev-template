# AGENTS.md

This file is the automatically loaded entry point for AI agents working in an
AGIT Dev Template repository. Keep it concise: it routes agents to the
repository's authoritative guidance and does not replace that guidance.

## Before Substantive Work

1. Read `CODEX.md` in full before using tools or changing files. It defines the
   local operating policy, access boundaries and protected Git actions.
2. Read `ChatGPT.md` for the development collaboration model.
3. Read `README.md`, `PROJECT_CONTEXT.md`, `REPOSITORY.md`, `DOCUMENTATION.md`
   and `PHILOSOPHY.md` as relevant to the task.
4. Inspect the actual source, tests, configuration and Decision Records affected
   by the requested change before designing an implementation.
5. For initialization, continuation, harmonization or retrospective work,
   follow the corresponding prompt file instead of reconstructing its workflow.

If repository guidance appears inconsistent, report the conflict and ask for a
maintainer decision when it could materially affect the result.

## Working Agreement

- Confirm the active repository and inspect its current Git state before edits.
- Preserve existing staged selections, working-tree changes and unrelated work.
- Treat maintainer intent, architecture, roadmap and consequential decisions as
  human-owned.
- Prefer the smallest maintainable implementation that satisfies the stated
  goal and preserves human code readability.
- Keep code, tests, configuration and user-facing documentation synchronized.
- Keep private inputs, secrets, logs, dumps and generated working files out
  of Git unless a separate reviewed decision permits them.
- Classify new external files through `input/`; presence in `input/intake/`
  never authorizes assistant access.
- Use project-local environments and existing tools; do not add or update
  dependencies without a concrete need and maintainer approval.
- Follow the authorization rules in `CODEX.md`; an edit request does not by
  itself authorize protected Git actions.

## Validation and Handoff

Run the repository's relevant tests, linters, formatters, builds or validation
scripts. At minimum, review the diff and run `git diff --check`. Validate local
Markdown links and English/German structural alignment when documentation is
affected.

Report the outcome, changed files, checks performed, limitations or skipped
checks and suitable commit metadata. Do not present an implementation as ready
when relevant validation is missing or failing.
