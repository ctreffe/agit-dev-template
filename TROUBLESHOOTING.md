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

No portable verified issues are recorded yet.
