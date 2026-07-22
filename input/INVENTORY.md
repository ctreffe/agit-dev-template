# External File and Source Inventory

Record only metadata that is suitable for Git versioning. Use neutral IDs when
filenames or source details are sensitive. Keep sensitive local details in
`INVENTORY.local.md`, which is ignored by Git.

| ID | Description | Origin or reference | Classification | Assistant access | Git versioning | External sharing | Notes |
| --- | --- | --- | --- | --- | --- | --- | --- |
| `<source-id>` | `<safe description>` | `<safe origin, URL or reference>` | `<intake | restricted | local | versioned>` | `<not approved | approved scope>` | `<no | yes>` | `<not approved | approved scope>` | `<provenance or handling notes>` |

An inventory entry documents a decision; it does not grant permission beyond
the recorded scope. Update it when a file moves or becomes maintained source,
test or configuration content elsewhere in the repository.
