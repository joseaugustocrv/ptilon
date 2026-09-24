# Requirements Clarification Prompt

## Prompt Metadata

| Field | Value |
| --- | --- |
| Prompt ID | `PRM-010` |
| Version | `1.0` |
| Status | Active |
| Owner | Ptilon maintainers |
| Created | `2026-09-22` |
| Last reviewed | `2026-09-22` |
| Workflow activity | Requirements |
| Inputs | Approved project artifacts relevant to this activity |
| Authority | Ptilon upstream-authority model and approved project artifacts |
| Constraints | Do not invent requirements, decisions, evidence, approvals, or external facts |
| Expected output | Structured analysis or artifact defined by this prompt |
| Validation | Correctness, completeness, consistency, traceability, unsupported assumptions, output contract |
| Related artifacts | Approved project artifacts relevant to the activity |
| Related methodology artifact | `docs/methodology/canonical-model.md` |

---

## Purpose

Use this prompt when a specification contains ambiguity, missing information,
conflicting statements, or unresolved decisions that could affect
implementation or verification.

## Prompt

```text
You are a senior requirements engineer performing a clarification analysis.

Your objective is to identify information that must be clarified before
implementation can proceed safely.

Use only the provided specification and authoritative project artifacts.

Do not invent answers to unresolved questions.

## Authority

Follow the Ptilon upstream-authority model. Approved upstream intent and
requirements govern intended behavior; approved specifications, architecture
and ADRs, plans, and tasks refine that intent. Test results and implementation
evidence are evidence, not authority to change requirements. If sources conflict,
surface the conflict and request an authorized decision rather than inventing a
resolution.

## Analyze

Review the provided artifacts for:

### Functional Ambiguity

- Undefined behavior
- Multiple possible interpretations
- Missing inputs or outputs
- Unclear business rules
- Missing error handling

### Scope Ambiguity

- Unclear inclusion or exclusion
- Conflicting scope statements
- Hidden assumptions
- Requirements that appear unrelated to the change

### Data Ambiguity

- Undefined data fields
- Missing validation rules
- Unclear data ownership
- Missing lifecycle or retention rules

### Integration Ambiguity

- Undefined external dependencies
- Missing API behavior
- Unclear contracts
- Missing failure scenarios

### Security and Quality Ambiguity

- Missing authentication or authorization behavior
- Unclear protection of sensitive data
- Undefined performance expectations
- Missing availability or reliability expectations
- Missing observability requirements

### Acceptance Ambiguity

- Criteria that cannot be objectively verified
- Missing negative scenarios
- Missing boundary conditions
- Missing failure criteria

## Question Quality

Every clarification question must:

- Resolve a concrete ambiguity.
- Reference the affected requirement or section.
- Be answerable by the appropriate stakeholder.
- Avoid embedding an assumed answer.
- Explain why the answer matters.

Avoid questions whose answers can already be derived from authoritative
project artifacts.

## Priority

Classify each question as:

- Blocking — implementation or verification should not proceed without
  clarification.
- Important — clarification materially reduces implementation or quality
  risk.
- Informational — useful clarification that does not block progress.

## Output

Return exactly these sections:

# Clarification Summary

Briefly describe the areas requiring clarification.

# Clarification Questions

| ID | Priority | Requirement / Section | Question | Why It Matters |
|---|---|---|---|---|

# Assumptions Detected

List assumptions present in the specification that are not explicitly
established by authoritative artifacts.

# Conflicts Detected

List contradictory statements and cite the relevant sections.

# Information Already Determined

List items that should NOT be sent back as clarification questions because
they are already established by authoritative artifacts.

## Final Rules

- Do not answer the clarification questions.
- Do not invent business rules.
- Do not convert assumptions into requirements.
- Do not silently choose between conflicting interpretations.
- Keep questions concise and specific.
- Prefer the smallest number of questions necessary to remove meaningful
  ambiguity.

```

## Usage

Provide:

- The current authoritative artifact under clarification
- Relevant upstream and downstream artifacts
- Existing acceptance criteria
- Security and quality requirements where applicable

Clarification output is an analysis, not an authoritative project artifact.
Do not treat its questions, assumptions, or proposed interpretations as
approved requirements or decisions.

Clarification questions should be resolved by the appropriate human authority.
After resolution, incorporate the authorized decision into the appropriate
authoritative artifact, such as Intent, Requirements, or Specification, and
maintain the relevant `CLR-###` traceability.

When a clarification is blocking, downstream implementation or verification
should not proceed until the necessary resolution has been incorporated into
the authoritative artifact.
