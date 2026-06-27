# Changelog

All notable changes to this project will be documented in this file.

This project follows Semantic Versioning.

## [Unreleased]

### Changed

- Clarify that derived projects should preserve the AI Collaboration Note's purpose, placement and visibility while adapting project-specific wording when literal template text would be inaccurate.

## [v1.0.9] - 2026-06-27

### Changed

- Upgrade the Collaboration Model to v1.6.
- Generalize repository-ready delivery beyond browser-based ZIP workflows.
- Clarify that local working tree changes, patches, explicit file contents or archives may be valid delivery forms depending on the assistant environment.
- Add local repository working trees as accepted repository baselines when accessible to the assistant.
- Bump template version to 1.0.9.

## [v1.0.8] - 2026-06-27

### Added

- Add `CODEX.md` as the local Codex operating policy for AGIT repositories.
- Document allowed, approval-required and forbidden local Codex actions.
- Document read-only Git usage, local tool environments and internet/data disclosure rules.
- Add ignore rules for local Codex inputs, caches, generated artifacts and project-local tool environments.

### Changed

- Update template documentation to distinguish the general Collaboration Model from local Codex execution rules.
- Update setup and repository guidance to reference `CODEX.md`.
- Bump template version to 1.0.8.

## [v1.0.7] - 2026-06-27

### Changed

- Upgrade the Collaboration Model to v1.5.
- Add Integrity over Helpfulness, Artifact Integrity and Capability Transparency as explicit collaboration rules.
- Clarify that repository-ready artifacts must actually exist before they are reported as complete.
- Require derived projects to preserve the original AI Collaboration Note in README files directly below the badges.
- Update setup, documentation, repository and project-context guidance to treat the AI Collaboration Note as a required standardized template artifact.
- Bump template version to 1.0.7.

## [v1.0.6] - 2026-06-27

### Changed

- Upgrade the Collaboration Model to v1.4 after the BootProfile Switcher v0.3.0 retrospective.
- Harmonize repository-first collaboration, roadmap-first implementation, validated learning and repository-ready delivery across the template documentation.
- Clarify the distinction between feature commits and milestone commits.
- Refine documentation standards so retrospective updates are integrated across affected documents instead of appended as isolated notes.
- Update README files, project setup guidance, repository standards and project context guidance to reflect the improved workflow.
- Bump template version to 1.0.6.

## [v1.0.5] - 2026-06-27

### Added

- Introduce `PROJECT_CONTEXT.md` as the primary entry point for resuming AGIT projects.
- Add guidance for documenting the current project state independently from chat history.

### Changed

- Update README files, documentation standards and project setup guidance to include `PROJECT_CONTEXT.md`.
- Bump template version to 1.0.5.

## [v1.0.4] - 2026-06-27

### Added

- Introduce the Completion Integrity principle to the Collaboration Model.

### Changed

- Bump template version to 1.0.4.

## [v1.0.3] - 2026-06-27

### Added

- Document retrospective-driven evolution of the AGIT Project Template.
- Clarify that practical project experience is the basis for template improvements.
- Record the first retrospective-driven refinement cycle after applying the template in a real project.

### Changed

- Update project version metadata to 1.0.3.
- Extend the project philosophy with experience-driven template evolution.

## [v1.0.2] - 2026-06-26

### Changed

- Clarify the versioning philosophy by distinguishing repository version tags from GitHub Releases.
- Document that not every version tag requires a GitHub Release.

## [v1.0.1] - 2026-06-26

### Changed

- Use the latest Git tag instead of the latest GitHub Release for the version badge in the English and German README files.

## [v1.0.0] - 2026-06-26

### Changed

- Refine the English and German README files into concise user-facing entry points.
- Clarify the role of template-only documents and documents that usually remain in derived projects.
- Refine `DOCUMENTATION.md` and `REPOSITORY.md` wording for the AGIT Project Template.
- Add guidance to remove template-only setup files in a dedicated commit.
- Update project version metadata to 1.0.0.

## [v0.7.0] - 2026-06-26

### Added

- Extend `PHILOSOPHY.md` with a section describing versioning principles based on Semantic Versioning.

### Changed

- Update English and German README files.
- Update project version metadata to 0.7.0.

## [v0.6.0] - 2026-06-26

### Added

- Add `PROJECT_SETUP.md` as the initial setup guide for projects created from the template.
- Document the recommended setup workflow for derived repositories.
- Document which template-only files may be removed after project initialization.

### Changed

- Update English and German README files to reference `PROJECT_SETUP.md`.
- Update `DOCUMENTATION.md` and `REPOSITORY.md` to describe the role of setup-only documents in derived projects.
- Update project version metadata to 0.6.0.

## [v0.5.0] - 2026-06-26

### Added

- Add `REPOSITORY.md` as a core repository document.
- Document repository naming, descriptions, Git workflow, commit messages, version tags, releases and repository metadata.
- Document repository-ready delivery as a repository-level standard.

### Changed

- Update English and German README files to reference `REPOSITORY.md`.
- Update project version metadata to 0.5.0.

## [v0.4.0] - 2026-06-26

### Added

- Add `DOCUMENTATION.md` as a core repository document.
- Document the purpose and responsibility of the core project documents.
- Define guidance for user-facing documentation, engineering philosophy and collaboration documentation.

### Changed

- Update English and German README files to reference `DOCUMENTATION.md`.
- Update project version metadata to 0.4.0.

## [v0.3.0] - 2026-06-26

### Added

- Add `PHILOSOPHY.md` as a core repository document.
- Document the engineering philosophy shared by projects created from the AGIT Project Template.
- Define principles for simplicity, maintainability, transparency, documentation, pragmatism, quality and continuous evolution.

### Changed

- Update English and German README files to reference `PHILOSOPHY.md`.
- Update project version metadata to 0.3.0.

## [v0.2.0] - 2026-06-26

### Added

- Add `ChatGPT.md` with Collaboration Model v1.1.
- Introduce the AGIT Collaboration Model as a core repository document.
- Document repository-ready delivery and shared repository state requirements.
- Document Git workflow conventions for AGIT projects.
- Add historical note for the Collaboration Model.

### Changed

- Update English and German README files to reference the Collaboration Model.
- Update project version metadata to 0.2.0.
- Replace earlier "vision" wording with more precise project language.

## [v0.1.0] - 2026-06-26

### Added

- Establish initial repository foundation.
- Add English README.
- Add German README translation.
- Define the initial scope of the AGIT Project Template.
- Add initial project version metadata.
