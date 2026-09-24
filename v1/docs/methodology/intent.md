# Intent

## Purpose

Intent establishes why a software project or change exists, what outcome is
desired, and the initial boundaries and constraints that should guide
downstream engineering.

Intent is the first stage of the canonical Ptilon lifecycle:

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

## What Intent Contains

An Intent artifact should capture, as applicable:

- the problem or opportunity;
- the objective;
- relevant stakeholders;
- known scope boundaries;
- desired outcomes;
- established constraints;
- material assumptions;
- open questions that require clarification.

Intent should describe **why** the work exists and **what outcome is desired**.
It should not unnecessarily prescribe the technical solution.

## Authority

Once approved, Intent is an upstream authoritative artifact.

Downstream requirements and engineering artifacts refine the approved intent.
They must not silently change its meaning.

If downstream analysis identifies a missing or changed business need, the
appropriate upstream artifact must be updated through the applicable change
and approval process.

## Assumptions and Open Questions

Assumptions and open questions recorded in Intent are not equivalent to
approved requirements or decisions.

Material uncertainty should be resolved before downstream work relies on it.
When clarification is required, use the Ptilon clarification activity and
incorporate the authorized resolution into the appropriate authoritative
artifact.

## Quality Gate

Before Intent is approved, verify that:

- the problem or opportunity is understandable;
- the desired outcome is explicit;
- relevant stakeholders are identified;
- known scope boundaries are visible;
- known constraints are recorded;
- material assumptions are visible;
- material open questions are identified;
- the Intent does not unnecessarily prescribe implementation details;
- the Intent is suitable to guide requirements engineering.

## Template

Use the reusable [Intent Template](../../templates/intent.md) to record an
Intent artifact.

## Traceability

Intent is the upstream source for requirements and subsequent engineering
artifacts derived from it. Traceability should remain explicit as downstream
artifacts are created or changed.
