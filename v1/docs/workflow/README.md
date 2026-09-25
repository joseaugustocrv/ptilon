# Ptilon Workflow

Ptilon uses one canonical engineering lifecycle. Clarification, analysis,
checklists, and reviews are activities or gates inside this lifecycle.

## Lifecycle

```text
Intent
  ↓
Requirements
  ↓
Specification
  ↓
Architecture & Design
  ↓
Plan
  ↓
Tasks
  ↓
Implementation
  ↓
Verification
  ↓
Convergence
  ↓
Release
```

The detailed definitions and authority rules are maintained in
[`../methodology/canonical-model.md`](../methodology/canonical-model.md).

## Decomposition

Requirements and Specifications may be organized into engineering units when
a project or change is too large or heterogeneous to manage reliably as a
single unit.

The default pattern is:

```text
Intent
  ↓
Requirements
  ├── Unit A
  ├── Unit B
  └── Unit C
       ↓
Specification
  ├── Unit A
  ├── Unit B
  └── Unit C
       ↓
Architecture
       ↓
Plan
       ↓
Tasks
       ↓
Implementation
       ↓
Verification
       ↓
Convergence
       ↓
Release
```

Architecture, Plan, Tasks, Verification, and other downstream artifacts are
updated according to impact rather than duplicated automatically for each unit.

## Cross-Cutting Activities

The following activities may occur at the relevant lifecycle points:

- Clarification — resolve ambiguity and missing information.
- Checklist — evaluate completeness and readiness.
- Analysis — evaluate dependencies, risks, security, quality, and conflicts.
- Review — evaluate an artifact against its authoritative inputs.
- Change impact analysis — evaluate the effect of a material change.

These activities do not create an alternative lifecycle.

## Spec-Driven Foundation

Where appropriate, Ptilon uses GitHub Spec Kit as an operational reference for
Specification-Driven Development. Spec Kit mechanisms such as Specify,
Clarify, Plan, Checklist, Tasks, Analyze, Implement, and Converge are mapped
onto the Ptilon lifecycle rather than replacing it.

## Quality Gates

Typical gates are:

1. Intent readiness.
2. Requirements readiness.
3. Specification readiness.
4. Architecture readiness.
5. Implementation readiness.
6. Verification readiness.
7. Convergence readiness.
8. Release readiness.

A project may use lighter or stronger gates according to risk.

## Traceability

The principal traceability chain is:

```text
REQ / SEC / QLT
      ↓
    ACC
      ↓
    TSK
      ↓
    TST
      ↓
Verification Evidence
```

Architecture and ADRs are linked where they explain or decide how requirements
are realized. Threats and mitigations are linked to security analysis.

## Authority

Downstream artifacts do not silently override upstream approved intent. When a
conflict is detected, the workflow must surface it, obtain an authorized human
decision, update the source of intent, and propagate the change.

## Evolution and Change Flow

A gap may be discovered at any lifecycle point. It must not be resolved by
silently inventing behavior.

```text
Any lifecycle activity
        ↓
      QST
        ↓
Clarification / analysis
        ↓
      CLR
        ↓
Update authoritative artifact
        ↓
Impact analysis
        ↓
Revalidate affected downstream artifacts
        ↓
Continue work
```

When the resolution changes approved intent or behavior, use `CHG` and the
material-change process:

```text
CHG
 ↓
Impact Analysis
 ↓
Update authoritative source
 ↓
Revise affected artifacts
 ↓
Revalidate
 ↓
Implementation
 ↓
Verification
 ↓
Convergence
 ↓
Release
```

`Implementation Ready` is reached only when the readiness criteria in the
canonical model are satisfied.

## AI Participation

AI may participate in any applicable activity. It must use the authoritative
project artifacts supplied for the activity, surface missing information, and
avoid inventing requirements, decisions, evidence, or approvals.

Human responsibility remains for domain intent, approvals, risk acceptance,
exceptions, significant architectural decisions, and release decisions.
