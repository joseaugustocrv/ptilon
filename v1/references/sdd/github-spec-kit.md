# GitHub Spec Kit — Ptilon Reference

## 1. Purpose

Document how GitHub Spec Kit is used as the primary operational reference for
Specification-Driven Development (SDD) within Ptilon.

This document describes the relationship between Spec Kit and Ptilon. It does
not reproduce Spec Kit documentation.

---

## 2. Reference

GitHub Spec Kit

Official repository: <https://github.com/github/spec-kit>

Official documentation: <https://github.github.com/spec-kit/>

Spec Kit provides structured workflows that keep intent and evidence ahead of
implementation.

---

## 3. Role in Ptilon

Ptilon uses Spec Kit as its primary operational reference for SDD.

The distinction is:

**External engineering standards → Ptilon methodology → Spec Kit workflow →
Project artifacts → Implementation evidence**

Ptilon provides the broader methodology, governance, quality, security, and
lifecycle context.

Spec Kit provides the concrete SDD mechanisms used to move from specification
to implementation and convergence.

Ptilon should complement Spec Kit rather than unnecessarily duplicate its
capabilities.

---

## 4. Core SDD flow

The current Spec Kit core flow is:

Specify → Plan → Tasks → Implement → Converge

For projects requiring additional quality controls, Spec Kit provides:

- **Constitution** — establish project principles;
- **Clarify** — resolve ambiguity before planning;
- **Checklist** — validate requirements quality;
- **Analyze** — check consistency across specification, plan, and tasks.

A project using Ptilon with Spec Kit may use the following tool-level sequence:

Constitution → Specify → Clarify → Plan → Checklist → Tasks → Analyze → Implement → Converge

This is a Spec Kit operational sequence, not the Ptilon lifecycle. The
Constitution is a project-governance artifact, and Clarify, Checklist, Analyze,
and Review are activities or gates mapped onto the applicable Ptilon lifecycle
points. After convergence, Ptilon applies the applicable release-readiness and
release controls; review remains cross-cutting rather than becoming a lifecycle
stage.

---

## 5. Command responsibilities

| Command | Primary responsibility |
| --- | --- |
| `/speckit.constitution` | Establish or update project principles |
| `/speckit.specify` | Define requirements, scope, and user stories |
| `/speckit.clarify` | Resolve ambiguity before planning |
| `/speckit.plan` | Define the technical implementation approach |
| `/speckit.checklist` | Generate requirements-quality checks |
| `/speckit.tasks` | Create dependency-ordered implementation tasks |
| `/speckit.analyze` | Detect conflicts, gaps, and inconsistencies |
| `/speckit.implement` | Execute the implementation tasks |
| `/speckit.converge` | Verify implementation against the governing artifacts |

The exact invocation syntax depends on the selected coding-agent integration.

---

## 6. Constitution

The constitution establishes project-level principles that govern subsequent
work. In Ptilon, this is a project governance artifact and is not a lifecycle
stage. It may be created or updated before feature-level specification when
the project adopts this governance mechanism.

Typical principles may address:

- architecture;
- security;
- testing;
- maintainability;
- coding standards;
- observability;
- documentation;
- compliance.

The constitution is a governing constraint rather than a feature
specification.

---

## 7. Specify

Specification focuses on **what** should be built and **why**.

The specification should establish:

- scope;
- intended behavior;
- actors;
- user stories;
- requirements;
- acceptance criteria;
- relevant constraints.

Implementation details should not be introduced prematurely unless they are
genuine requirements or constraints.

---

## 8. Clarify

Clarification resolves material ambiguity before technical planning.

Questions should target areas such as:

- behavior;
- boundaries;
- permissions;
- error conditions;
- acceptance criteria;
- dependencies;
- constraints;
- security;
- quality requirements.

When clarification reveals a requirement problem, the requirement should be
corrected at its source.

---

## 9. Plan

Planning is where technical implementation detail is introduced.

The plan may define:

- technology stack;
- architecture;
- components;
- interfaces;
- data structures;
- dependencies;
- technical constraints;
- implementation strategy.

The plan should remain consistent with the approved specification.

---

## 10. Checklist

The checklist acts as a requirements-quality gate.

It should help determine whether the specification is:

- complete;
- clear;
- consistent;
- testable;
- appropriately scoped;
- sufficiently precise.

Checklist items are quality-review criteria. They are not implementation tasks.

---

## 11. Tasks

