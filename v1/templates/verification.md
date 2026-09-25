# Verification Record Template

## 1. Purpose

Record objective evidence that implemented behavior satisfies applicable
requirements, acceptance criteria, quality controls, and security controls.

## 2. Verification Metadata

- **Verification:** [Reference]
- **Scope:** [Feature / Engineering Unit]
- **Specification:** [Reference]
- **Implementation:** [Commit / Build / Version]
- **Environment:** [Environment]
- **Date:** [Date]
- **Verifier:** [Person / Team]
- **Status:** [Planned / In Progress / Passed / Failed / Accepted with Exception]

## 3. Scope and Entry Criteria

Describe what is being verified and the conditions required to begin.

## 4. Verification Results

| Requirement / Criterion | Test / Method | Expected Result | Actual Result | Status | Evidence |
| --- | --- | --- | --- | --- | --- |
| [REQ / ACC / SEC / QLT] | [TST / method] | [Expected] | [Actual] | [Pass/Fail] | [Evidence] |

## 5. Defects and Exceptions

Record failed verification, known gaps, approved exceptions, and residual risks.

No failed or incomplete verification may be represented as passed evidence.

## 6. Regression Verification

Identify regression scenarios executed because of the change.

## 7. Security Verification

Record applicable security checks and results.

## 8. Quality Verification

Record applicable performance, reliability, compatibility, observability, and
other quality checks.

## 9. Evidence

List durable evidence such as test reports, logs, scan reports, screenshots,
build identifiers, or review records.

## 10. Conclusion

State whether the defined verification scope passed and identify any remaining
conditions.

## 11. Traceability

```text
Requirement → Acceptance Criterion → Test / Method → Result → Evidence
```
