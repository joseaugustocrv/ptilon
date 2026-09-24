# Ptilon Methodology

## 1. Purpose

Ptilon is a software engineering methodology for developing software with
systematic use of Artificial Intelligence.

It combines established Software Engineering practices with
Specification-Driven Development (SDD), using AI as an engineering
participant while preserving human accountability, traceability,
verification, security, and quality controls.

Ptilon is not intended to replace Agile, Scrum, Kanban, DevOps, or other
delivery approaches. It defines an engineering layer that can operate
within those approaches.

## 2. Design Goals

Ptilon is designed to make AI-assisted development:

- explicit;
- traceable;
- verifiable;
- repeatable;
- maintainable;
- secure;
- adaptable to different AI agents and technology stacks.

The methodology prioritizes reuse of established practices. A
Ptilon-specific mechanism should only be introduced when an existing
practice does not adequately address an identified need created or
amplified by AI-assisted development.

## 3. Canonical Model

The canonical concepts, lifecycle, identifier taxonomy, authority model, and
AI responsibility rules are defined in [`canonical-model.md`](canonical-model.md).
All other Ptilon documentation, templates, prompts, and examples must remain
consistent with that document.

## 4. Central Principle

> **Intent must be explicit before implementation, remain traceable during
> implementation, and be verified against the delivered software.**

The central engineering chain is:

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

Each downstream artifact should be derived from, or demonstrably related
to, the upstream intent.

## 5. Methodology Layers

Ptilon is organized into six complementary layers.

### 5.1 Governance

Defines the rules under which the project operates.

Includes:

- project principles;
- roles and responsibilities;
- human approval points;
- change control;
- risk management;
- AI usage rules;
- evidence requirements.

### 5.2 Requirements Engineering

Defines what the software must accomplish and the constraints under
which it must operate.

Includes:

- stakeholder needs;
- functional requirements;
- quality requirements;
- business rules;
- constraints;
- acceptance criteria;
- requirement validation;
- traceability.

### 5.3 Specification-Driven Development

Transforms validated intent into development artifacts that an AI coding
agent can use consistently.

Ptilon adopts GitHub Spec Kit as its primary operational reference for
this layer.

GitHub Spec Kit provides an operational SDD workflow that Ptilon maps onto its
own lifecycle. Its project Constitution mechanism is a governance artifact,
not a Ptilon lifecycle stage.

A typical Spec Kit feature flow is:

```text
Specify → Clarify → Plan → Checklist → Tasks → Analyze → Implement → Converge
```

The exact set and ordering of Spec Kit commands may evolve. Ptilon therefore
treats these mechanisms as tool-level activities and quality gates, not as an
alternative canonical lifecycle. Ptilon does not reproduce these mechanisms;
it defines when and why they are used within the broader engineering lifecycle.

### 5.4 Architecture and Design

Defines how the requirements and specification will be realized
technically.

Includes:

- architecture description;
- system boundaries;
- components;
- interfaces;
- data models;
- technology constraints;
- architectural decisions;
- quality attributes;
- security architecture.

Architecture decisions should be explicitly recorded when they have
meaningful consequences for the system.

### 5.5 Implementation and Verification

Transforms approved plans into working software and verifies the result.

Includes:

- dependency-ordered implementation tasks;
- code generation or modification;
- automated tests;
- integration tests;
- static analysis;
- security checks;
- acceptance verification;
- code review;
- convergence analysis.

### 5.6 Evolution

Software and its specifications are living artifacts.

When intended behavior changes:

```text
Change in intent
      ↓
Update requirement / specification
      ↓
Revalidate
      ↓
Update architecture / plan
      ↓
Regenerate or update tasks
      ↓
Analyze consistency
      ↓
Implement
      ↓
Verify
      ↓
Converge
```

The specification must not silently become obsolete while implementation
evolves.

## 6. Quality Gates

