# Harmonization Prompt

Use this prompt for a deliberate development-project harmonization. It compares
a derived project with its recorded source template, checks the internal
consistency of code and repository documentation and reviews roadmap fit.

Harmonization concerns project content. It does not evaluate Maintainer-Agent
collaboration and does not derive improvements for the source template.

Invoke it with `Read and execute HARMONIZATION_PROMPT.md.`

## Prompt

```text
Perform a structured content harmonization of this development project.

The concrete project, maintainer intent, architecture and project Decision
Records remain authoritative. Never copy template changes blindly.

1. Read CODEX.md and ChatGPT.md for authority, safety and Git rules.
2. Read PROJECT_CONTEXT.md, including repository role, source template,
   baselines, intentional deviations, roadmap and human code readership.
3. Read README.md, VERSION, current CHANGELOG.md sections, DOCUMENTATION.md,
   REPOSITORY.md, PHILOSOPHY.md, relevant Decision Records and active
   architecture, source, test, configuration and user-documentation files.
4. Inspect branch, working tree, recent commits, relevant tags and staged or
   unstaged changes with read-only Git commands. Preserve uncommitted work.
5. Apply sensitive-input, secret, fixture, generated-artifact and publication
   rules before opening or validating project materials.

For a derived project, locate the exact source template and last recorded
harmonization baseline, then establish the latest verifiable template baseline.
Do not assume that a local template clone is current; use authoritative
read-only remote evidence when it is available and permitted. If freshness or a
baseline cannot be verified, stop the external comparison at metadata level
and ask for the missing path, version or commit. Do not substitute another
template or compare with unrelated repositories.

Classify each material template change as adopt, adapt, reject or defer. Record
the rationale, affected project files and any Decision Record or intentional
deviation that governs the result. Project architecture, supported behavior,
maintainer intent and validated project-specific rules override template
defaults. Present conflicts as numbered maintainer decisions before editing.
Never modify the source-template repository during harmonization.

If this repository is itself a template, do not infer a parent template. Skip
the external comparison.

Perform an internal development consistency pass across:

- project identity, version, changelog, status and completed milestones
- roadmap objectives, dependencies, validation and intentional non-goals
- architecture, source, tests, configuration and Decision Records
- public behavior, setup, usage, reference and troubleshooting documentation
- dependency, environment, build, packaging and release guidance
- human-readable English code documentation for assistant-authored code
- sensitive inputs, sanitized fixtures, generated artifacts and ignore rules
- actual test or validation evidence versus documented claims
- working-commit state versus milestone-closure state

Review whether the roadmap still fits project intent, the implemented system,
known constraints and remaining work. Propose concrete content changes without
inventing product direction or resolving maintainer-owned tradeoffs.

Harmonization is not a retrospective. Do not evaluate the collaboration or
derive template improvements. Defer collaboration observations to a future
retrospective and do not implement template feedback.

Before edits, provide a concise numbered report:

1. repository role and project/template baselines
2. template comparison matrix: change, adopt/adapt/reject/defer, rationale,
   affected files and decision needed
3. code, test, documentation and repository consistency findings
4. roadmap findings and proposed project-content changes
5. validation, security and disclosure checks required
6. proposed edit and commit-sized work sequence
7. collaboration observations deferred to a retrospective
8. blocking maintainer decisions

Apply findings only when my instruction clearly authorizes implementation, and
only after reporting. Stop at project conflicts. After approved edits, validate
the affected behavior and documentation. Update the last harmonization baseline
and deviations in PROJECT_CONTEXT.md only after the comparison and integration
actually succeed.

Staging and unstaging do not require a control word, but perform them only when
I specifically request the index action or authorize the corresponding commit.
Preserve existing staged selections and unrelated changes.

Do not perform a protected Git action unless I instruct you to perform that
specific action with a recognized control word: `explicit`, `explicitly` or the
German word family `explizit`.
```
