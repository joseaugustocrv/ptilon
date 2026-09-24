# Ptilon — Governance

## 1. Purpose

Define the governance principles and controls that ensure software

development with AI remains intentional, traceable, reviewable, and aligned

with organizational objectives.

Governance establishes how decisions are made, recorded, reviewed, and changed

throughout the software lifecycle.

---

## 2. Core principle

AI may accelerate analysis, specification, implementation, and verification,

but accountability for decisions remains with the responsible humans.

Governance must ensure that:

- decisions have identifiable ownership;
- relevant decisions are documented;
- changes remain traceable;
- risks are visible;
- quality and security controls are enforceable;
- exceptions are explicit and reviewable.

---

## 3. Governance layers

Ptilon governance operates across six complementary layers:

1. **Strategic governance** — objectives, scope, constraints, and priorities;
2. **Requirements governance** — intent, requirements, acceptance criteria,
   and changes;
3. **Technical governance** — architecture, design decisions, standards,
   and technical risks;
4. **Quality governance** — verification, quality attributes, evidence,
   and release criteria;
5. **Security governance** — security requirements, risks, vulnerabilities,
   and controls;
6. **Lifecycle governance** — releases, changes, maintenance, and
   continuous improvement.

These layers should remain connected through traceability.

---

## 4. Roles and responsibilities

Roles may vary by organization, but responsibilities must remain explicit.

### Human responsibilities

Humans are responsible for:

- defining objectives and constraints;
- approving requirements;
- resolving ambiguity and conflicts;
- approving significant architectural decisions;
- accepting residual risks;
- reviewing AI-generated artifacts when required;
- approving releases and exceptions.

### AI responsibilities

AI may assist with:

- analysis;
- drafting;
- decomposition;
- code generation;
- test generation;
- documentation;
- review support;
- consistency checks;
- traceability analysis.

AI output is subject to human validation according to its impact and risk.

---

## 5. Decision governance

Important decisions should be recorded in a durable form.

Examples include:

- requirements decisions;
- architecture decisions;
- technology selections;
- security decisions;
- risk acceptance;
- scope changes;
- deviations from standards;
- release decisions.

ADRs should be used for significant architectural and technical decisions.

---

## 6. Traceability

Ptilon promotes traceability across the lifecycle.

Where applicable, relationships should be maintained between:

### Traceability chain

Intent → Requirements → Specification → Architecture → Tasks → Implementation

→ Tests → Evidence → Release

Traceability does not require every artifact to reference every other

artifact. It requires sufficient relationships to demonstrate why a change

exists, what it affects, and how it was verified.

---

## 7. Change control

Changes must be evaluated according to their impact.

A change may affect:

- requirements;
- scope;
- architecture;
- implementation;
- tests;
- security;
- quality attributes;
- documentation;
- release plans.

Significant changes should trigger re-analysis of affected downstream

artifacts.

The principle is:

> Change the source of truth first, then propagate the change.

---

## 8. Exceptions and deviations

Exceptions to Ptilon practices, project standards, or defined controls

should be explicit.

An exception record should identify, when applicable:

- what is being deviated from;
- reason;
- affected scope;
- risks introduced;
- compensating controls;
- responsible approver;
- expiration or review condition.

Exceptions should not silently become permanent practices.

---

## 9. Quality gates

Governance is enforced through lifecycle gates.

Typical gates include:

- requirements readiness;
- specification readiness;
- architecture readiness;
- implementation readiness;
- verification readiness;
- release readiness.

A gate should define objective conditions that must be satisfied or explicitly

waived.

---

## 10. Evidence and auditability

Governance decisions should produce durable evidence.

Examples include:

- approved specifications;
- ADRs;
- review records;
- test results;
- security assessments;
- risk decisions;
- release records;
- change history.

Evidence should be stored in systems that preserve version history whenever

practical.

Git repositories are the preferred system of record for methodology artifacts

and project artifacts that can be versioned there.

---

## 11. Governance of AI usage

Projects using AI should define appropriate controls for:

- approved AI tools;
- information that may be submitted to AI systems;
- handling of confidential information;
- review requirements;
- attribution or provenance where required;
- validation of AI-generated artifacts;
- retention of relevant evidence;
- treatment of AI-generated code and specifications.

The level of control should be proportional to risk.

---

## 12. Risk-based governance

Not every artifact requires the same level of governance.

Controls should be proportional to factors such as:

- business impact;
- security impact;
- regulatory exposure;
- architectural complexity;
- change size;
- operational criticality;
- uncertainty;
- potential consequences of failure.

Higher-risk changes require stronger evidence and review.

---

## 13. Governance of the Ptilon methodology

Ptilon itself must evolve through controlled change.

Changes to the methodology should:

1. identify the reason for change;
2. evaluate impact on existing practices;
3. update affected normative documents;
4. update templates and prompts;
5. update examples where necessary;
6. review consistency across the repository;
7. record the resulting change.

The methodology should remain internally coherent and version controlled.

---

## 14. Relationship with Spec Kit

Ptilon uses GitHub Spec Kit as an operational reference for

Specification-Driven Development.

Spec Kit provides mechanisms for specification workflows and related artifacts.

Ptilon governance defines the broader controls around those mechanisms,

including:

- decision ownership;
- quality gates;
- security;
- traceability;
- evidence;
- exceptions;
- lifecycle management.

Ptilon should complement rather than unnecessarily duplicate Spec Kit

capabilities.

---

## 15. Minimum governance checklist

Before a significant release, verify that:

- ownership is clear;
- relevant requirements are approved;
- significant decisions are documented;
- applicable quality and security controls were executed;
- relevant risks are addressed or explicitly accepted;
- required evidence is available;
- changes are traceable;
- release approval is recorded.

---

## 16. References

- ISO/IEC/IEEE 12207 — Systems and software engineering — Software life
  cycle processes
- ISO/IEC/IEEE 29148 — Systems and software engineering — Requirements
  engineering
- ISO/IEC/IEEE 42010 — Architecture description
- ISO/IEC 25010 — Product quality model
- NIST — Secure Software Development Framework (SSDF):
  [https://csrc.nist.gov/Projects/ssdf](https://csrc.nist.gov/Projects/ssdf)
- GitHub Spec Kit: [https://github.com/github/spec-kit](https://github.com/github/spec-kit)

---

## 17. Status

This document defines the governance guidelines for Ptilon.

Project-specific governance rules may extend these guidelines while preserving

the principles of ownership, traceability, evidence, proportionality, and

controlled change.
