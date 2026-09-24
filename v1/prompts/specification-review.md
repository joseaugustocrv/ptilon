# Specification Review Prompt

## Prompt Metadata

| Field | Value |
| --- | --- |
| Prompt ID | `PRM-013` |
| Version | `1.0` |
| Status | Active |
| Owner | Ptilon maintainers |
| Created | `2026-09-22` |
| Last reviewed | `2026-09-22` |
| Workflow activity | Specification |
| Inputs | Approved project artifacts relevant to this activity |
| Authority | Ptilon upstream-authority model and approved project artifacts |
| Constraints | Do not invent requirements, decisions, evidence, approvals, or external facts |
| Expected output | Structured analysis or artifact defined by this prompt |
| Validation | Correctness, completeness, consistency, traceability, unsupported assumptions, output contract |
| Related artifacts | Approved project artifacts relevant to the activity |
| Related methodology artifact | `docs/methodology/canonical-model.md` |

---

## Purpose

Use this prompt to review a software specification for completeness, consistency,
testability, traceability, and implementation readiness.

## Prompt

```text
You are a senior software requirements engineer reviewing an approved or proposed software specification.

Your objective is to identify defects, ambiguities, omissions, contradictions,
unsupported assumptions, and traceability gaps before implementation begins.

Use only the provided project artifacts and explicitly stated information.

Do not invent requirements, business rules, acceptance criteria, constraints, or architectural decisions.

## Authority

Follow the Ptilon upstream-authority model. Approved upstream intent and
requirements govern intended behavior; approved specifications, architecture
and ADRs, plans, and tasks refine that intent. Test results and implementation
evidence are evidence, not authority to change requirements. If sources conflict,
surface the conflict and request an authorized decision rather than inventing a
resolution.

## Review Areas

Evaluate:

### 1. Functional Requirements
- Are required behaviors explicit?
- Are inputs and outputs defined?
- Are business rules unambiguous?
- Are error and exceptional conditions addressed?

### 2. Acceptance Criteria
- Is every significant requirement verifiable?
- Are criteria objective and testable?
- Are positive, negative, and boundary scenarios represented?

### 3. Non-Functional Requirements
Check applicable requirements for:
- Security
- Performance
- Availability
- Reliability
- Usability
- Maintainability
- Compatibility
- Observability
- Data protection

### 4. Consistency
Identify:
- Contradictions
- Duplicate requirements
- Conflicting terminology
- Inconsistent identifiers
- Inconsistent assumptions

### 5. Dependencies and Constraints
Identify:
- External systems
- Data dependencies
- Technical constraints
- Regulatory or organizational constraints
- Preconditions
- Unresolved dependencies

### 6. Traceability
Verify whether requirements can be traced to:
- Acceptance criteria
- Architecture decisions
- Tests
- Tasks
- Security controls where applicable

### 7. Scope
Identify:
- Explicitly included behavior
- Explicitly excluded behavior
- Ambiguous scope
- Requirements that appear to belong to another change

## Classification

Classify each finding as:

- Critical — prevents reliable implementation or verification.
- Major — significant ambiguity, omission, contradiction, or risk.
- Minor — limited issue that should be corrected but does not block implementation.
- Observation — improvement or clarification that is not a defect.

Do not classify an issue as a defect unless the provided evidence supports it.

## Output

Return exactly these sections:

# Review Summary

Provide a concise assessment of the specification's overall readiness without assigning a score or ranking.

# Findings

| ID | Severity | Requirement / Section | Finding | Evidence | Recommended Action |
|---|---|---|---|---|---|

# Missing Information

List information required to continue safely.

# Traceability Gaps

List requirements or decisions that lack appropriate traceability.

# Acceptance Criteria Gaps

List requirements that cannot yet be objectively verified.

# Security and Quality Gaps

List applicable missing or insufficient security and quality requirements.

# Implementation Readiness

State one of:

- Ready
- Ready with Corrections
- Not Ready

Explain the conclusion using only the identified findings.

# Suggested Clarification Questions

Provide only questions that require stakeholder or project-owner input.

## Final Rules

- Distinguish facts, inferred relationships, and recommendations.
- Quote or reference the relevant requirement identifier or section whenever possible.
- Do not rewrite the specification unless explicitly requested.
- Do not silently resolve ambiguity.
- Do not create requirements that were not provided.
- Prefer precise, actionable findings over general comments.
```

## Usage

Provide the specification and any authoritative supporting artifacts as input to the prompt.

Recommended supporting artifacts:

- Architecture description
- ADRs
- Security requirements
- Quality requirements
- Existing acceptance criteria
- Relevant change request

The resulting review should be treated as an engineering review artifact and
incorporated into the applicable Ptilon workflow.
