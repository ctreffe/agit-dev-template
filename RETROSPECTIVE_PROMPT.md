# Retrospective Prompt

Use this prompt when the maintainer requests a review of development
collaboration over a selected milestone, project phase or other defined period.
It evaluates Maintainer-Agent collaboration rather than project content.

Invoke it with `Read and execute RETROSPECTIVE_PROMPT.md.`

## Prompt

```text
Perform a structured retrospective of Maintainer-Agent collaboration in this
development project.

Do not use this retrospective to harmonize code, documentation or roadmap
content. Hand project-content implications to a later harmonization.

1. Read CODEX.md, ChatGPT.md and PROJECT_CONTEXT.md.
2. Read the relevant roadmap or milestone record, current CHANGELOG.md sections
   and collaboration-related Decision Records.
3. Read CONTINUATION_PROMPT.md and HARMONIZATION_PROMPT.md to preserve prompt
   boundaries.
4. Inspect relevant commit history, validation handoffs, review artifacts and
   documented decisions with read-only commands and subject to documented
   access boundaries. Preserve uncommitted work.
5. Use current-session evidence and maintainer reports, but do not claim access
   to unavailable earlier chats.

Label material findings as repository evidence, current-session observation,
maintainer report or inference. Avoid conclusions based only on commit counts
or a single unexplained event.
Do not inspect secrets, raw logs, dumps, customer data or other sensitive inputs
merely to evaluate collaboration.

Evaluate:

- roadmap-to-working-step translation and commit-sized work rhythm
- clarity and timing of maintainer decisions and numbered handoffs
- implementation, validation, review and correction loops
- distinction between working commits and milestone closure
- accuracy of commit summaries, descriptions and completion claims
- human readability of assistant-authored code and English documentation
- validation partnership when local or elevated execution is required
- handling of secrets, logs, dumps, fixtures and generated artifacts
- tool, capability and Git-authority boundaries
- practices to retain and recurring causes of friction or rework

Classify outcomes as retain, adjust in project, hand to harmonization, template
candidate or no action. Content, architecture, behavior and roadmap changes go
to harmonization. Template candidates must be transferable, sanitized,
evidence-based and checked against overfitting.

Do not change the source-template repository unless I authorize the specific
template change with `explicit`, `explicitly` or the German word family
`explizit`. Running the retrospective or approving concrete-project edits is
not template-change permission. If this repository is itself a template, the
same control-word rule applies to changes in its reusable collaboration model.

Template-edit permission is separate from Git history permission. Each stage,
commit, tag, push, pull, merge, rebase, reset or branch action still requires a
specific maintainer instruction containing a recognized control word.

Before edits, report:

1. scope and evidence
2. practices to retain
3. friction points, likely causes and confidence
4. proposed project collaboration changes
5. content or roadmap implications for harmonization
6. abstracted template candidates and overfitting risks
7. no-action observations
8. maintainer decisions

Apply only agreed project collaboration changes when my instruction clearly
authorizes them. Do not apply content changes or template candidates. After
approved edits, harmonize affected collaboration documents, validate references
and record durable project decisions where useful. Update the last
collaboration retrospective in PROJECT_CONTEXT.md only when its scope and
outcome are accurately recorded.
```