Tasks translate the technical plan into actionable, dependency-ordered
implementation work.

Tasks should provide sufficient information for implementation without becoming
a substitute for the specification or plan.

Tasks should remain traceable to the artifacts that establish their intent.

---

## 12. Analyze

Analysis checks consistency across the principal artifacts.

At minimum, analysis should consider:

- specification;
- plan;
- tasks;
- constitution constraints.

When conflicts or gaps are identified, the responsible upstream artifact
should be corrected.

The Ptilon rule is:

> The artifact that owns the decision owns the correction.

---

## 13. Implement

Implementation executes the approved tasks.

AI may perform a significant portion of implementation work, but implementation
remains subject to:

- project constitution;
- specification;
- plan;
- tasks;
- quality requirements;
- security controls;
- applicable engineering standards.

Implementation should not silently redefine requirements.

---

## 14. Converge

Convergence compares the implemented codebase against the feature artifacts.

The purpose is to identify remaining gaps between:

- specification;
- plan;
- tasks;
- implementation.

If gaps remain, convergence adds traceable tasks for subsequent implementation.

The cycle is repeated:

Implement → Converge → Implement → Converge

until the feature is complete according to the governing artifacts.

---

## 15. Living specifications

Ptilon treats the specification as the source of truth for intended behavior.

When intended behavior changes:

1. update the specification first;
2. update or regenerate the plan;
3. update or regenerate tasks;
4. run consistency analysis;
5. implement the resulting changes;
6. converge again.

Derived artifacts must not silently become more authoritative than the
specification.

---

## 16. Existing projects

Spec Kit can also be adopted in established codebases.

When introducing SDD to an existing project, the existing system should be
understood before new specifications are created.

Relevant existing constraints may include:

- architecture;
- technology stack;
- dependencies;
- operational behavior;
- technical debt;
- security constraints;
- existing interfaces.

Ptilon governance and architecture practices remain applicable.

---

## 17. Large features

For features that exceed the practical context of a single SDD cycle, Spec Kit
supports decomposition into independently specified sub-features.

Ptilon treats this as a controlled decomposition:

Large Intent → Roadmap / Spec of Specs → Sub-specifications → Individual SDD
Cycles

Each sub-feature should retain clear dependencies and traceability to the
larger objective.

Decomposition should be used when simpler approaches are insufficient.

---

## 18. Bug fixing

Bug fixing is treated separately from normal feature development when the
primary objective is to diagnose and repair existing behavior.

The process should distinguish:

Diagnosis → Repair → Verification

The original symptom and expected behavior should remain explicit throughout
the process.

When the defect reveals a missing or incorrect requirement, the governing
specification should be corrected rather than merely patching implementation
behavior.

---

## 19. AI responsibility model

Spec Kit structures the artifacts and workflow, but it does not eliminate
human responsibility.

Humans remain responsible for:

- intent;
- requirements approval;
- ambiguity resolution;
- significant technical decisions;
- risk acceptance;
- review;
- release decisions.

AI may assist with:

- drafting;
- analysis;
- decomposition;
- implementation;
- testing;
- documentation;
- consistency checking;
- convergence analysis.

---

## 20. Ptilon integration

Ptilon adds controls around Spec Kit for:

- requirements engineering;
- architecture;
- quality;
- security;
- governance;
- traceability;
- evidence;
- release management;
- methodology evolution.

This creates the relationship:

Ptilon governs the engineering system; Spec Kit operationalizes SDD within
that system.

---

## 21. Current reference status

Spec Kit is an actively evolving project.

Ptilon should periodically review the official Spec Kit documentation for:

- command changes;
- workflow changes;
- new quality gates;
- new integrations;
- extensions;
- presets;
- workflow capabilities.

Ptilon should reference the current official behavior rather than relying
indefinitely on a historical command set.

---

## 22. References

- GitHub Spec Kit repository: <https://github.com/github/spec-kit>
- GitHub Spec Kit documentation: <https://github.github.com/spec-kit/>
- Agentic SDD reference:
  <https://github.github.com/spec-kit/reference/agentic-sdd.html>
- Ptilon Standards: `docs/standards/README.md`
- Ptilon Methodology: `docs/methodology/README.md`
- Ptilon Workflow: `docs/workflow/README.md`

---

## 23. Status

This document defines the role of GitHub Spec Kit as the primary operational
SDD reference within Ptilon.

It should be reviewed whenever the current Spec Kit workflow or architecture
changes materially.
