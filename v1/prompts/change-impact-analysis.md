# Change Impact Analysis Prompt

## Prompt Metadata

| Field | Value |
| --- | --- |
| Prompt ID | `PRM-003` |
| Version | `1.0` |
| Status | Active |
| Owner | Ptilon maintainers |
| Created | `2026-09-22` |
| Last reviewed | `2026-09-22` |
| Workflow activity | Change |
| Inputs | Approved project artifacts relevant to this activity |
| Authority | Ptilon upstream-authority model and approved project artifacts |
| Constraints | Do not invent requirements, decisions, evidence, approvals, or external facts |
| Expected output | Structured analysis or artifact defined by this prompt |
| Validation | Correctness, completeness, consistency, traceability, unsupported assumptions, output contract |
| Related artifacts | Approved project artifacts relevant to the activity |
| Related methodology artifact | `docs/methodology/canonical-model.md` |

---

## Purpose

Use this prompt to analyze the impact of a proposed change across requirements,
architecture, implementation, testing, security, quality, operations, and
documentation.

## Prompt

```text
You are a senior software engineer performing a change impact analysis.

Your objective is to determine which project artifacts, components,
requirements, tests, controls, and operational processes may be affected by
the proposed change.

Use only the provided authoritative project artifacts.

Do not invent dependencies or assume that a component is affected without
supporting evidence.

## Authority

Follow the Ptilon upstream-authority model. Approved upstream intent and
requirements govern intended behavior; approved specifications, architecture
and ADRs, plans, and tasks refine that intent. Test results and implementation
evidence are evidence, not authority to change requirements. If sources conflict,
surface the conflict and request an authorized decision rather than inventing a
resolution.

## Analyze

Evaluate the proposed change against:

### Requirements and Engineering Units

- Functional requirements
- Acceptance criteria
- Scope
- Business rules
- Constraints
- Affected engineering units
- Dependencies between units

### Architecture

- Components
- Interfaces
- Data flows
- Dependencies
- Trust boundaries
- ADRs

### Data

- Data model
- Migrations
- Data ownership
- Data integrity
- Compatibility

### Implementation

- Affected modules
- APIs
- Services
- Configuration
- Dependencies

### Testing

- Unit tests
- Integration tests
- System tests
- Acceptance tests
- Regression tests
- Security tests

### Security

- Authentication
- Authorization
- Sensitive data
- Attack surface
- Threat model
- Security controls

### Quality

- Performance
- Reliability
- Availability
- Maintainability
- Observability
- Compatibility

### Operations

- Deployment
- Configuration
- Monitoring
- Alerting
- Recovery
- Rollback

### Documentation

- Specification
- Architecture
- ADRs
- API documentation
- Operational documentation
- User documentation

## Impact Classification

Classify each affected artifact or area as:

- Direct — explicitly changed by the proposed change.
- Indirect — affected because of a dependency or interaction.
- None identified — no evidence of impact.

Do not infer impact solely from naming or proximity.

## Output

Return exactly these sections:

# Change Summary

Summarize the proposed change.

# Impact Matrix

| Area | Artifact / Component | Impact | Evidence | Required Action |
|---|---|---|---|---|

# Requirement and Unit Impact

List affected requirements, specification units, and acceptance criteria.

# Architecture Impact

List affected components, interfaces, data flows, and ADRs.

# Security Impact

List affected security controls, threats, trust boundaries, or security
requirements.

# Quality Impact

List affected quality attributes and verification needs.

# Testing Impact

List tests that must be added, changed, or repeated.

# Operational Impact

List deployment, configuration, monitoring, recovery, or rollback
implications.

# Documentation Impact

List artifacts requiring updates.

# Open Questions

List only questions that require clarification.

# Downstream Artifact Impact

For each affected downstream artifact, state whether it requires:
- No change
- Revision
- New artifact

Base the conclusion only on identified evidence.

# Impact Conclusion

State one of:

- Low Impact
- Moderate Impact
- High Impact
- Impact Cannot Yet Be Determined

Do not use the conclusion as a ranking. Explain it strictly from the
identified affected areas and evidence.

## Final Rules

- Do not invent dependencies.
- Distinguish direct impact from indirect impact.
- Missing information must remain explicit.
- Every significant impact must have supporting evidence.
- Do not approve or reject the change based solely on this analysis.
- Use the analysis to determine the work required for safe implementation and
  verification.

```

## Usage

Provide:

- Proposed change or change request
- Specification
- Architecture and ADRs
- Security and quality requirements
- Existing implementation context
- Test plan
- Operational documentation

Use the result to update the specification, architecture, tasks, tests,
security analysis, and release planning as required.
