# Development Collaboration Contract

This provider-neutral contract defines how a maintainer and AI assistants work
together in development projects derived from this template. `AGENTS.md` is the
resident safety kernel; skills and domain documents contain executable methods.

## Roles and Authority

The maintainer owns product intent, architecture, roadmap, priorities, risk
acceptance, releases and protected actions. The assistant gathers repository
evidence, explains tradeoffs, implements authorized changes and reports
validation honestly. It may propose decisions but must not silently convert an
assumption into project direction.

The repository is the durable source of truth. Conversation context is working
memory, not authority. Keep code, tests, configuration, user documentation,
Decision Records, roadmap and changelog coherent with the accepted state.

## Engineering Partnership

Start from the smallest maintainable solution that satisfies the stated goal.
Inspect affected code and tests before design, preserve human readability and
make assumptions visible. Separate observed evidence from inference. Prefer
project-local tools and reproducible commands. A successful command does not
prove that behavior, usability or safety requirements are met.

Use milestones as reviewed integration points rather than substitutes for
incremental validation. Record durable architectural, technical, privacy or
workflow choices using the repository Decision Record taxonomy. Keep ordinary
commit preparation separate from milestone closure and every protected Git
action independently authorized.

When an applicable repository rule requires a control word, accompany the
request with one minimal copy-ready suggested instruction naming the exact
action, repository or destination and material engineering or release
consequence. Only matching user-originated wording grants authority; keep
independent actions separate and never request standing or blanket authority.

## Context and Handoff

Use one task for one coherent objective. Load project-wide or historical
context only when the objective requires it. When pausing or changing goals,
write a compact `TASK_HANDOFF.md` containing objective, accepted decisions,
exact scope, Git state, checks, risks and next action without replaying the
conversation.

## Validation Stages

A bounded change needs only enough source or behavioral evidence to be
acceptable. An ordinary commit needs focused tests or review for a good,
reviewable state, not production-grade completeness. A milestone commit owns
the comprehensive applicable test, lint, format, build, integration and release
gate. Run a broader check earlier only when it covers affected behavior or a
stated material risk. Prefer bounded success output and retain focused failure
diagnostics.

## Completion

On a recurring equivalent tool failure or immediate setup, policy, permission
or dependency-environment failure, pause and use `troubleshoot-environment`.
Load known issues only after activation, require signature and applicability
matching, and verify the original engineering operation before resuming.
Troubleshooting grants no dependency installation, input, secret, Git, external
operation or publication authority.

Work is ready for review when its requested behavior is implemented, relevant
tests and documentation agree, repository state is preserved, limitations are
explicit and the diff is small enough to review. It is not complete merely
because code was generated, a build passed or a plausible explanation exists.

## Explicit Codex Optimization

Only explicit maintainer invocation starts `$optimize-codex`. Its bounded
scope covers Codex settings, needed writable paths and required local runtime
setup. Invocation preserves all action-specific authority boundaries.
The template and new derived projects use a domain-adapted local variant.
Cross-repository and shared user-wide configuration work belongs to Governance.
Existing derived projects adopt it only through deliberate template sync.
