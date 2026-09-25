# Clarification Record Template

## 1. Purpose

Record an uncertainty discovered during any Ptilon lifecycle activity and its
authorized resolution.

A clarification does not automatically change approved intent. If the
resolution changes approved meaning, create or update the applicable `CHG-###`.

## 2. Clarification Metadata

- **Clarification:** `CLR-001`
- **Question:** `QST-001`
- **Origin Activity:** [Intent / Requirements / Specification / Architecture /
  Plan / Tasks / Implementation / Verification / Convergence]
- **Related Artifacts:** [References]
- **Owner:** [Person / Team]
- **Status:** [Open / Resolved / Superseded]
- **Date:** [Date]

## 3. Question

Describe the ambiguity, missing information, conflict, or newly discovered fact.

## 4. Context and Evidence

Record the facts, artifacts, constraints, and evidence that motivated the
question.

## 5. Resolution

Describe the authorized answer or interpretation.

## 6. Authority

- **Decision Owner:** [Person / Role]
- **Approval / Evidence:** [Reference]
- **Decision Date:** [Date]

AI-generated proposals are not approval.

## 7. Impact Analysis

Identify whether the resolution affects:

- Intent
- Requirements
- Specification
- Architecture / ADRs
- Plan
- Tasks
- Tests / Verification
- Security / Threat Model
- Quality
- Documentation
- Operations
- Release evidence

## 8. Required Updates

| Artifact | Identifier | Action | Status |
| --- | --- | --- | --- |
| [Artifact] | [ID] | [Update / No change / Supersede] | [Pending / Done] |

## 9. Traceability

```text
QST → CLR → Affected Authoritative Artifact → Impacted Downstream Artifacts
```

## 10. Closure

The clarification is closed only when the authorized resolution has been
incorporated into the applicable authoritative artifacts and required impact
reviews have been completed.
