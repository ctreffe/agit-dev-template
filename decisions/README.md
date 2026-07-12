# Decision Records

This directory is the default location for durable decision records in development-oriented AGIT projects.

Use the record type that matches the decision:

- `ADR` - Architecture Decision Record for architecture, implementation structure, configuration formats, lifecycle behavior, deployment, security, tooling, fixtures or generated-artifact decisions.
- `PDR` - Project Decision Record for scope, roadmap, collaboration, privacy, repository structure, release model or governance decisions.
- `DDR` - Documentation Decision Record for user-facing documentation, reference structure, terminology, examples, screenshots or documentation QA decisions.

Development projects often use ADRs, but they may legitimately contain PDRs and DDRs as well. Choose the prefix by decision subject, not by repository type.

## Naming

Use a stable prefix, number and short kebab-case title:

```text
ADR-0001-configuration-format.md
PDR-0001-project-scope.md
DDR-0001-user-guide-structure.md
```

## Templates

Use the matching template as a starting point:

- [ADR-0000-template.md](ADR-0000-template.md)
- [PDR-0000-template.md](PDR-0000-template.md)
- [DDR-0000-template.md](DDR-0000-template.md)
