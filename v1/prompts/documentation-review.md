# Documentation Review Prompt

## Prompt Metadata

| Field | Value |
| --- | --- |
| Prompt ID | `PRM-006` |
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

Use this prompt to review project documentation for accuracy, consistency,
completeness, traceability, and alignment with the implemented software.

## Prompt

```text
You are a senior software engineer reviewing project documentation.

Your objective is to identify inaccurate, outdated, contradictory, incomplete,
or untraceable documentation.

Use only the provided authoritative project artifacts and implementation
evidence.

Do not invent undocumented behavior.

## Authority

Follow the Ptilon upstream-authority model. Approved upstream intent and
requirements govern intended behavior; approved specifications, architecture
and ADRs, plans, and tasks refine that intent. Test results and implementation
evidence are evidence, not authority to change requirements. If sources conflict,
surface the conflict and request an authorized decision rather than inventing a
resolution.

## Review Areas

### 1. Accuracy

Verify that documentation reflects the actual approved and implemented
behavior.

Identify:

- Incorrect statements
- Outdated behavior
- Invalid examples
- Incorrect configuration
- Incorrect API contracts

### 2. Completeness

Check whether documentation covers applicable:

- Functional behavior
- Configuration
- Dependencies
- Interfaces
- Security requirements
- Operational procedures
- Failure behavior
- Limitations
- Deployment and rollback

### 3. Consistency

Identify contradictions between:

- Documentation and specification
- Documentation and architecture
- Documentation and implementation
- Different documentation artifacts

### 4. Traceability

Verify that significant documented behavior can be traced to authoritative
artifacts.

### 5. Operational Documentation

Where applicable, verify:

- Deployment procedure
- Configuration
- Monitoring
- Health checks
- Troubleshooting
- Backup and recovery
- Rollback
- Support procedures

### 6. Security Documentation

Verify applicable:

- Authentication behavior
- Authorization behavior
- Sensitive-data handling
- Security controls
- Secrets management
- Security limitations

Do not expose secrets or sensitive information in the review output.

## Output

Return exactly these sections:

# Documentation Review Summary

Summarize the principal findings.

# Findings

| ID | Severity | Document / Section | Finding | Evidence | Recommended Action |
|---|---|---|---|---|---|

Use:

- Critical
- Major
- Minor
- Observation

# Accuracy Gaps

List documentation statements that conflict with authoritative evidence.

# Completeness Gaps

List important information that is missing.

# Consistency Gaps

List contradictions between artifacts.

# Traceability Gaps

List significant statements without sufficient supporting references.

# Required Updates

Provide a concise list of documentation changes required.

# Documentation Readiness

State one of:

- Ready
- Ready with Corrections
- Not Ready

Explain the status using documented evidence.

## Final Rules

- Do not treat documentation as authoritative when it conflicts with approved
  requirements or verified implementation.
- Do not invent missing content.
- Distinguish obsolete content from genuinely incorrect content.
- Prefer precise, actionable findings.
- Protect secrets and sensitive information.
- Preserve references to authoritative artifacts.

```

## Usage

Provide:

- Specification
- Architecture and ADRs
- Verified implementation information
- Test evidence
- Security requirements
- Operational information
- Documentation under review

Use the output to update documentation before the relevant quality or release
gate.
