# Test Plan Template

## 1. Purpose

This template defines the standard structure for planning and documenting

software testing within Ptilon.

A test plan is derived from the approved specification, architecture,

acceptance criteria, quality requirements, and identified risks.

The test plan does not replace automated tests or acceptance criteria. It

provides the strategy and scope that guide their definition and execution.

---

## 2. Test Plan Metadata

- **Feature / Change:** `<name>`
- **Specification:** `<path or reference>`
- **Version:** `<version>`
- **Owner:** `<person or team>`
- **Status:** `Draft | Ready | In Progress | Completed`
- **Date:** `<YYYY-MM-DD>`

---

## 3. Objectives

Define what the testing activities must demonstrate.

Examples:

- Functional behavior satisfies the approved specification.
- Acceptance criteria are demonstrably satisfied.
- Quality requirements are verified.
- Regression risk is controlled.
- Security-relevant behavior is verified where applicable.

---

## 4. Scope

### 4.1 In Scope

- `<item>`
- `<item>`

### 4.2 Out of Scope

- `<item>`
- `<item>`

Out-of-scope items must be explicitly identified rather than assumed.

---

## 5. Test Strategy

Define the testing approach appropriate to the change.

### 5.1 Test Levels

- Unit tests
- Integration tests
- System tests
- Acceptance tests

Select only the levels applicable to the change and explain any omission.

### 5.2 Test Types

- Functional
- Regression
- Performance
- Security
- Usability
- Compatibility
- Reliability
- Other: `<type>`

### 5.3 Automation

Identify which tests must be automated.

- **Automated:** `<tests>`
- **Manual:** `<tests>`
- **Reason for manual execution:** `<reason>`

---

## 6. Traceability

Every significant requirement should be traceable to one or more verification

activities.

| Requirement | Acceptance Criterion | Test | Result |
| --- | --- | --- | --- |
| `<REQ-ID>` | `<ACC-ID>` | `<TST-ID>` | `Pending` |

Traceability must be maintained when the specification changes.

---

## 7. Test Cases

### TST-001 — `<name>`

**Requirement:** `<REQ-ID>`

### Preconditions

- `<condition>`

### Steps

1. `<step>`
2. `<step>`

### Expected Result

- `<expected result>`

**Status:** `Pending | Passed | Failed | Blocked`

---

## 8. Test Data and Environment

### Test Data

- `<dataset>`
- `<fixture>`
- `<mock/stub>`
- `<special condition>`

### Environment

- **Application version:** `<version>`
- **Runtime:** `<version>`
- **Database:** `<version>`
- **External dependencies:** `<dependencies>`

Environment differences that may affect results must be documented.

---

## 9. Risks and Coverage Gaps

Document known risks, limitations, and untested areas.

| Risk / Gap | Impact | Mitigation |
| --- | --- | --- |
| `<risk>` | `Low/Medium/High` | `<mitigation>` |

---

## 10. Entry Criteria

Testing may begin when the required conditions are satisfied.

Examples:

- Specification is approved.
- Acceptance criteria are defined.
- Required environments are available.
- Required test data exists.
- Build is deployable.

---

## 11. Exit Criteria

Testing may be considered complete when:

- Planned tests have been executed.
- Critical defects are resolved or formally accepted.
- Acceptance criteria have been verified.
- Required regression tests have passed.
- Known limitations are documented.
- Evidence required by the project has been retained.

---

## 12. Defect Handling

Failed tests must produce a traceable defect or change record when appropriate.

Each defect should identify:

- Related requirement or test.
- Reproduction steps.
- Expected behavior.
- Actual behavior.
- Evidence.
- Severity / priority.
- Resolution status.

---

## 13. Evidence

Record relevant evidence such as:

- Test execution results.
- Automated test reports.
- Screenshots or recordings.
- Logs.
- Performance measurements.
- Security test results.

Evidence should be sufficient to support independent verification.

---

## 14. AI Assistance

AI may assist with:

- Generating candidate test cases from specifications.
- Identifying missing scenarios.
- Suggesting boundary and negative cases.
- Generating test data.
- Reviewing test coverage.
- Drafting automated test code.

AI-generated tests must be reviewed against the approved specification and

acceptance criteria before being treated as authoritative.

---

## 15. Completion Record

- **Tests executed:** `<number>`
- **Passed:** `<number>`
- **Failed:** `<number>`
- **Blocked:** `<number>`
- **Open defects:** `<number>`
- **Coverage assessment:** `<summary>`
- **Final status:** `Passed | Passed with Exceptions | Failed`
- **Reviewed by:** `<person/team>`
- **Review date:** `<YYYY-MM-DD>`

---

## 16. Principles

Ptilon testing follows these principles:

1. Test against approved requirements, not assumptions.

2. Maintain traceability between requirements and verification.

3. Prefer automation for repeatable checks.

4. Test positive, negative, boundary, and failure scenarios.

5. Treat security and quality requirements as testable requirements.

6. Preserve objective evidence of significant verification activities.

7. Use AI to accelerate testing, not to replace engineering judgment.
