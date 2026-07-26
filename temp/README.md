# Temporary Working Files

`temp/` contains disposable intermediate engineering files. All contents
outside `restricted/` are assistant-readable. Everything under `temp/` is
local-only, ignored by Git and must never be versioned.

Use `restricted/` for temporary files that assistants must not enumerate or
read. Temporary files are not cataloged. Promote a durable file to
`materials/`, source, tests, fixtures or configuration as appropriate and
preserve its provenance.
