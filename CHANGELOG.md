# Changelog

All notable changes to Ptilon are documented in this file.

## [1.2.1] - 2026-09-25

### Added

- Made human validation an explicit default progression gate between lifecycle
  activities.
- Defined the status of downstream drafts generated before upstream approval as
  provisional and non-authoritative.
- Defined a blocking rule for material unresolved questions discovered at a
  downstream activity: resolve the question, update and approve the authoritative
  source, then revalidate affected downstream artifacts before continuing.

### Changed

- Clarified the distinction between generating downstream proposals for analysis
  and advancing the lifecycle using approved authoritative artifacts.
- Strengthened the workflow and methodology guidance so `Implementation Ready`
  requires the applicable human approval gates to have been passed.

## [1.2.0] - 2026-09-25

### Added

- Defined controlled feedback from any lifecycle activity back to authoritative
  artifacts through `QST` questions and `CLR` clarification records.
- Distinguished clarification from material change and formalized `CHG` impact
  analysis for changes to approved intent.
- Defined `Implementation Ready` as a quality state with explicit readiness
  criteria before coding.
- Added reusable Architecture, Plan, Verification, and Clarification templates.
- Expanded the User Profile API example with plan, verification, and a
  downstream-discovered clarification scenario.

### Changed

- Strengthened the canonical lifecycle to explicitly support iterative and
  recursive evolution without creating additional lifecycle stages.
- Strengthened task requirements so tasks must be actionable and independently
  verifiable rather than merely present.
- Clarified that affected downstream artifacts remain not revalidated until
  impact assessment and required revisions are complete.
- Updated standards references to current published editions where applicable,
  including ISO/IEC/IEEE 12207:2026 and ISO/IEC/IEEE 42010:2022.
- Updated the Spec Kit reference to its current clarification, checklist,
  analysis, implementation, and convergence workflow.

## [1.1.0] - 2026-09-25

### Added

- Introduced engineering units as a decomposition mechanism for large or
  heterogeneous requirements and specifications.
- Defined requirements and specifications as the primary artifacts that may be
  decomposed into engineering units.
- Defined Architecture, Plan, Tasks, Verification, and related downstream
  artifacts as shared by default and updated according to impact rather than
  duplicated automatically for each unit.
- Added explicit impact analysis rules for changes to engineering units.
- Generalized the previous Large Features guidance into a reusable decomposition
  model.
- Updated templates, prompts, workflow documentation, and the User Profile API
  example to demonstrate the model.

### Changed

- Clarified that engineering units are project-local organizational scopes,
  not lifecycle stages, canonical artifact types, architectural modules, or new
  identifier prefixes.
- Clarified that the canonical lifecycle remains unchanged.
- Clarified traceability across engineering units and shared downstream
  artifacts.

## [1.0.1] - 2026-09-24

### Added

- Added a reusable Intent template for establishing project or change intent
  before downstream engineering artifacts.
- Clarified that Clarification is a cross-cutting activity rather than a
  lifecycle stage.
- Clarified that clarification output is non-authoritative until an authorized
  human resolution is incorporated into the applicable authoritative artifact.
- Updated the Specification template and documentation references to remain
  aligned with the canonical lifecycle.

## [1.0.0] - 2026-09-24

### Added

- Established the Ptilon software engineering methodology.
- Defined the canonical Ptilon development lifecycle:
  `Intent → Requirements → Specification → Architecture & Design → Plan →
  Tasks → Implementation → Verification → Convergence → Release`.
- Defined the Ptilon core principle of explicit intent, traceability, and
  verification.
- Established the upstream-authority model for engineering artifacts.
- Defined the canonical identifier taxonomy for requirements, acceptance
  criteria, security, quality, tasks, tests, decisions, changes, threats,
  mitigations, assumptions, questions, clarifications, and prompts.
- Defined human and AI responsibilities throughout the engineering lifecycle.
- Established Ptilon Core and Ptilon Governed usage models.
- Added reusable AI-assisted engineering prompts.
- Added reusable engineering templates.
- Added methodology, workflow, governance, quality, security, and standards
  documentation.
- Added a complete User Profile API example with requirements, architecture,
  tasks, tests, threat modeling, API contract, and traceability artifacts.
- Added references to relevant software engineering standards and practices.
- Added MkDocs-based documentation published through GitHub Pages.
- Added repository quality, documentation-link, and documentation-site
  automation.

## Versioning

Ptilon follows semantic versioning for methodology releases.

Material changes to lifecycle behavior, engineering controls, or reusable
artifacts are recorded in this changelog.
