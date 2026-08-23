---
name: start-project
description: Initialize an uninitialized working repository from its retained setup contract. Use once, explicitly, and never to reinitialize a source-template maintenance checkout or active project.
---

# Start Project

Verify that this is an uninitialized working repository created from a source
template, not a source-template maintenance checkout or an active project. In
the Secure AI Template this may be a fresh local control-plane clone.

1. Apply `AGENTS.md`, then read `PROJECT_SETUP.md` and only the setup,
   privacy, domain and repository guidance it directly requires. Inspect Git
   read-only and preserve all existing work.
2. Establish the access boundary before inspecting external material. Ask for
   the maintainer-owned identity, intent, scope, audience, non-goals, storage,
   validation, roadmap and collaboration decisions required by the local setup
   contract. Do not invent or accept those decisions.
3. After the maintainer answers, update the project-specific context and
   documentation named by `PROJECT_SETUP.md`. Record initialization status and
   date, source-template version and commit, synchronization baseline and
   intentional deviations.
4. Establish local input, temporary, material and output handling only as the
   repository guidance authorizes. Do not inspect, move, transmit or version a
   file merely because it exists.
5. Adapt `AGENTS.md` only for concrete commands, layout or validation
   differences. Retain `PROJECT_SETUP.md` and domain setup documents as the
   initialization method; no separate initialization prompt is retained.
6. After successful normal-project initialization, remove the inherited
   `create-local-project` skill and its template-only references. Do not remove
   `create-secure-project` from a Secure AI control plane. If setup is
   incomplete, leave cleanup pending and report it.
7. Run proportionate local validation and report changes, checks, limitations,
   remaining maintainer decisions and suitable commit metadata.

Do not recreate the repository, configure a remote, create concrete Decision
Records in a regular source template or perform protected Git actions unless
the specific action is separately authorized.
