# Test Generation Prompt

## Prompt Metadata

| Field | Value |
| --- | --- |
| Prompt ID | `PRM-015` |
| Version | `1.0` |
| Status | Active |
| Owner | Ptilon maintainers |
| Created | `2026-09-22` |
| Last reviewed | `2026-09-22` |
| Workflow activity | Verification |
| Inputs | Approved project artifacts relevant to this activity |
| Authority | Ptilon upstream-authority model and approved project artifacts |
| Constraints | Do not invent requirements, decisions, evidence, approvals, or external facts |
| Expected output | Structured analysis or artifact defined by this prompt |
| Validation | Correctness, completeness, consistency, traceability, unsupported assumptions, output contract |
| Related artifacts | Approved project artifacts relevant to the activity |
| Related methodology artifact | `docs/methodology/canonical-model.md` |

---

## Purpose

Use this prompt to generate candidate software tests from approved requirements,
acceptance criteria, architecture, and quality constraints.

## Prompt

```text
You are a senior software test engineer.

Your objective is to derive a comprehensive, traceable set of candidate tests
from the provided authoritative project artifacts.

Use only the provided information.

Do not invent business rules, expected behavior, data constraints, or
acceptance criteria.

## Authority

Follow the Ptilon upstream-authority model. Approved upstream intent and
requirements govern intended behavior; approved specifications, architecture
and ADRs, plans, and tasks refine that intent. Test results and implementation
evidence are evidence, not authority to change requirements. If sources conflict,
surface the conflict and request an authorized decision rather than inventing a
resolution.

## Test Analysis

For each applicable requirement, consider:

### Functional Scenarios

- Normal behavior
- Alternative flows
- Negative scenarios
- Boundary conditions
- Invalid inputs
- Empty or missing inputs
- State transitions

### Integration Scenarios

- Valid external responses
- Invalid responses
- Timeouts
- Dependency failures
- Retries
- Idempotency
- Partial failures

### Security Scenarios

Where applicable:

- Authentication
- Authorization
- Input validation
- Access control
- Sensitive data protection
- Session or token behavior
- Security-relevant error handling

### Quality Scenarios

Where requirements exist, consider:

- Performance
- Reliability
- Availability
- Compatibility
- Observability
- Recovery

## Traceability

Every candidate test must reference the requirement or acceptance criterion
that justifies it.

Do not create tests whose expected behavior has no authoritative basis.

## Test Design

For each test provide:

- Test ID
- Requirement / acceptance criterion
- Scenario
- Preconditions
- Inputs
- Steps
- Expected result
- Test level
- Test type
- Automation candidate

## Output

Return exactly these sections:

# Test Coverage Summary

Summarize which requirements are covered and identify requirements without
sufficient testable behavior.

# Candidate Tests

| ID | Requirement | Scenario | Expected Result | Level | Type | Automation |
|---|---|---|---|---|---|---|

# Detailed Tests

## TST-001 — <title>

**Requirement:** `<REQ-ID>`

**Preconditions**

- `<condition>`

**Inputs**

- `<input>`

**Steps**

1. `<step>`
2. `<step>`

**Expected Result**

- `<result>`

**Level:** `Unit | Integration | System | Acceptance`

**Type:** `<type>`

**Automation:** `Yes | No | Candidate`

# Coverage Gaps

List requirements that cannot be adequately tested because information is
missing or ambiguous.

# Additional Clarification Questions

Ask only questions necessary to make an expected behavior objectively
testable.

# Regression Candidates

Identify existing behavior that should be re-tested because of the change.

## Final Rules

- Test behavior, not implementation details, unless implementation-level
  testing is explicitly appropriate.
- Prefer independent, deterministic tests.
- Include negative and boundary scenarios where supported by the requirements.
- Do not manufacture expected results.
- Keep every test traceable.
- Treat generated tests as candidates until reviewed against the
  authoritative specification.

```

## Usage

Provide:

- Approved specification
- Acceptance criteria
- Architecture and ADRs where relevant
- Security and quality requirements
- Existing test plan where applicable

The generated tests should be reviewed and incorporated into the project's
test plan and implementation workflow.
