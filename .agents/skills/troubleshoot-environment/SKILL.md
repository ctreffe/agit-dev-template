---
name: troubleshoot-environment
description: Diagnose and recover from recurring or clear setup, policy, permission and toolchain failures after the resident repository trigger pauses ordinary work. Do not use for expected code or test failures without infrastructure evidence.
---

# Troubleshoot Environment

Restore a verified working path without broadening the suspended task.

1. Suspend the original task. Capture the failed operation, output, environment
   boundary and whether activation followed one clear infrastructure failure or
   a second equivalent failure after one plausibly transient retry.
2. Load `TROUBLESHOOTING.local.md` when present and then
   `TROUBLESHOOTING.md`. Reuse an entry only when its stable signature and
   applicability match and its safe diagnostic reconfirms the recorded cause.
3. Classify the recovery as a durable repair, stable workaround or task-local
   bypass. Prefer a durable repair and never disguise an equivalent failed path
   as a workaround.
4. Preserve architecture, dependency, test, input, material and temporary-data
   boundaries. Ask before privilege, installation, credentials, sensitive
   access, external transmission, global configuration, security relaxation,
   destructive recovery or another protected action. Existing project-local
   tool and environment choices take precedence.
5. Apply only the authorized recovery, then rerun the originally failing
   operation through its normal path. Recheck any security or trust assumption
   changed by the recovery.
6. Resume the original task only after verification. Otherwise leave it paused
   and record the evidence, requested authority and smallest next step.
7. Record only portable sanitized patterns in `TROUBLESHOOTING.md`. Put machine
   identifiers, absolute paths and host-specific facts in ignored
   `TROUBLESHOOTING.local.md`. Include signature, applicability, cause, safe
   diagnostic, durable repair, bounded workaround, authorization needs,
   verification and last confirmed date. Never record secrets.
