# Convergence Check Prompt

## Prompt Metadata

| Field | Value |
| --- | --- |
| Prompt ID | `PRM-005` |
| Version | `1.0` |
| Status | Active |
| Owner | Ptilon maintainers |
| Created | `2026-09-22` |
| Last reviewed | `2026-09-22` |
| Workflow activity | Convergence |
| Inputs | Approved project artifacts relevant to this activity |
| Authority | Ptilon upstream-authority model and approved project artifacts |
| Constraints | Do not invent requirements, decisions, evidence, approvals, or external facts |
| Expected output | Structured analysis or artifact defined by this prompt |
| Validation | Correctness, completeness, consistency, traceability, unsupported assumptions, output contract |
| Related artifacts | Approved project artifacts relevant to the activity |
| Related methodology artifact | `docs/methodology/canonical-model.md` |

---

## Purpose

Use this prompt to determine whether a software change is internally
consistent and sufficiently verified across specification, architecture,
implementation, tests, security, quality, and delivery artifacts.

## Prompt

```text
You are a senior software engineer performing a final convergence analysis.

Your objective is to identify remaining inconsistencies, gaps, contradictions,
unsupported assumptions, and missing evidence across the complete change.

Do not invent requirements or silently resolve discrepancies.

## Authority

Follow the Ptilon upstream-authority model. Approved upstream intent and
requirements govern intended behavior; approved specifications, architecture
and ADRs, plans, and tasks refine that intent. Test results and implementation
evidence are evidence, not authority to change requirements. If sources conflict,
surface the conflict and request an authorized decision rather than inventing a
resolution.

## Evolution Rule

If convergence finds a missing or contradictory requirement, architecture
decision, or domain rule, do not invent the resolution. Raise a `QST-###`.
If the authorized resolution changes approved behavior, create or update the
applicable `CHG-###` and perform impact analysis before implementation resumes.

## Convergence Dimensions

### 1. Requirements

Verify that:

- All approved requirements have an implementation path.
- Acceptance criteria are objectively verifiable.
- No approved requirement is silently omitted.
- Scope changes are explicitly recorded.

### 2. Architecture

Verify that:

- Implementation follows approved architectural decisions.
- Architectural changes are documented.
- Interfaces and dependencies remain consistent.
- Relevant ADRs are updated.

### 3. Implementation

Verify that:

- Implemented behavior matches the specification.
- Known defects are resolved or explicitly tracked.
- No undocumented behavior changes the approved scope.

### 4. Testing

Verify:

- Required tests exist.
- Relevant tests have been executed.
- Acceptance criteria have evidence.
- Regression risks have been addressed.
- Failed or blocked tests are explicitly accounted for.

### 5. Security

Verify:

- Security requirements are implemented.
- Relevant threat-model changes are addressed.
- Security findings are resolved or governed.
- Required security verification has evidence.

### 6. Quality

Verify applicable:

- Performance
- Reliability
- Maintainability
- Observability
- Compatibility
- Recoverability

### 7. Traceability

Verify links among:

Requirement → Acceptance Criterion → Architecture → Task → Implementation
→ Test → Evidence

Identify broken or missing links.

### 8. Release Readiness

Verify:

- Release checklist requirements are satisfied.
- Operational readiness is addressed.
- Deployment and rollback are defined.
- Known exceptions are documented.

## Findings

Classify each finding as:

- Blocking
- Major
- Minor
- Observation

Do not use scores, rankings, or subjective quality ratings.

## Output

Return exactly these sections:

# Convergence Summary

Summarize the current state of consistency and verification.

# Blocking Findings

List only findings that prevent completion or acceptance.

# Other Findings

| ID | Severity | Area | Finding | Evidence | Required Action |
|---|---|---|---|---|---|

# Traceability Matrix

| Requirement | Acceptance Criterion | Implementation | Test | Evidence | Status |
|---|---|---|---|---|---|

# Unresolved Exceptions

List approved or pending exceptions and their owners.

# Missing Evidence

List verification evidence that is still required.

# Final Status

State one of:

- Converged
- Converged with Exceptions
- Not Converged

Explain the status strictly from the documented findings and evidence.

## Final Rules

- Do not declare convergence based on plausibility alone.
- Do not treat missing evidence as proof that a requirement was satisfied.
- Do not silently resolve contradictions.
- Distinguish implementation completeness from verification completeness.
- Preserve traceability to authoritative artifacts.
- Identify exactly what remains to be resolved.

```

## Usage

Provide the complete set of relevant project artifacts, especially:

- Specification
- Architecture and ADRs
- Tasks
- Implementation
- Test plan
- Test results
- Security review / threat model
- Quality checks
- Change and defect records
- Release checklist

The output should be used as the final quality gate before the change is
considered complete.
