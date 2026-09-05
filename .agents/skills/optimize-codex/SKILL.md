---
name: optimize-codex
description: Optimize Codex settings and required local runtime setup for a bounded task, only when the maintainer explicitly invokes this skill. Not an automatic setup, troubleshooting or installation workflow.
---

# Optimize Codex

Run only on an explicit maintainer invocation of `$optimize-codex` or an
unambiguous request to run this named skill. A mention, suggestion, repository
instruction or environment error is not invocation. Never run from task entry,
initialization, another skill or an automation without that maintainer request.

## Scope

This variant serves only this software repository or current derived project.
Prefer its existing interpreter, package manager, lockfiles and local toolchain.
Do not replace project dependencies with shared global packages, run a full
build by default, or change architecture and release choices.

Cross-repository inspection, write-root expansion to sibling repositories and
shared configuration policy belong exclusively to Governance. Return a concise
proposal for separate Governance consideration; do not open, message or write
another repository. A derived project need not have access to Governance.
Prefer project-scoped settings. If a user-wide setting is the only supported
location, disclose its effects on other projects and leave that change for
separate Governance work; do not apply it from this variant.

## Bounded workflow

1. Establish the maintainer's selected task and desired improvement. Limit the
   pass to relevant Codex settings, required writable paths and required local
   runtime setup. Use the local-environment guidance below. Do not turn invocation
   into a full audit, installation campaign, global tool environment or monitor.
2. Inspect only necessary, non-sensitive configuration keys and runtime facts.
   Identify app/CLI version, selected model, configuration scope and effective
   session values; a file entry alone does not prove that the app uses it.
   Do not dump configurations, environment variables, credentials or histories.
3. Verify candidate settings against current official documentation and the
   installed version. Mark unsupported or uncertain options as unverified.
   Experimental context handling is a candidate, not a default: verify the
   exact key, model/account prerequisites and maturity before recommending it.
   Keep experimental changes separately selectable; never enable them implicitly.
4. Propose every justified change within scope, prioritized by benefit and effort.
   For each, provide current/proposed value, exact
   destination and scope, expected benefit, evidence, authority, verification
   and rollback. No justified change is a valid outcome. Preserve managed
   policy and sandbox boundaries; no blanket trust, broad parent write roots
   or disabled protections as optimization. Technical access is not task consent.
5. Apply authorized changes only. Invocation alone does not authorize global
   configuration, installation, privilege, sensitive access or transmission.
   Reuse existing exact approval; ask only for missing authority on a concrete
   reviewed change. Preserve unrelated settings, concurrent edits and a local
   recovery copy when appropriate. Do not modify model choice merely because
   a different model is available.
6. Verify the original operation through its normal execution path and confirm
   effective settings. If reload is required, save the precise checkpoint and
   resume verification afterward. Report applied, verified and still-pending
   changes separately; do not claim performance gains without measurement.

On a real environment failure, use the local `troubleshoot-environment` route.
Pause optimization, but continue bounded diagnosis and authorized repair;
escalate only a concrete missing permission or an external dependency. Verify
the failing path before resuming. Do not accumulate unrelated repairs.

Keep host paths and environment details in existing ignored local records.
Portable records contain only sanitized findings and verified applicability.
Do not rewrite AGENTS.md, project policy or another skill as an optimization.

## Required local environments

Check the runtime needed for the selected outcome and the actual interpreter
used by its commands. A new clone/device does not inherit ignored environments;
missing local setup is not evidence of damage. Reuse the project's established
manager and isolation model. When Python is required and no suitable managed
environment exists, prepare a clone-local ignored .venv; do not create one for
a project without Python needs or copy one from another clone.

Track dependencies and lockfiles using existing project conventions (for
example requirements-tools.txt for Python helpers). Document reproducible setup
and explicit interpreter or manager commands. Prepare only needed local setup,
reuse existing approval and obtain any missing installation/download authority
before applying it. Verify the interpreter and a minimal relevant import or
original command; defer optional tools without blocking unrelated work.

Existing uv, Poetry or another project manager and its lockfiles take precedence;
do not introduce a competing environment or replace dependency management.