Ptilon introduces quality gates at points where defects are
comparatively inexpensive to detect.

### Gate 1 — Intent

Verify that the problem and desired outcome are understood.

### Gate 2 — Requirements

Verify that requirements are sufficiently complete, consistent,
unambiguous, feasible, and verifiable.

### Gate 3 — Specification

Verify that the specification represents the intended behavior and
contains testable acceptance criteria.

### Gate 4 — Architecture

Verify that the proposed design satisfies requirements and relevant
quality and security constraints.

### Gate 5 — Pre-Implementation

Verify consistency between specification, plan, and tasks.

This is where Spec Kit's checklist and analyze capabilities are
particularly useful.

### Gate 6 — Implementation

Verify code quality, tests, security controls, and adherence to the
approved artifacts.

### Gate 7 — Convergence

Verify the implemented system against the specification, plan, and
tasks.

Spec Kit's `/speckit.converge` provides this mechanism for SDD features
and can append remaining work to the task list when gaps are found.

### Gate 8 — Release

Verify that release criteria, required evidence, security controls,
tests, and approvals are satisfied.

## 7. Human and AI Responsibilities

Ptilon does not treat AI output as inherently authoritative.

### AI may

- generate candidate requirements;
- identify ambiguities;
- produce specifications;
- propose designs;
- generate implementation plans;
- generate or modify code;
- generate tests;
- analyze consistency;
- identify defects;
- generate documentation.

### Humans must retain responsibility for

- business intent;
- domain decisions;
- acceptance of requirements;
- architectural decisions;
- risk acceptance;
- security risk acceptance;
- exceptions to mandatory controls;
- final release approval.

The exact approval model may vary according to project risk and
organizational governance.

## 8. Authority and AI Responsibility

Ptilon follows the upstream-authority model defined in [`canonical-model.md`](canonical-model.md):

- downstream artifacts refine upstream intent;
- conflicts must be surfaced rather than silently resolved by AI;
- AI-generated requirements, security requirements, quality requirements,
  decisions, evidence, and approvals remain proposals until appropriately
  approved;
- missing information must be surfaced rather than invented.

Reviews are cross-cutting activities, not an additional lifecycle stage.

## 9. Traceability

Ptilon uses traceability as a primary quality mechanism.

A feature should be traceable through:

```text
Requirement ID
    ↓
Specification
    ↓
Acceptance Criterion
    ↓
Design / ADR
    ↓
Task
    ↓
Implementation
    ↓
Test
    ↓
Verification Evidence
```

Traceability does not require every line of code to map to a
requirement. It requires that significant intended behavior and
important engineering decisions can be followed through the relevant
artifacts.

## 10. Quality Model

Ptilon uses established software quality models rather than inventing a
proprietary definition of quality.

The methodology uses ISO/IEC 25010 as a principal reference for
product quality and will translate relevant quality characteristics into
measurable requirements, acceptance criteria, tests, controls, and
release evidence.

## 11. Security

Security is integrated into the lifecycle.

Security activities may include:

- security requirements;
- threat modeling;
- secure architecture decisions;
- dependency analysis;
- secure coding controls;
- automated security testing;
- vulnerability management;
- security verification;
- release controls.

The depth of these activities must be proportional to project risk.

## 12. Change Management

Changes to intended behavior must originate in the appropriate upstream
artifact.

The preferred rule is:

> **Change the source of intent before changing derived artifacts.**

For example, when a requirement changes, the specification, plan, tasks,
implementation, and tests must be evaluated for impact.

Spec Kit's current guidance explicitly supports a living-spec model in
which `spec.md` is treated as the contract and downstream artifacts are
updated when intended behavior changes.

## 13. Large Features

When a feature is too large to maintain reliably as a single
specification and implementation cycle, it should be decomposed into
independently manageable specifications.

Ptilon adopts Spec Kit's "spec of specs" concept for this purpose.

