# Ptilon

> Software engineering with human and artificial intelligence working together.

Ptilon is a software development methodology designed for the systematic use of
Artificial Intelligence throughout the software engineering lifecycle.

It combines established Software Engineering practices with
Specification-Driven Development and AI-assisted engineering.

## Purpose

Ptilon aims to make AI-assisted software development:

- structured;
- traceable;
- verifiable;
- secure;
- maintainable;
- repeatable.

The methodology does not replace established Software Engineering practices.
It integrates them into a development process in which specifications,
engineering decisions, implementation, tests, and evidence remain connected
throughout the lifecycle.

## Core Principle

> **Make intent explicit before implementation, keep it traceable throughout
> development, and verify the result against that intent.**

## Development Model

The canonical lifecycle, authority model, identifier taxonomy, and AI
responsibility rules are defined in
[`v1/docs/methodology/canonical-model.md`](v1/docs/methodology/canonical-model.md).

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

Artificial Intelligence may participate throughout the process, but generated
artifacts are subject to defined quality gates and human accountability.

Ptilon is iterative: when a question or gap is discovered during architecture,
planning, implementation, or verification, it is recorded, resolved through
the appropriate authority, incorporated into the authoritative artifact, and
propagated through impact analysis before downstream work continues.

## Foundation

Ptilon builds upon established practices and standards, including:

- ISO/IEC/IEEE 12207 — Software life cycle processes
- ISO/IEC/IEEE 29148 — Requirements engineering
- ISO/IEC 25010 — Product quality model
- ISO/IEC/IEEE 42010 — Architecture description
- NIST Secure Software Development Framework (SSDF)
- Specification-Driven Development
- Test-Driven Development
- Behavior-Driven Development
- Architecture Decision Records
- Continuous Integration and Continuous Delivery

## AI-Assisted Development

Ptilon treats AI as an engineering participant rather than as an unrestricted
code generator.

AI may assist with:

- requirements analysis;
- specification generation;
- ambiguity detection;
- architecture analysis;
- implementation planning;
- code generation;
- test generation;
- documentation;
- consistency analysis;
- verification;
- convergence analysis.

Human responsibility remains essential for domain decisions, architectural
decisions, risk acceptance, and final accountability.

## Spec-Driven Development

Ptilon adopts GitHub Spec Kit as the operational foundation for
Specification-Driven Development where appropriate.

The Spec Kit workflow provides structured artifacts and processes for:

```text
Constitution
    ↓
Specification
    ↓
Clarification
    ↓
Plan
    ↓
Checklist
    ↓
Tasks
    ↓
Analysis
    ↓
Implementation
    ↓
Convergence
```

Ptilon adds the broader Software Engineering, Quality, Security, Governance,
and Traceability context around this workflow.

## Traceability

A central objective of Ptilon is maintaining traceability across the software
lifecycle:

```text
Intent
    ↓
Requirement / Engineering Unit
    ↓
Specification
    ↓
Acceptance Criteria
    ↓
Architecture / Design Decision
    ↓
Task
    ↓
Code
    ↓
Test
    ↓
Verification Evidence
```

## Quality

Quality is treated as a continuous engineering concern.

Relevant quality characteristics are translated into:

- requirements;
- acceptance criteria;
- architecture decisions;
- implementation constraints;
- automated tests;
- verification activities;
- release criteria.

## Security

Security is integrated into the lifecycle rather than treated solely as a
final validation activity.

Security requirements, threats, controls, verification activities, and
evidence should be incorporated according to project risk.

## Governance

Ptilon defines explicit controls for:

- human approval;
- AI-generated artifacts;
- requirements changes;
- specification changes;
- architecture decisions;
- quality gates;
- security gates;
- traceability;
- verification evidence.

## Repository Structure

```text
v1/        Versioned Ptilon methodology and documentation
  docs/       Methodology and operational documentation
  prompts/    AI-assisted engineering prompts
  templates/  Reusable methodology artifacts
  examples/   Complete examples
  references/ Standards and engineering references
  assets/     Visual identity and supporting assets
.github/    Repository automation
README.md   Project entry point
CHANGELOG.md Release history
```

## Status

Ptilon v1 is an established methodology baseline.

The methodology is maintained as a versioned engineering system. Material
changes to lifecycle behavior, engineering controls, or reusable artifacts
should be evaluated for impact and recorded in the changelog.
