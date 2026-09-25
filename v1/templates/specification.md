# Specification

## 1. Engineering Unit

**Unit:** [Stable project-local unit name / key]

**Parent Intent:** [Intent reference]

**Requirements:** [REQ / SEC / QLT references]

**Scope:** [Brief description of the unit's scope]

---

## 2. Context

### Problem

[Describe the problem or opportunity.]

### Objective

[Describe what the change is intended to achieve.]

### Stakeholders

[List relevant stakeholders, users, systems, or teams.]

---

## 3. Scope

### In Scope

- [Item]
- [Item]

### Out of Scope

- [Item]
- [Item]

Explicitly defining out-of-scope behavior helps prevent unintended scope
expansion.

---

## 4. Actors

| Actor | Role / Responsibility |
| --- | --- |
| [Actor] | [Description] |

---

## 5. User Stories

### Story 1

**As a** [actor]

**I want** [capability]

**So that** [value / outcome]

---

## 6. Functional Requirements

### REQ-001 — [Requirement title]

#### Requirement

[Describe the required behavior.]

#### Priority

[Must / Should / Could]

#### Rationale

[Why the requirement exists.]

---

## 7. Quality Requirements

Identify relevant quality requirements.

Examples:

- performance;
- reliability;
- security;
- maintainability;
- compatibility;
- interaction capability;
- flexibility;
- safety.

### QLT-001 — [Quality requirement]

#### Requirement

[Describe the expected measurable or verifiable quality.]

#### Verification

[How the requirement will be verified.]

---

## 8. Security Requirements

### SEC-001 — [Security requirement]

#### Requirement

[Describe the required security behavior or constraint.]

#### Verification

[How it will be verified.]

---

## 9. Constraints

List constraints that affect the solution.

Examples:

- regulatory;
- contractual;
- architectural;
- technology;
- compatibility;
- operational;
- budget;
- schedule.

---

## 10. Dependencies

Identify dependencies that may affect implementation or acceptance.

Examples:

- external systems;
- APIs;
- teams;
- data;
- infrastructure;
- third-party services.

---

## 11. Assumptions

List assumptions that materially affect the specification.

Each assumption should be validated when necessary.

| ID | Assumption | Validation |
| --- | --- | --- |
| ASM-001 | [Assumption] | [How / when validated] |

---

## 12. Acceptance Criteria

Acceptance criteria must describe observable and verifiable outcomes.

### ACC-001 — [Criterion]

#### Given

[Initial context]

#### When

[Action or event]

#### Then

[Expected outcome]

Additional scenarios should be added for relevant alternatives, errors,
boundaries, permissions, and security behavior.

---

## 13. Business Rules

### BUS-001 — [Rule]

[Describe the rule.]

---

## 14. Error and Exceptional Behavior

Define expected behavior for relevant failure conditions.

Examples:

- invalid input;
- unauthorized access;
- unavailable dependency;
- conflicting state;
- timeout;
- duplicate request;
- partial failure.

---

## 15. Data Requirements

Identify relevant data requirements.

Consider:

- inputs;
- outputs;
- validation;
- persistence;
- retention;
- privacy;
- auditability;
- migration.

---

## 16. Observability Requirements

When applicable, define:

- logs;
- metrics;
- traces;
- audit events;
- alerts;
- diagnostic information.

---

## 17. Traceability

**Engineering Unit:** [Unit name / key]

**Parent Intent:** [Intent reference]

Where required, maintain relationships between:

Intent → Requirements → Acceptance Criteria → Plan → Tasks → Implementation →
Tests → Evidence

Requirement identifiers should remain stable enough to support impact analysis.

---

## 18. Open Questions

Record unresolved questions here.

| ID | Question | Owner | Status |
| --- | --- | --- | --- |
| QST-001 | [Question] | [Owner] | Open |

Open questions that materially affect implementation should be resolved before
the relevant implementation decision.

---

## 19. Clarifications

Record decisions resulting from clarification.

| ID | Question / Ambiguity | Resolution | Date |
| --- | --- | --- | --- |
| CLR-001 | [Issue] | [Resolution] | [Date] |

---

## 20. Change History

| Version | Date | Change | Author |
| --- | --- | --- | --- |
| 0.1 | [Date] | Initial specification | [Author] |

---

## 21. Specification Status

**Status:** [Draft / Ready / Approved / Superseded]

**Version:** [Version]

**Owner:** [Owner]

**Last updated:** [Date]

---

## 22. Quality Gate

Before the specification is considered ready for planning, verify that:

- scope is explicit;
- requirements are understandable;
- relevant actors are identified;
- acceptance criteria are verifiable;
- quality requirements are considered;
- security requirements are considered;
- constraints are identified;
- dependencies are identified;
- assumptions are visible;
- unresolved material questions are addressed;
- requirements do not silently prescribe unnecessary implementation details.

---

## 23. Ptilon Workflow

The specification is part of the canonical Ptilon lifecycle:

```text
Intent
  ↓
Requirements
  ↓
Specification
  ↓
Architecture & Design
  ↓
Plan
  ↓
Tasks
  ↓
Implementation
  ↓
Verification
  ↓
Convergence
  ↓
Release
```

Clarification, checklists, analysis, and reviews are cross-cutting activities
or gates performed at the relevant points in this lifecycle.

The specification remains the primary source of intended product behavior
within its scope and must remain traceable to the approved upstream intent and
requirements.
