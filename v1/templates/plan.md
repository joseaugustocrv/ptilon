# Implementation Plan Template

## 1. Purpose

Translate the approved specification and architecture into an executable,
dependency-aware implementation approach.

The Plan defines sequencing and strategy; it must not silently redefine
requirements or architectural decisions.

## 2. Plan Metadata

- **Plan:** [Reference]
- **Specification:** [Reference]
- **Architecture:** [Reference]
- **Engineering Units:** [Units]
- **Owner:** [Owner]
- **Status:** [Draft / Under Review / Approved / Superseded]
- **Version:** [Version]
- **Last updated:** [Date]

## 3. Scope

### In Scope

- [Scope]

### Out of Scope

- [Scope]

## 4. Work Breakdown

| Workstream | Objective | Source | Dependencies | Verification |
| --- | --- | --- | --- | --- |
| [Workstream] | [Objective] | [REQ / SPEC / ADR] | [Dependencies] | [Method] |

## 5. Sequencing

Describe phases, dependencies, parallel work, milestones, and integration
points.

```text
[Workstream A]
      ↓
[Workstream B] ──→ [Integration]
      ↓                 ↓
[Workstream C] ─────────┘
```

## 6. Technical Strategy

Describe implementation strategy, migration approach, compatibility strategy,
configuration, infrastructure, and rollout constraints as applicable.

## 7. Verification Strategy

Define the verification approach for functional behavior, quality,
security, integration, migration, and regression risks.

## 8. Risks, Assumptions, and Dependencies

Identify blockers and assumptions that must be resolved before affected tasks
can proceed.

Material unresolved questions must be recorded as `QST-###`.

## 9. Task Generation Rules

Tasks generated from this Plan must:

- identify an explicit source;
- be actionable;
- identify dependencies;
- have a verifiable completion signal;
- avoid introducing undocumented requirements;
- identify affected files/components when that information is known;
- expose blockers rather than hiding them as assumptions.

## 10. Implementation Readiness

The Plan is ready for task generation only when:

- specification and architecture are approved;
- material questions are resolved;
- dependencies are sufficiently understood;
- sequencing is coherent;
- verification strategy is defined;
- no architectural or requirement decision is being invented by the task
  generator.

## 11. Traceability

```text
Requirement → Specification → Architecture / ADR → Plan → Task → Test
```
