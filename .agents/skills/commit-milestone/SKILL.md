---
name: commit-milestone
description: Close an already reviewed version or milestone with synchronized metadata, expanded validation and milestone-specific commit wording.
---

# Commit Milestone

Use only when the maintainer explicitly invokes `$commit-milestone` for an
identified milestone or version closure. This is not a substitute for
developing or reviewing the milestone.

1. Establish the exact repository, completed version or milestone, Git state
   and staged file list.
2. Inspect staged versions of relevant version, changelog, README, objective or
   roadmap and handoff files. Read a full staged patch or unrelated working-tree
   file only when an inconsistency requires it.
3. Classify the semantic scope. Reuse a current ordinary-commit full-gate result
   only when no governed input changed; otherwise run the repository's mandatory
   full validation gate. Add its expanded release, rendering, security, privacy
   or domain checks. Use bounded success output and retain failure diagnostics.
   Rerun every affected gate after a relevant correction.
4. Check tags, upstream state and release rules with bounded commands. Load
   additional authority only for a real conflict or gap.
5. Keep unstaged and untracked work outside the milestone and report it without
   inventorying unrelated contents.
6. Resolve only authorized closure gaps, rerun required validation and propose
   a human-readable versioned summary plus concise evidence-based body.
7. Create the commit only with action-specific authorization and verify it.

Push, tag creation, tag push and release publication remain separate protected
actions requiring their own authorization and post-action verification.
