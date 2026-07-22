# Changelog

All notable changes to this project will be documented in this file.

This project follows Semantic Versioning.

## [Unreleased]

### Added

- Add an inventory-based workflow for external files and sources with
  `intake`, `restricted`, `local` and `versioned` input zones.
- Add `AGENTS.md` as the concise, automatically loaded entry point that routes
  AI agents to the complete engineering rules and validation guidance.

### Changed

- Replace abstract artifact terminology in active guidance with clearer terms
  for files, records, inputs, outputs and deliverables.
- Align the initialization and continuation prompts with `AGENTS.md`: setup is
  an explicit one-time workflow, while continuation only reconstructs state.
- Expand continuous-improvement guidance with engineering evidence,
  candidate review and transparent, unlinked private Templateverse governance.

## [v1.3.0] - 2026-07-20

### Changed

- Clarify `INITIAL_PROMPT.md` as the sole maintainer entry point for agent-led
  initialization, separate language navigation from the collaboration note,
  move README authority guidance into documentation rules and link maintainer
  tools to their official sources.
- Standardize template README badges as status, version and license links and
  document how derived projects adapt badges without inheriting template state
  or advertising nonexistent automation.
- Upgrade the Collaboration Model to v1.19 and classify staging and unstaging
  as specifically requested index operations outside the control-word rule.

## [v1.2.0] - 2026-07-19

### Added

- Add `RETROSPECTIVE_PROMPT.md` for evidence-based development-collaboration
  review and controlled template-learning candidates.
- Add `HARMONIZATION_PROMPT.md` for source-template comparison, development
  consistency review and roadmap alignment.
- Add `CONTINUATION_PROMPT.md` for reproducible development-project re-entry in
  a new context window or assistant session.
- Add `INITIAL_PROMPT.md` as a reproducible first-session prompt for derived project initialization.
- Add an AGIT Templateverse section to the English and German READMEs.
- Add `decisions/` as the shared Decision Record location with ADR, PDR and DDR templates.

### Changed

- Retain initialization artifacts as project provenance, record template
  lineage and harmonization baselines in `PROJECT_CONTEXT.md`, and clarify that
  documentation and repository guidance remain active project rules.
- Align the collaboration-model version in `PROJECT_CONTEXT.md` with the
  current template baseline.
- Separate assistant access, Git versioning and publication approval for
  sensitive development inputs, fixtures and generated artifacts.
- Extend disclosure review to generated artifacts and define automated checks
  as warnings rather than safety approval.
- Add a standard numbered checkpoint handoff for implementation steps.
- Upgrade the Collaboration Model to v1.18.
- Formalize human code readership and require clear English comments and code
  documentation for assistant-authored implementation when English is the
  repository standard.
- Strengthen the regular-commit rhythm below milestones and clarify that
  milestone commits close already recorded work.
- Strengthen safeguards against adding sensitive raw development inputs to Git.
- Define completion criteria for structured development-project initialization.
- Prefer concise numbered maintainer decisions and next steps.
- Require recognized Git history control words before an assistant may perform Git history actions.
- Clarify the AI Collaboration Note with an explicit sentence about documented engineering practices, AI-assisted workflows and repository conventions.
- Strengthen setup guidance so derived projects preserve a concrete, project-specific AI Collaboration Note linked to `ChatGPT.md`.
- Add guidance for sensitive local input handling, sanitized fixtures, generated artifacts and review checks based on access-plan project retrospection.
- Expand ADR checkpoint guidance for sensitive-input, fixture-versioning and generated-artifact decisions.
- Clarify that development projects may use PDRs and DDRs alongside ADRs when the decision subject calls for them.
- Clarify that project context should be refreshed after milestone commits or tags when pre-commit status remains documented.
- Clarify that template-only setup files may be removed or retained after initialization depending on project needs.
- Clarify that retained initialization files should keep their original names and may document setup status internally or in `PROJECT_CONTEXT.md`.
- Clarify that regular working commits must use Conventional Commit prefixes while milestone commits should omit prefixes and include the completed version number.

## [v1.1.2] - 2026-07-02

### Changed

- Upgrade the Collaboration Model to v1.16.
- Clarify that Git history actions are maintainer-controlled and forbidden for
  assistants by default.
- Harmonize `ChatGPT.md`, `REPOSITORY.md` and `CODEX.md` around explicit
  maintainer authorization for staging, commits, tags, pushes and other Git
  history actions.
- Bump template version to 1.1.2.

## [v1.1.1] - 2026-07-02

### Changed

- Reposition this repository as the AGIT Dev Template.
- Clarify that the AGIT Dev Template is the development-oriented specialization of the generic AGIT Project Template.
- Update README badges, version metadata and setup guidance for the `agit-dev-template` repository identity.
- Upgrade the Collaboration Model to v1.13.
- Add maintainer-owned project intent and desired end state as an explicit project-start step before roadmap derivation.
- Update project setup, project context and documentation guidance so initial roadmaps are derived from project context and target state.
- Upgrade the Collaboration Model to v1.14.
- Add dedicated documentation guidance for substantial modules, integrations and workflows.
- Clarify that substantial production components should include a demonstration, example configuration or validation path when applicable.
- Add a documentation freshness pass before milestone commits.
- Upgrade the Collaboration Model to v1.15.
- Add explicit ADR checkpoint guidance for important architecture, configuration-format, lifecycle, deployment and security decisions.
- Bump template version to 1.1.1.

## [v1.1.0] - 2026-06-28

### Changed

- Upgrade the Collaboration Model to v1.12.
- Add explicit user-facing documentation guidance for setup, configuration, productive usage, references and troubleshooting.
- Upgrade the Collaboration Model to v1.11.
- Add explicit code documentation and maintainability guidance for assistant-written implementation work.
- Upgrade the Collaboration Model to v1.10.
- Add explicit initial roadmap agreement guidance for new projects and substantially new phases.
- Upgrade the Collaboration Model to v1.9.
- Add milestone work rhythm and validation partnership guidance based on the BootProfile Switcher v0.4.0 through v0.7.0 workflow.
- Clarify that commit recommendations should include both a summary and a description.
- Update repository, setup, documentation, project-context and philosophy guidance to preserve the efficient validated collaboration pattern.
- Upgrade the Collaboration Model to v1.8.
- Add numbered maintainer next steps as the preferred handoff format when a change is approaching commit readiness.
- Upgrade the Collaboration Model to v1.7.
- Add Context Handoff Discipline for updating `PROJECT_CONTEXT.md` before context exhaustion becomes likely.
- Clarify that derived projects should preserve the AI Collaboration Note's purpose, placement and visibility while adapting project-specific wording when literal template text would be inaccurate.
- Harmonize README workflow summaries with roadmap-first development and documentation expectations.
- Bump template version to 1.1.0.

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
