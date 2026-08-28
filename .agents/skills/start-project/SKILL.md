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
2. Establish the access boundary before inspecting external material. Ask only
   unanswered fundamentals in one initial set of no more than six numbered,
   coherent questions: project identity and purpose; intended audience and use;
   first useful outcome and minimum success evidence; current scope and
   non-goals; source, material or data access and sensitivity; and only those
   operating constraints that must be fixed now. Explain unfamiliar terms,
   accept explicit deferral of nonessential choices and do not hide a longer
   questionnaire in nested subparts. Never infer access, versioning,
   transmission or publication authority from a default or another answer.
3. After the maintainer answers, apply safe repository and domain defaults to
   nonessential undecided details and update the project-specific context and
   documentation named by `PROJECT_SETUP.md`. Record initialization status and
   date, source-template version and commit, synchronization baseline and
   intentional deviations.
4. Establish local input, temporary, material and output handling only as the
   repository guidance authorizes. Do not inspect, move, transmit or version a
   file merely because it exists.
5. Adapt `AGENTS.md` only for concrete commands, layout or validation
   differences. Retain `PROJECT_SETUP.md` and domain setup documents as the
   initialization method; no separate initialization prompt is retained.
6. After successful normal-project initialization, replace the inherited
   source-template maintenance history in `CHANGELOG.md` with a project-owned
   `Unreleased` changelog and replace `TASK_HANDOFF.md` with a project-owned
   initialization handoff. Record source-template lineage only in
   `PROJECT_CONTEXT.md` and retained setup documentation. Remove the inherited
   source-template `IDEAS.md`, the `create-local-project` skill and their
   template-only references. Retain `IDEAS.md` only when the maintainer
   deliberately establishes a project-local backlog. Do not rewrite an
   existing active derived project through initialization cleanup, and do not
   remove `create-secure-project` from a Secure AI control plane. If setup is
   incomplete, leave every reset and cleanup pending and report it.
7. Run proportionate local validation and report changes, checks, limitations,
   remaining maintainer decisions and suitable commit metadata.

Do not recreate the repository, configure a remote, create concrete Decision
Records in a regular source template or perform protected Git actions unless
the specific action is separately authorized.
