---
name: troubleshoot-environment
description: Resolve a concrete recurring or clear setup, policy, permission or toolchain problem, either after the resident trigger pauses ordinary work or when the maintainer explicitly invokes the skill for a known environment problem. Do not use for general optimization or expected code or test failures without infrastructure evidence.
---

# Troubleshoot Environment

Remove the cause of one concrete engineering-environment problem without
broadening the suspended task.

## Activation and route choice

On implicit activation, suspend the task and state only a concise description
of the observed problem, failed operation and environment boundary. Do not
diagnose or load incident records before the maintainer chooses:

1. **Quick exit:** End this skill. The ordinary task agent may seek a safe
   task-local workaround under normal boundaries. Perform no skill analysis,
   create no incident record and make no recovery claim.
2. **Problem resolution:** Continue with the focused workflow below.

Explicit maintainer invocation for a concrete known or recurring environment
problem enters resolution directly. Clarify as needed; do not offer the quick
exit. General optimization is outside this skill.

## Focused problem resolution

1. Retain the exact failing checkpoint, or agree on a concrete acceptance test
   before changes for standalone invocation.
2. Load `TROUBLESHOOTING.local.md` when present and then
   `TROUBLESHOOTING.md`. Reuse a repair only after signature, applicability and
   a safe diagnostic reconfirm the same cause.
3. Investigate only this problem and recurrence risk. Diagnostic commands and
   diagnostic tests are allowed. Ask maintainer questions and proactively
   request concrete elevated authority whenever it enables an effective durable
   repair. State its exact scope and material security consequence; the
   maintainer owns the security judgment and critical questions. Do not suppress
   the option or weaken the solution merely to avoid elevated permission.
4. Implement the smallest authorized repair that removes the cause and prevents
   recurrence. Preserve architecture, dependencies, tests, inputs, materials,
   local toolchains and release controls. Troubleshooting grants no privilege,
   installation, credential, external, security or Git authority. When a
   repository control word is required, propose one minimal copy-ready
   instruction naming the exact recovery action, repository and material
   consequence; the proposal is not authorization.
5. Do not write a fix-specific test or insert substitute validation. Return to
   the exact checkpoint and continue the original operation normally; its
   success is the repair evidence. For standalone invocation, run the agreed
   acceptance test. Continue or reassess the repair loop if the evidence fails.
6. Only this route may update `TROUBLESHOOTING.md` with a portable problem,
   confirmed cause, diagnostic, durable repair, authority needs and verified
   acceptance path. An unresolved investigation remains an open task with its
   smallest next diagnostic step. Put host facts in ignored
   `TROUBLESHOOTING.local.md`; never record secrets or a quick-exit workaround.
7. Resume or close the original task only after the blockage is gone.
