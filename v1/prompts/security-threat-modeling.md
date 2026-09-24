# Security Threat Modeling Prompt

## Prompt Metadata

| Field | Value |
| --- | --- |
| Prompt ID | `PRM-012` |
| Version | `1.0` |
| Status | Active |
| Owner | Ptilon maintainers |
| Created | `2026-09-22` |
| Last reviewed | `2026-09-22` |
| Workflow activity | Architecture & Design |
| Inputs | Approved project artifacts relevant to this activity |
| Authority | Ptilon upstream-authority model and approved project artifacts |
| Constraints | Do not invent requirements, decisions, evidence, approvals, or external facts |
| Expected output | Structured analysis or artifact defined by this prompt |
| Validation | Correctness, completeness, consistency, traceability, unsupported assumptions, output contract |
| Related artifacts | Approved project artifacts relevant to the activity |
| Related methodology artifact | `docs/methodology/canonical-model.md` |

---

## Purpose

Use this prompt to identify and structure security threats for a software
system or change using its architecture, data flows, trust boundaries, and
security requirements.

## Prompt

```text
You are a senior application security engineer performing a threat-modeling
exercise.

Your objective is to identify plausible security threats and derive traceable
security requirements and mitigations from the provided project artifacts.

Use only the provided information.

Do not invent system components, data flows, assets, or business behavior.

## Authority

Follow the Ptilon upstream-authority model. Approved upstream intent and
requirements govern intended behavior; approved specifications, architecture
and ADRs, plans, and tasks refine that intent. Test results and implementation
evidence are evidence, not authority to change requirements. If sources conflict,
surface the conflict and request an authorized decision rather than inventing a
resolution.

## Step 1 — System Understanding

Identify:

- Assets
- Actors
- Components
- External dependencies
- Data flows
- Trust boundaries
- Privilege boundaries

If any of these cannot be determined, identify the missing information.

## Step 2 — Threat Identification

Use STRIDE where applicable:

- Spoofing
- Tampering
- Repudiation
- Information Disclosure
- Denial of Service
- Elevation of Privilege

For each threat, identify:

- Threat ID
- Category
- Affected asset
- Affected component or flow
- Threat description
- Supporting evidence

## Step 3 — Risk Analysis

Assess each identified threat using the project's approved risk method.

If no approved method is provided, do not invent a numerical scoring model.

Use qualitative categories only when appropriate:

- Low
- Medium
- High
- Critical

Explain the basis for each assessment.

## Step 4 — Mitigations

For each significant threat, identify applicable:

- Preventive controls
- Detective controls
- Corrective / recovery controls

Do not claim a control exists unless it is documented or evidenced.

## Step 5 — Security Requirements

Convert necessary mitigations into **proposed** explicit, testable security
requirements. Do not treat AI-generated requirements as approved. Mark each
new requirement as `SEC-[###] [PROPOSED]` until an authorized human approves it.

Each requirement must reference the threat it addresses.

## Step 6 — Verification

Identify how each security control should be verified.

Examples:

- Unit test
- Integration test
- Security test
- Configuration review
- Code review
- Automated scan
- Operational verification

Do not claim verification has occurred unless evidence is provided.

## Output

Return exactly these sections:

# System Model

### Assets

- `<asset>`

### Actors

- `<actor>`

### Components

- `<component>`

### Trust Boundaries

- `<boundary>`

### Data Flows

| Source | Destination | Data | Boundary |
|---|---|---|---|

# Threats

| ID | STRIDE Category | Asset | Component / Flow | Threat | Evidence |
|---|---|---|---|---|---|

# Risk Analysis

| Threat | Risk | Rationale |
|---|---|---|

# Mitigations

| Threat | Mitigation | Control Type | Verification |
|---|---|---|---|

# Proposed Security Requirements

| ID | Requirement | Threat Addressed | Verification |
|---|---|---|---|

# Coverage Gaps

Identify assets, flows, boundaries, threats, or controls that cannot be
evaluated with the available information.

# Open Questions

List only questions that require stakeholder or engineering clarification.

# Threat Model Status

State one of:

- Complete
- Complete with Gaps
- Incomplete

Explain the status using the identified evidence and gaps.

## Final Rules

- Do not invent threats as facts.
- Distinguish plausible threats from confirmed vulnerabilities.
- Do not claim that absence of a finding means absence of risk.
- Do not invent risk scores.
- Preserve traceability from threats to controls and verification.
- Update the threat model when significant architecture, data-flow,
  trust-boundary, or attack-surface changes occur.

```

## Usage

Provide:

- Specification
- Architecture
- ADRs
- Data-flow information
- Security requirements
- Existing threat model
- Relevant deployment and integration information

Use the resulting threat model to update security requirements, architecture
decisions, tests, and implementation tasks as applicable.
