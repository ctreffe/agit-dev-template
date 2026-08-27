# Environment Troubleshooting

This conditionally loaded registry stores portable environment failures whose
cause and recovery have been verified. Read it only after the resident trigger
pauses a task. Host-specific facts belong in ignored
`TROUBLESHOOTING.local.md`; secrets do not belong in either file.

Reuse an entry only when both its stable signature and applicability match and
its diagnostic reconfirms the cause. Otherwise diagnose anew. A recorded repair
or workaround does not grant protected authority.

## Entry Schema

Every entry records:

- **Stable signature:** Output and execution stage that distinguish the issue.
- **Applicability:** Platforms, runners, repositories or prerequisites in scope.
- **Cause:** The verified root cause, not a symptom or guess.
- **Safe diagnostic:** Bounded read-only evidence that confirms or rejects it.
- **Durable repair:** The preferred recovery and its security boundary.
- **Bounded workaround:** A stable narrower path, or `None verified`.
- **Authorization needs:** Every approval or control-word requirement.
- **Verification:** The normal operation that must succeed before resumption.
- **Last confirmed:** ISO date and sanitized evidence scope.

## Known Issues

No portable verified issues are recorded yet.
