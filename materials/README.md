# Project Materials

Synchronized external materials use provider-neutral `sync:` roots and storage
`external`; see [SYNCHRONIZED_STORAGE.md](../SYNCHRONIZED_STORAGE.md).

`materials/` contains retained working files created within the project or
derived by changing content from external files under `input/`. Every material
is approved for assistant access. Git versioning and external sharing remain
separate decisions.

Files under `input/` remain content-unchanged. Decompression, conversion,
redaction, cropping, annotation, normalization, combination or any other
content change creates a new material; preserve the original input and record
its ID under `Based on` in `CATALOG.md`.

The catalog records three storage states:

- `local`: stored under `materials/local/`, ignored by Git and assistant-readable;
- `versioned`: stored under `materials/versioned/` and approved for Git;
- `external`: stored outside the repository and represented by a stable
  logical location in `CATALOG.md`.

Copy `PATHS.local.example.md` to the ignored `PATHS.local.md` for
device-specific paths. Do not version credentials, private share tokens or
absolute local paths.

Examples include sanitized reproduction files, transformed exports, reviewed
screenshots and retained diagnostic extracts. Disposable build products,
caches and runtime files remain outside this component. A material promoted to
source, tests, fixtures or configuration keeps its cataloged provenance.
