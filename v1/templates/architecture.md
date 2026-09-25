# Architecture & Design Template

## 1. Purpose

Describe how the approved specification will be realized technically. The
architecture must explain significant structures, boundaries, interfaces,
constraints, quality concerns, security concerns, and decisions.

## 2. Architecture Metadata

- **Architecture ID / Reference:** [Reference]
- **Scope / Engineering Units:** [Units]
- **Specification:** [Reference]
- **Requirements:** [REQ / SEC / QLT references]
- **Status:** [Draft / Under Review / Approved / Superseded]
- **Version:** [Version]
- **Owner:** [Owner]
- **Last updated:** [Date]

## 3. Stakeholders and Concerns

| Stakeholder | Concern |
| --- | --- |
| [Stakeholder] | [Concern] |

## 4. System Context and Boundaries

Describe the system of interest, external actors, systems, dependencies, trust
boundaries, and major interfaces.

## 5. Architecture Views

### View 1 — [Name]

**Purpose:** [Concern addressed]

**Description:** [Architecture view]

## 6. Components and Responsibilities

| Component | Responsibility | Dependencies |
| --- | --- | --- |
| [Component] | [Responsibility] | [Dependencies] |

## 7. Interfaces and Contracts

Document relevant APIs, events, protocols, data contracts, integration
constraints, and compatibility expectations.

## 8. Data and State

Describe important entities, data flows, persistence, consistency, retention,
migration, privacy, and ownership considerations.

## 9. Quality and Security

Address applicable:

- performance and scalability;
- availability and reliability;
- maintainability;
- observability;
- compatibility;
- security and privacy;
- resilience and recovery.

Each material constraint should trace to a requirement or approved decision.

## 10. Architecture Decisions

List significant decisions and link to ADRs.

| Decision | ADR | Affected Requirements |
| --- | --- | --- |
| [Decision] | [ADR] | [REQ / SEC / QLT] |

## 11. Risks and Trade-offs

| Risk / Trade-off | Impact | Mitigation / Decision |
| --- | --- | --- |
| [Risk] | [Impact] | [Action] |

## 12. Dependencies and Assumptions

Record dependencies and assumptions that affect the architecture. Material
uncertainties must be raised as `QST-###` questions rather than silently
resolved.

## 13. Verification

Describe how architectural requirements and significant decisions will be
verified.

## 14. Traceability

Maintain, where applicable:

```text
Requirement → Architecture Element / ADR → Task → Test → Evidence
```

## 15. Quality Gate

Before approval, verify:

- relevant requirements are covered;
- boundaries and interfaces are explicit;
- quality and security constraints are addressed;
- significant decisions are recorded;
- dependencies and assumptions are visible;
- material open questions are resolved or explicitly accepted as non-blocking;
- the architecture is feasible within the stated constraints;
- downstream planning can be performed without inventing architectural
  decisions.
