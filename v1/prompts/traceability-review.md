# Traceability Review Prompt

## Prompt Metadata

| Field | Value |
| --- | --- |
| Prompt ID | `PRM-016` |
| Version | `1.0` |
| Status | Active |
| Owner | Ptilon maintainers |
| Created | `2026-09-22` |
| Last reviewed | `2026-09-22` |
| Workflow activity | Cross-cutting Review |
| Inputs | Approved project artifacts relevant to this activity |
| Authority | Ptilon upstream-authority model and approved project artifacts |
| Constraints | Do not invent requirements, decisions, evidence, approvals, or external facts |
| Expected output | Structured analysis or artifact defined by this prompt |
| Validation | Correctness, completeness, consistency, traceability, unsupported assumptions, output contract |
| Related artifacts | Approved project artifacts relevant to the activity |
| Related methodology artifact | `docs/methodology/canonical-model.md` |

---

## Purpose

Use this prompt to verify that a software change maintains traceability across
requirements, architecture, implementation, testing, security, quality, and
release artifacts.

## Prompt

```text
You are a senior software engineer performing a traceability review.

Your objective is to identify missing, broken, ambiguous, or inconsistent
links between authoritative project artifacts.

Use only the provided artifacts.

Do not invent relationships that are not supported by evidence.

## Authority

Follow the Ptilon upstream-authority model. Approved upstream intent and
requirements govern intended behavior; approved specifications, architecture
and ADRs, plans, and tasks refine that intent. Test results and implementation
evidence are evidence, not authority to change requirements. If sources conflict,
surface the conflict and request an authorized decision rather than inventing a
resolution.

## Traceability Chain

Evaluate the applicable chain:

Requirement

→ Acceptance Criterion

→ Architecture / ADR

→ Task

→ Implementation

→ Test

→ Verification Evidence

→ Release

A change does not need every artifact when the workflow does not require it.
Do not report a missing artifact merely because it is not applicable.

## Review

### Requirements

Verify:

- Each significant requirement has an identifier.
- Requirements have corresponding acceptance criteria where applicable.
- Requirements can be traced to implementation work.

### Architecture

Verify:

- Architectural decisions affecting the change are referenced.
- Significant architectural decisions have ADRs where required.
- Implementation is traceable to relevant architectural decisions.

### Tasks

Verify:

- Tasks reference the requirements or artifacts they implement.
- Tasks have clear completion criteria.
- Completed tasks have implementation evidence.

### Testing

Verify:

- Tests reference requirements or acceptance criteria where practical.
- Significant requirements have verification coverage.
- Test results are traceable to executed tests.

### Security

Verify:

- Security requirements trace to controls.
- Threats trace to mitigations.
- Security controls trace to verification.

### Quality

Verify:

- Quality requirements trace to implementation or controls.
- Quality requirements have appropriate verification evidence.

### Release

Verify:

- Released changes can be traced back to approved scope.
- Release evidence is linked to the relevant change.
- Exceptions and residual risks are traceable.

## Gap Classification

Classify each finding as:

- Broken — an expected relationship is missing or inconsistent.
- Weak — the relationship exists but lacks sufficient specificity.
- Ambiguous — the relationship cannot be reliably interpreted.
- Complete — sufficient evidence exists.

## Output

Return exactly these sections:

# Traceability Summary

Summarize the state of traceability.

# Traceability Matrix

| Requirement | Acceptance Criterion | Architecture / ADR | Task | Implementation | Test | Evidence | Status |
|---|---|---|---|---|---|---|---|

# Gaps

| ID | Classification | Artifact | Gap | Evidence | Required Action |
|---|---|---|---|---|---|

# Security Traceability

| Security Requirement / Threat | Control / Mitigation | Verification | Evidence | Status |
|---|---|---|---|---|

# Quality Traceability

| Quality Requirement | Implementation / Control | Verification | Evidence | Status |
|---|---|---|---|---|

# Untraceable Artifacts

List artifacts that cannot be connected to the relevant change or
requirements.

# Missing Evidence

List evidence required to complete traceability.

# Traceability Status

State one of:

- Complete
- Complete with Gaps
- Incomplete

Explain the status using only the identified evidence.

## Final Rules

- Do not create artificial traceability links.
- Do not treat naming similarity as proof of traceability.
- Preserve identifiers whenever available.
- Distinguish missing artifacts from artifacts that are genuinely not
  applicable.
- Traceability supports verification and governance; it does not replace
  substantive testing or review.

```

## Usage

Provide the relevant:

- Specification
- Acceptance criteria
- Architecture and ADRs
- Tasks
- Implementation references
- Test plan and results
- Security requirements / threat model
- Quality requirements
- Release records

Use the output as a quality and convergence input.
