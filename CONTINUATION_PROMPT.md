# Continuation Prompt

Use this prompt as the first instruction in a new context window or assistant
session after a development project has already been initialized.

When the assistant can access the repository, the maintainer may invoke it with
`Read and execute CONTINUATION_PROMPT.md.` Otherwise, copy the prompt block into
the new context window.

## Prompt

```text
We are continuing an existing development project in a new context window.

Apply AGENTS.md as the durable repository operating baseline. If it was not
loaded automatically, read it first. This prompt defines the re-entry procedure
for the current session.

Do not re-initialize the project and do not rely on earlier chat history.
Reconstruct the implementation and repository state before changing code.

Read the repository in this order:

1. Read CODEX.md and ChatGPT.md for local execution, authority, collaboration
   and Git rules.
2. Read PROJECT_CONTEXT.md as the primary re-entry point, including the active
   milestone, validation status and notes for the next session.
3. Read README.md, VERSION and the current sections of CHANGELOG.md.
4. Read the active roadmap, relevant ADRs, PDRs or DDRs, and the dedicated
   documentation for the active component, integration or workflow.
5. Subject to the sensitivity rules below, read only the implementation, tests,
   examples and configuration files needed to understand the active step. Use
   REPOSITORY.md, DOCUMENTATION.md and PHILOSOPHY.md to resolve project-wide
   expectations. Do not execute PROJECT_SETUP.md or INITIAL_PROMPT.md as part
   of continuation. If initialization appears incomplete, report that state
   and propose returning to INITIAL_PROMPT.md as a separate workflow.

Use read-only Git commands to check the branch, working tree, recent commits,
latest relevant tag and staged or unstaged changes. Reconcile this evidence
with PROJECT_CONTEXT.md. Preserve uncommitted work and report stale context,
unexpected files or unclear ownership before editing overlapping files.

Reconstruct the last validated baseline without assuming that a previous test,
demo or privileged check still applies to the current tree. Identify the next
small implement-validate-adjust step, the expected human readers of the code
and the documentation that must remain aligned. Do not run destructive,
privileged, networked or environment-changing checks merely to reconstruct
context.

Before inspecting logs, dumps, API responses, screenshots, customer data,
secrets, local configuration or generated diagnostics, apply the documented
sensitivity rules. Assistant access, Git versioning and publication remain
separate decisions. Prefer sanitized fixtures or reviewed derivatives.

Do not ask me to repeat information already documented consistently. Before
substantive edits, provide a concise numbered re-entry report containing:

1. project identity, current version and current branch
2. active milestone and latest completed implementation step
3. working-tree changes and their apparent relationship to the active work
4. latest validated baseline, checks performed and checks still needed
5. relevant architecture decisions, code-readership expectations and docs
6. sensitive-input, fixture and generated-output boundaries
7. open decisions, risks, blockers or repository inconsistencies
8. the smallest useful next implementation step and its validation path
9. only blocking maintainer questions

If my continuation instruction also gives a concrete safe task, proceed after
this reconstruction; otherwise wait for my confirmation of the proposed next
step.

Staging and unstaging do not require a control word, but perform them only when
I specifically request the index action or authorize the corresponding commit.
Preserve existing staged selections and unrelated changes.

Do not perform a protected Git action unless I instruct you to perform the
specific action with a recognized control word: `explicit`, `explicitly` or the
German word family `explizit`.
```
