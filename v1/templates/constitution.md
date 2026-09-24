# Ptilon Constitution Template

## Purpose

Define the project principles that govern software development, architecture,
quality, security, and AI usage.

This is a project-level governance artifact. It should be created before
feature-level specification when the project adopts this governance mechanism.
It is not a lifecycle stage in the Ptilon canonical model.

The Ptilon canonical methodology is defined in
`../docs/methodology/canonical-model.md`; this Constitution template defines
project-specific principles that operate within that methodology.

---

## 1. Project Identity

**Project:** [Project name]

**Purpose:** [Short description]

**Repository:** [Repository]

**Owner:** [Responsible organization or team]

**Version:** [Version]

---

## 2. Core Principles

### Principle 1 — [Name]

[State the principle clearly and concisely.]

**Rationale:** [Why this principle exists.]

---

### Principle 2 — [Name]

[State the principle clearly and concisely.]

**Rationale:** [Why this principle exists.]

---

### Principle 3 — [Name]

[State the principle clearly and concisely.]

**Rationale:** [Why this principle exists.]

---

## 3. Requirements Engineering

Define the project's expectations for:

- requirement quality;
- specification;
- clarification;
- acceptance criteria;
- traceability;
- change management.

Example:

> Requirements must be explicit, verifiable, and traceable to their source
> when traceability is required by project risk or governance.

---

## 4. Architecture

Define architectural principles and constraints.

Consider:

- architectural style;
- technology constraints;
- modularity;
- interfaces;
- integration;
- data;
- scalability;
- observability;
- architectural decision records.

Example:

> Significant architectural decisions must be documented using ADRs or an
> equivalent mechanism.

---

## 5. Quality

Define quality expectations.

Consider:

- testing;
- maintainability;
- performance;
- reliability;
- security;
- compatibility;
- usability;
- observability.

Example:

> Quality requirements must be explicit and verifiable when relevant to the
> product.

---

## 6. Security

Define security principles and constraints.

Consider:

- authentication;
- authorization;
- data protection;
- secrets;
- dependencies;
- secure development;
- vulnerability management.

Example:

> Secrets must never be committed to source control.

---

## 7. AI Usage

Define how AI may be used in the project.

Consider:

- approved tools;
- sensitive information;
- generated specifications;
- generated code;
- generated tests;
- human review;
- evidence;
- intellectual property;
- security.

Example:

> AI-generated artifacts must be validated according to their impact and risk
> before becoming authoritative project artifacts.

---

## 8. Testing and Verification

Define the project's verification expectations.

Consider:

- unit testing;
- integration testing;
- acceptance testing;
- security testing;
- performance testing;
- automated verification;
- evidence retention.

Example:

> Changes must pass the applicable automated verification before release.

---

## 9. CI/CD

Define delivery principles.

Consider:

- required checks;
- branch protection;
- environments;
- approvals;
- deployment;
- rollback;
- artifact traceability.

---

## 10. Governance

Define:

- decision ownership;
- approval responsibilities;
- exception handling;
- risk acceptance;
- release authority;
- documentation expectations.

Example:

> Exceptions to mandatory project controls must be explicitly recorded and
> approved by the responsible authority.

---

## 11. Traceability

Define the required traceability level.

A typical chain is:

Intent → Requirements → Specification → Architecture → Tasks → Implementation
→ Tests → Evidence → Release

Specify which relationships are mandatory for the project.

---

## 12. Development Workflow

The project adopts the following Ptilon canonical workflow:

Intent → Requirements → Specification → Architecture & Design → Plan →
Tasks → Implementation → Verification → Convergence → Release

Project-specific adaptations should be documented here.

---

## 13. Standards and References

List mandatory or adopted references.

Example:

- ISO/IEC/IEEE 12207
- ISO/IEC/IEEE 29148
- ISO/IEC 25010
- ISO/IEC/IEEE 42010
- NIST SSDF
- GitHub Spec Kit

For each reference, identify whether it is:

- mandatory;
- adopted;
- recommended;
- informative.

---

## 14. Exceptions

Define how deviations from this constitution are handled.

An exception should identify:

- principle or rule affected;
- reason;
- scope;
- risk;
- compensating control;
- responsible approver;
- review or expiration condition.

---

## 15. Amendment Procedure

Define how this constitution can be changed.

A change should:

1. identify the reason;
2. assess impact;
3. update the constitution;
4. assess affected project artifacts;
5. record approval;
6. communicate the change when necessary.

---

## 16. Governance Metadata

**Status:** [Draft / Active / Superseded]

**Version:** [Version]

**Effective date:** [Date]

**Approved by:** [Person / Role]

**Last review:** [Date]

**Next review:** [Date]

---

## 17. Notes

This template is intentionally generic.

Projects should adapt it to their context while preserving the Ptilon principles
of explicit intent, traceability, verification, security, proportionality, and
human accountability.
