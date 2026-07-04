# Initial Prompt

Use this prompt as the first instruction to the AI assistant after creating a new project repository from the AGIT Dev Template.

The purpose is to make the first session reproducible: the assistant should read the repository, understand all template rules, ask for the required maintainer-owned information, initialize the project files and prepare the first project-specific setup state without taking Git history actions unless explicitly instructed.

---

# Prompt

```text
We are starting a new development-oriented AGIT project from the AGIT Dev Template.

Please first read the repository fully enough to understand its structure,
collaboration model, Codex policy, setup guide, documentation standards,
repository standards, project context template, current placeholders and
initialization rules.

Pay special attention to:

- README.md
- PROJECT_SETUP.md
- DOCUMENTATION.md
- REPOSITORY.md
- PROJECT_CONTEXT.md
- ChatGPT.md
- CODEX.md
- PHILOSOPHY.md
- CHANGELOG.md
- VERSION

Then initialize this repository as a concrete project.

Follow PROJECT_SETUP.md. Ask me for all maintainer-owned information that is
required before implementation should begin, including the problem space,
operating context, desired end state, intended users or maintainers,
boundaries, non-goals, first roadmap milestones, validation expectations,
repository metadata and any project-specific collaboration constraints.

Before reading raw private, confidential or personal development material such as `.env` files, logs, dumps, API responses, screenshots or customer data, inventory it at the metadata level and ask whether direct inspection is allowed or whether a sanitized derivative should be used.

Do not invent the project intent, roadmap, architecture, validation status or
repository direction. You may ask clarifying questions, point out gaps and give
feedback on structure, consistency, scope and feasibility, but I remain in
control of project direction and durable decisions.

After I provide the required information, update the project-specific files:

- README.md
- README.de.md, if kept
- PROJECT_CONTEXT.md
- CHANGELOG.md
- VERSION, if appropriate
- any project-specific documentation created during setup

Preserve the collaboration model in ChatGPT.md and the local Codex policy in
CODEX.md unless I explicitly ask to change them.

Review template-only initialization files and recommend whether they should be
removed or retained for onboarding, traceability or future re-initialization:

- PROJECT_SETUP.md
- INITIAL_PROMPT.md
- DOCUMENTATION.md
- REPOSITORY.md

Do not rename retained initialization files. If retention is useful, add a
short status note inside the retained file or document the decision in
PROJECT_CONTEXT.md.

Do not stage, commit, tag, push, pull, merge, reset, rebase, switch branches or
otherwise modify Git history unless I explicitly instruct you to perform that
specific Git action.

When the setup state is ready, provide:

- a concise change summary
- checks performed
- known limitations or open questions
- a suggested commit summary
- a suggested commit description
- any short next steps I should take in GitHub Desktop
```
