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
3. Check tags, upstream state, release rules and documented milestone
   validation with bounded commands. Load additional authority only for a real
   conflict or gap.
4. Keep unstaged and untracked work outside the milestone and report it without
   inventorying unrelated contents.
5. Resolve only authorized closure gaps, rerun required validation and propose
   a human-readable versioned summary plus concise evidence-based body.
6. Create the commit only with action-specific authorization and verify it.

Push, tag creation, tag push and release publication remain separate protected
actions requiring their own authorization and post-action verification.
