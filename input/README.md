# External Files and Sources

Use `input/` for externally supplied development files such as logs, dumps,
API responses, screenshots, exports and reproduction material. New or uncertain
files start in `intake/`; already classified files may go directly to
`restricted/`, `local/` or `versioned/`.

- `intake/` contains files not yet classified;
- `restricted/` contains ignored files unavailable to assistants;
- `local/` contains ignored files approved for assistant access;
- `versioned/` contains files deliberately approved for Git and assistant
  access.

Use `INVENTORY.md` for safe source metadata and handling decisions. Use the
ignored `INVENTORY.local.md` when filenames, paths or details are sensitive.
Assistant access, Git versioning and external sharing remain separate
maintainer decisions.

Some runtime files must remain at tool-defined paths, such as a root `.env` or
a local database. Document those exceptions in the inventory and protect them
with path-specific ignore rules instead of moving them merely for uniformity.
Files promoted into source, tests or configuration retain their recorded
provenance.
