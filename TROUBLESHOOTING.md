# Environment Troubleshooting

This registry belongs only to focused problem resolution. It stores portable
observed problems, confirmed causes, safe diagnostics and verified durable
repairs. It may retain an unresolved incident as an open task with the smallest
next diagnostic step. Do not read or update it after a quick exit. Host-specific
facts belong in ignored
`TROUBLESHOOTING.local.md`; secrets do not belong in either file.

Reuse an entry only when both its stable signature and applicability match and
its diagnostic reconfirms the cause. Otherwise diagnose anew. A recorded repair
does not grant protected authority.

## Entry Schema

Every entry records:

- **Stable signature:** Output and execution stage that distinguish the issue.
- **Applicability:** Platforms, runners, repositories or prerequisites in scope.
- **Cause:** The verified root cause, not a symptom or guess.
- **Safe diagnostic:** Bounded read-only evidence that confirms or rejects it.
- **Durable repair:** The preferred recovery and its security boundary.
- **Authorization needs:** Every approval or control-word requirement.
- **Verification:** The normal operation that must succeed before resumption.
- **Last confirmed:** ISO date and sanitized evidence scope.
- **Unresolved marker:** Only when no repair was verified; retain the problem as
  an open task and state the smallest next diagnostic step.

## Known Issues

## KI-0004: Context-sensitive patch application rejects a coordinated edit

- **Stable signature:** `apply_patch` rejects an edit with
  `verification failed: Failed to find expected lines` before reporting any
  changed file. A retry using freshly read exact context and smaller independent
  hunks succeeds.
- **Applicability:** Context-based repository patches, especially coordinated
  multi-file edits and line-wrapped Markdown where a generated hunk reconstructs
  or approximates surrounding text instead of copying the current target span.
  The same signature may follow a concurrent edit, different indentation or
  line wrapping; it is not by itself evidence of whitespace or line-ending
  damage.
  Dynamically assembled patch text can produce the same rejection when inserted
  lines lose their line-level operation markers.
- **Cause:** `apply_patch` verifies each hunk against exact current context. In
  the confirmed Governance incident, the failed hunk expected a shortened
  phrase at a line boundary that did not match the actual sentence. Because the
  combined patch was rejected as one operation, none of its otherwise valid
  hunks changed a file. The mismatch was generated patch context, not verified
  repository whitespace corruption.
  During the family rollout, one dynamically assembled insertion likewise lost
  its add-operation markers and was rejected atomically before changing a file.
- **Safe diagnostic:** Do not retry the same patch. Read only the bounded target
  span named in the failure, compare its exact wording and indentation with the
  rejected hunk, and inspect the affected repositories read-only to confirm
  whether any partial edit occurred. Distinguish stale or approximated context
  from malformed line-level operation markers and actual line-ending or
  whitespace evidence before selecting a repair.
- **Durable repair:** Before the first complex patch, read the exact target
  spans and build hunks around the smallest stable semantic anchors. Separate
  independent files or uncertain hunks so one context mismatch does not reject
  a broad coordinated edit. When assembling patch text dynamically, preserve an
  explicit operation marker on every hunk line. For repeated family changes,
  prove the hunk on one representative file, then apply the same verified shape
  to matching copies.
  After any rejection, verify atomicity and correct only the mismatched hunk;
  do not broaden the context or attribute the failure to whitespace by default.
- **Authorization needs:** Read-only context and state inspection need no new
  authority inside the active repository scope. Resulting edits retain all
  dependency, engineering, test, release and Git boundaries.
- **Verification:** On a natural coordinated multi-file edit, read the exact
  spans before constructing the first patch, apply the bounded hunks through
  the normal `apply_patch` path and inspect the resulting diff. Success
  requires first-attempt application with only the intended files changed; do
  not create a fix-specific fixture or substitute patch test.
- **Last confirmed:** 2026-09-06, coordinated Governance and six-source-template
  rollout. One normal multi-repository patch updated all seven freshly read
  `start-task` targets on its first attempt, and focused diffs showed only the
  intended skill changes. After the malformed generated insertion was diagnosed
  and rejected atomically, a later dynamically assembled seven-file handoff
  patch with explicit line markers also succeeded on its first attempt.
