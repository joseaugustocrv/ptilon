# Ptilon — Quality

## 1. Purpose

Define the quality principles and controls that support reliable,
verifiable, maintainable, and secure software development with AI.

Quality is treated as a lifecycle concern rather than a final inspection.

## 2. Quality Principles

Ptilon follows these principles:

- quality requirements should be explicit;
- quality attributes should be measurable where practical;
- verification should be planned before implementation;
- defects should be detected as early as practical;
- automated verification should be preferred where appropriate;
- evidence should be preserved;
- quality controls should be proportional to risk.

## 3. Quality Model

Ptilon uses established quality models rather than defining a proprietary
quality taxonomy.

ISO/IEC 25010 is used as a principal reference for product quality.

Relevant quality characteristics should be translated into:

- requirements;
- acceptance criteria;
- architecture constraints;
- implementation controls;
- tests;
- verification evidence;
- release criteria.

Not every quality characteristic applies equally to every system.

## 4. Quality Requirements

Quality requirements should be explicit when they are important to the
system's behavior or risk profile.

Examples include:

- performance;
- reliability;
- availability;
- security;
- maintainability;
- compatibility;
- usability;
- scalability;
- recoverability;
- observability.

Quality requirements should be sufficiently precise to support objective
verification.

## 5. Verification Strategy

Verification should be planned as part of the development lifecycle.

A typical verification strategy may include:

```text
Requirement
    ↓
Acceptance Criterion
    ↓
Test / Verification Method
    ↓
Expected Result
    ↓
Evidence
```

Verification methods may include:

- unit testing;
- integration testing;
- system testing;
- acceptance testing;
- static analysis;
- security testing;
- performance testing;
- manual review;
- exploratory testing.

The selected methods should reflect the nature and risk of the software.

## 6. Test Strategy

Testing should provide evidence that the implemented software satisfies
its intended behavior.

Test coverage should be considered across:

- functional behavior;
- error handling;
- boundary conditions;
- integration points;
- quality requirements;
- security requirements;
- regression scenarios.

Tests should be traceable to the relevant requirements or acceptance
criteria when practical.

## 7. AI-Assisted Testing

AI may assist with:

- test case generation;
- test data generation;
- edge-case identification;
- test maintenance;
- failure analysis;
- coverage analysis.

AI-generated tests must be reviewed and validated.

Generated tests should not be treated as proof of correctness merely
because they execute successfully.

## 8. Static and Automated Analysis

Automated checks should be used where they provide meaningful value.

Depending on the project, these may include:

- formatting checks;
- linting;
- type checking;
- static analysis;
- dependency analysis;
- vulnerability scanning;
- secret detection;
- code coverage measurement.

Automated checks should be integrated into CI/CD where appropriate.

## 9. Quality Gates

Ptilon applies quality gates throughout the lifecycle.

Typical gates include:

### Requirements Gate

Requirements are sufficiently complete, consistent, feasible, and
verifiable.

### Specification Gate

The specification accurately represents intended behavior and includes
testable acceptance criteria.

### Architecture Gate

Architecture addresses relevant functional, quality, and security
constraints.

### Implementation Readiness Gate

Before coding begins, the scope is `Implementation Ready`: approved
requirements and architecture are current, material questions are resolved,
tasks are actionable and verifiable, and cross-artifact consistency analysis
has no unapproved blocking findings.

### Implementation Gate

Implementation follows approved artifacts and required engineering
controls. If implementation reveals a requirement, architecture, or domain
gap, raise a question and return through the controlled evolution loop rather
than silently inventing behavior.

### Verification Gate

Required tests and quality checks have passed, or approved exceptions
have been recorded.

### Release Gate

Release criteria, required evidence, and approvals are satisfied.

## 10. Defect Management

Defects should be analyzed and corrected systematically.

A defect workflow should distinguish:

```text
Observed Failure
    ↓
Reproduction
    ↓
Diagnosis
    ↓
Root / Contributing Cause
    ↓
Correction
    ↓
Regression Verification
```

The original failure should be verified after correction.

Regression coverage should be added when the defect reveals a gap in the
existing test suite.

## 11. Quality Evidence

Quality decisions and verification activities should produce durable
evidence.

Examples include:

- test results;
- automated check results;
- review records;
- quality assessments;
- defect records;
- coverage reports;
- release verification;
- approved exceptions.

Evidence should remain traceable to the relevant development artifacts.

## 12. Code Review

Code review should consider more than functional correctness.

Depending on the project's risk, review may consider:

- conformance to requirements;
- design consistency;
- maintainability;
- readability;
- error handling;
- performance;
- security;
- test adequacy;
- dependency usage;
- unintended side effects.

AI-assisted code should receive the same or stronger review controls as
other code, according to its risk.

## 13. Security and Quality

Security is an integral quality concern.

Security verification should be performed according to project risk and
applicable security requirements.

Relevant controls may include:

- threat modeling;
- secure coding review;
- dependency scanning;
- vulnerability testing;
- authentication and authorization testing;
- input validation testing;
- secrets detection.

Security evidence should be retained with other quality evidence.

## 14. Traceability

Quality activities should remain connected to intended behavior.

Where applicable:

```text
Requirement
    ↓
Quality Attribute
    ↓
Acceptance Criterion
    ↓
Test / Verification
    ↓
Evidence
```

This relationship allows quality claims to be supported by explicit
verification evidence.

## 15. Risk-Based Quality

Quality controls should be proportional to risk.

Factors may include:

- business criticality;
- security impact;
- regulatory requirements;
- technical complexity;
- operational exposure;
- change size;
- failure consequences.

Higher-risk systems or changes require stronger verification and evidence.

## 16. Continuous Improvement

Quality findings should contribute to continuous improvement.

Examples include:

- recurring defect analysis;
- test-gap analysis;
- workflow improvements;
- automation improvements;
- quality-gate refinement;
- updates to templates and prompts.

Improvements should be incorporated into the methodology when they address
repeatable needs.

## 17. Definition of Done

A project's Definition of Done should establish the minimum conditions for
considering work complete.

Typical conditions include:

- intended behavior implemented;
- acceptance criteria verified;
- required tests passed;
- required quality checks passed;
- applicable security checks completed;
- traceability updated;
- required evidence preserved;
- review completed;
- unresolved risks or exceptions explicitly recorded.

The exact Definition of Done may vary by project.

## 18. Relationship with Ptilon

Ptilon quality controls are integrated with the broader methodology.

Quality activities should connect:

```text
Requirements
    ↓
Specification
    ↓
Architecture
    ↓
Implementation
    ↓
Verification
    ↓
Evidence
    ↓
Release
```

Quality should not be treated as a separate phase after implementation.

## 19. References

- ISO/IEC 25010 — Product quality model
- ISO/IEC/IEEE 12207 — Software life cycle processes
- ISO/IEC/IEEE 29148 — Requirements engineering
- NIST — Secure Software Development Framework (SSDF)
- OWASP Application Security Verification Standard (ASVS)

## 20. Status

This document defines the quality guidelines for Ptilon.

Project-specific quality controls may extend these guidelines according to
system characteristics, risk, regulatory requirements, and organizational
governance.
