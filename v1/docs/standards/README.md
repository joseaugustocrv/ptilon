# Ptilon — Standards

## 1. Purpose

Define the standards and established engineering references that provide the
technical foundation for Ptilon.

Ptilon uses standards as reference points for defining practices, controls,
quality attributes, lifecycle activities, and engineering decisions.

Standards provide guidance and constraints; they do not replace
project-specific analysis and decisions.

---

## 2. Core principle

A standard should be applied according to its scope, relevance, and context.

Ptilon distinguishes between:

- **Normative references** — standards or requirements that a project is
  explicitly required to comply with;
- **Reference standards** — established standards used to guide practices and
  decisions;
- **Engineering practices** — established techniques used to implement the
  methodology;
- **Project-specific rules** — constraints defined for a particular product or
  organization.

This distinction prevents references from being treated as universal
mandatory requirements without justification.

---

## 3. Primary standards

### 3.1 ISO/IEC/IEEE 12207:2026

Systems and software engineering — Software life cycle processes

Provides the lifecycle process foundation for organizing software development,
operation, maintenance, and evolution.

Ptilon uses 12207 primarily to establish lifecycle coverage and process
completeness.

---

### 3.2 ISO/IEC/IEEE 29148:2018

Systems and software engineering — Life cycle processes — Requirements engineering

Provides principles and practices for requirements engineering, including
requirements definition, analysis, specification, validation, and management.

Ptilon uses 29148 as a primary reference for requirements quality and
traceability.

---

### 3.3 ISO/IEC 25010:2023

Systems and software engineering — Systems and software Quality Requirements
and Evaluation (SQuaRE) — Product quality model

Provides the product quality model used by Ptilon to structure quality
attributes and quality requirements.

Ptilon uses ISO/IEC 25010 to avoid treating functional correctness as the
only dimension of software quality.

---

### 3.4 ISO/IEC/IEEE 42010:2022

Systems, software and enterprise — Architecture description

Provides principles for describing system architecture, including
stakeholders, concerns, viewpoints, views, and architecture descriptions.

Ptilon uses 42010 as a reference for architecture documentation and
architectural reasoning.

---

### 3.5 NIST Secure Software Development Framework

NIST SP 800-218 — Secure Software Development Framework (SSDF)

Provides a set of secure software development practices covering
organizational preparation, software protection, secure software production,
and vulnerability response.

Ptilon uses SSDF as its primary security development reference.

Reference: <https://csrc.nist.gov/pubs/sp/800/218/final>

---

## 4. Engineering practices

Ptilon also incorporates established engineering practices where appropriate.

### Specification-Driven Development

Ptilon uses GitHub Spec Kit as its primary operational reference for
Specification-Driven Development.

Reference: <https://github.com/github/spec-kit>

### Test-Driven Development

TDD may be used to establish executable expectations before or alongside
implementation.

### Behavior-Driven Development

BDD may be used when behavior-oriented examples provide clearer communication
between stakeholders and engineering teams.

### Architecture Decision Records

ADRs provide a lightweight mechanism for recording significant architectural
and technical decisions.

### Continuous Integration and Continuous Delivery

CI/CD provides automated validation and controlled delivery throughout the
lifecycle.

### Risk-Based Testing

Testing depth and coverage should be proportional to the risks and
consequences associated with the system and change.

---

## 5. Standards and AI-assisted development

AI does not change the underlying engineering requirements.

When AI is used to produce an artifact influenced by a standard, the artifact
remains subject to the applicable standard and project constraints.

Examples include:

- AI-generated requirements must still satisfy applicable requirements
  engineering principles;
- AI-generated architecture must still address relevant architectural
  concerns;
- AI-generated code must still satisfy applicable quality and security
  controls;
- AI-generated tests must still provide meaningful verification evidence.

AI output is not considered authoritative solely because it references a
standard.

---

## 6. Applying standards proportionally

Standards should be applied according to:

- system criticality;
- business impact;
- security and privacy risk;
- regulatory requirements;
- architectural complexity;
- project size;
- operational environment;
- change impact.

A small internal tool and a safety-critical system may require substantially
different levels of process and evidence.

The objective is appropriate engineering rigor, not unnecessary process
overhead.

---

## 7. Compliance and conformance

Ptilon distinguishes between:

Reference use

A standard informs engineering practices without a formal claim of compliance.

Conformance

The project intentionally follows the applicable requirements of a standard
and maintains sufficient evidence to support that claim.

Regulatory or contractual compliance

Compliance is required by an external obligation such as law, regulation,
contract, or organizational policy.

Claims of compliance must be supported by evidence and must not be inferred
merely from using a standard as a reference.

---

## 8. Version management

Standards evolve.

Ptilon documentation should identify the edition or version of a standard
when version differences may affect interpretation or implementation.

When a referenced standard is revised:

1. assess whether the change affects Ptilon;
2. identify affected practices;
3. update the relevant documentation;
4. update templates or controls if necessary;
5. preserve historical context when required.

---

## 9. Standards hierarchy

When multiple sources apply, the project should resolve precedence
explicitly.

A typical order is:

1. applicable law and regulation;
2. contractual obligations;
3. mandatory organizational policies;
4. project-specific requirements;
5. applicable standards;
6. Ptilon methodology;
7. recommended engineering practices.

This hierarchy is contextual: a project may define a different precedence
model when justified.

---

## 10. References

- ISO Standards: <https://www.iso.org/standards.html>
- ISO/IEC/IEEE 12207: <https://www.iso.org/standard/90219.html>
- ISO/IEC/IEEE 29148: <https://www.iso.org/standard/72089.html>
- ISO/IEC 25010: <https://www.iso.org/standard/78176.html>
- ISO/IEC/IEEE 42010: <https://www.iso.org/standard/74393.html>
- NIST SSDF: <https://csrc.nist.gov/Projects/ssdf>
- GitHub Spec Kit: <https://github.com/github/spec-kit>

---

## 11. Status

This document defines the standards and engineering references used by Ptilon.

Specific projects should document which standards are mandatory, applicable,
or merely informative for their context.