The decomposition should preserve traceability between the higher-level
objective and the individual specifications.

## 14. Existing Systems

Ptilon does not require an entire existing system to be retrospectively
specified before making a change.

For an existing system, the specification should describe the intended
change and explicitly identify compatibility boundaries that must remain
intact.

This follows the current Spec Kit guidance for existing projects.

## 15. Defect and Bug Work

Feature development and defect correction should not be treated as
identical workflows.

For defects, the process should distinguish:

```text
Observed behavior
    ↓
Diagnosis
    ↓
Root / contributing cause
    ↓
Scoped correction
    ↓
Verification of original symptom
    ↓
Regression verification
```

Ptilon uses Spec Kit's bug-fixing process where appropriate rather
than creating a parallel defect methodology.

## 16. AI-Specific Controls

Ptilon explicitly addresses risks associated with AI-assisted
development.

Controls include:

- explicit specifications;
- quality gates;
- consistency analysis;
- human review;
- automated verification;
- security verification;
- traceability;
- controlled context;
- evidence preservation;
- convergence analysis.

Particular attention should be given to:

- hallucinated requirements;
- invented APIs or dependencies;
- incorrect assumptions;
- inconsistent artifacts;
- insecure generated code;
- incomplete tests;
- specification drift;
- implementation drift;
- loss of decision rationale;
- excessive reliance on generated output.

## 17. Tool Independence

Ptilon uses GitHub Spec Kit as the primary SDD implementation reference,
but the methodology itself is not tied to a single coding agent.

The conceptual artifacts and quality controls should remain
understandable and usable even if the underlying AI tool changes.

## 18. Relationship to Established Standards

Ptilon is an integration methodology.

Its reference model includes:

| Domain | Primary reference |
| --- | --- |
| Software life cycle | ISO/IEC/IEEE 12207 |
| Requirements engineering | ISO/IEC/IEEE 29148 |
| Product quality | ISO/IEC 25010 |
| Architecture description | ISO/IEC/IEEE 42010 |
| Secure development | NIST SSDF |
| Specification-driven development | GitHub Spec Kit |
| Testing | Established testing practices |
| Architecture decisions | ADR practice |
| Delivery | CI/CD practices |

The detailed treatment and version of each reference is maintained under
`references/`.

## 19. Methodology Output

A Ptilon implementation should produce or maintain, as applicable:

- project constitution;
- requirements;
- specifications;
- clarification decisions;
- acceptance criteria;
- architecture documentation;
- architecture decisions;
- implementation plan;
- task breakdown;
- quality checklists;
- analysis results;
- source code;
- automated tests;
- verification evidence;
- security evidence;
- release evidence;
- change history.

Not every project requires every artifact. Required artifacts should be
determined by project size, complexity, risk, regulatory requirements,
and organizational governance.

## 20. Completion Model

A feature is considered ready for release when:

1. its intended behavior is explicitly specified;
2. relevant ambiguities have been resolved;
3. the technical approach is consistent with the specification;
4. implementation tasks have been completed;
5. required tests and quality controls have passed;
6. security controls appropriate to the risk have been satisfied;
7. traceability is sufficient for the feature;
8. convergence finds no unresolved implementation gaps;
9. required human approvals have been obtained.

## 21. Methodology Evolution

Ptilon distinguishes between:

- **Established practice** — adopted from an external standard or
  recognized practice.
- **Tool mechanism** — provided by Spec Kit or another tool.
- **Ptilon adaptation** — an established practice adapted for AI-assisted
  development.
- **Ptilon original control** — a mechanism created specifically to
  address a demonstrated gap.

Every Ptilon-specific mechanism should document why the existing practice
was insufficient and what problem the new mechanism addresses.

## 22. Status

This document defines the normative high-level structure of the Ptilon
methodology.

Detailed procedures, templates, prompts, checklists, examples, and
reference analyses are maintained in the corresponding repository
sections.
