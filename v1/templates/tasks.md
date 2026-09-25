# Ptilon Tasks Template

## 1. Purpose

Define implementation tasks derived from an approved specification and

technical plan.

Tasks should be actionable, dependency-aware, traceable, and sufficiently

precise for implementation without becoming a substitute for the

specification or architecture.

---

## 2. Change Information

**Project:** [Project]

**Feature / Change:** [Name]

**Specification:** [Reference]

**Plan:** [Reference]

**Owner:** [Owner]

---

## 3. Task Principles

Tasks should:

- have a clear objective;
- identify relevant dependencies;
- remain traceable to governing artifacts;
- be small enough to execute and verify;
- identify the affected component, file, interface, or artifact when known;
- state the expected implementation behavior or change;
- identify relevant verification and acceptance criteria;
- expose blockers and assumptions;
- avoid silently introducing new requirements or architectural decisions.

---

## 4. Task Template

### TSK-001 — [Task title]

#### Objective

[What must be accomplished?]

#### Scope of Change

[What component, file, interface, data structure, test, or artifact is expected
to change?]

#### Source

[Requirement / specification / ADR / plan reference]

#### Expected Behavior

[Describe the behavior or implementation outcome required by the source
artifacts.]

#### Dependencies

- [T-XXX]

- [External dependency]

#### Implementation Notes

[Relevant technical guidance.]

#### Verification

[Specific test, check, acceptance criterion, review, or other completion signal.]

#### Acceptance / Completion Criteria

- [ ] [Observable criterion]
- [ ] [Observable criterion]

#### Evidence

[Expected evidence.]

#### Status

[Pending / In Progress / Blocked / Done]

---

## 5. Task Categories

Use categories when they improve organization.

Examples:

- Requirements
- Architecture
- Backend
- Frontend
- Database
- Integration
- Security
- Testing
- Documentation
- Infrastructure
- CI/CD
- Migration

---

## 6. Dependency Ordering

Tasks should be ordered according to actual dependencies rather than arbitrary

execution order.

Example:

```text
TSK-001 — Define data model

    ↓

TSK-002 — Implement persistence

    ↓

TSK-003 — Implement service logic

    ↓

TSK-004 — Implement API

    ↓

TSK-005 — Add acceptance tests
```

Parallel work should be identified when dependencies allow it.

---

## 7. Verification

Each task should identify an appropriate completion signal.

Examples:

- unit test passes;
- integration test passes;
- acceptance criterion verified;
- migration executed successfully;
- security check passes;
- documentation updated;
- artifact generated.

“Code completed” alone is generally insufficient evidence.

---

## 8. AI-Assisted Task Generation

AI may assist with:

- task decomposition;
- dependency identification;
- sequencing;
- verification suggestions;
- missing-task detection.

Generated tasks must be reviewed for:

- missing work;
- duplicated work;
- incorrect dependencies;
- unsupported implementation assumptions;
- hidden scope expansion.

AI must not silently convert assumptions into requirements.

---

## 9. Change Impact

When the governing specification or plan changes:

1. identify affected tasks;
2. update or remove obsolete tasks;
3. create missing tasks;
4. reassess dependencies;
5. rerun consistency analysis.

The task list is derived from higher-level artifacts and must remain

synchronized with them.

---

## 10. Blocked Tasks

A blocked task should identify:

- blocker;
- responsible party;
- affected work;
- expected resolution;
- impact if unresolved.

Example:

**Status:** Blocked

**Blocker:** API contract not approved.

**Owner:** [Role]

**Impact:** TSK-004 cannot begin.

---

## 11. Definition of Done

A task is complete when:

- the intended work is implemented;
- applicable tests pass;
- required review is complete;
- relevant quality and security checks pass;
- evidence is available;
- related documentation is updated when required.

Project-specific Definition of Done rules may be stricter.

---

## 12. Traceability

Maintain the relationship:

Requirement → Plan → Task → Implementation → Test → Evidence

Use stable identifiers where traceability is required.

---

## 13. Task Summary

| ID | Task | Dependency | Verification | Status |
| --- | --- | --- | --- | --- |
| TSK-001 | [Task] | — | [Verification] | Pending |
| TSK-002 | [Task] | TSK-001 | [Verification] | Pending |

---

## 14. Ptilon Workflow

Tasks are created after planning and quality checks:

### Workflow

**Specify → Clarify → Plan → Checklist → Tasks → Analyze → Implement →

Converge**

Task generation should not begin from an ambiguous or materially incomplete

specification.

---

## 15. Implementation Readiness

A task is implementation-ready only when an implementer can determine from the
task and its linked authoritative artifacts:

- what behavior or technical change is required;
- why the change is required;
- which component, file, interface, or artifact is affected, when known;
- which requirements or acceptance criteria govern the work;
- what dependencies or blockers exist;
- what completion criteria must be satisfied;
- how completion will be verified.

A task that requires the implementer to invent a requirement, make an
unrecorded architectural decision, or discover the expected behavior from
informal conversation is not implementation-ready. Raise a `QST-###` instead.

## 16. Status

This template defines the recommended structure for implementation tasks within
Ptilon.

Projects may adapt the format while preserving traceability, dependency

clarity, verification, and alignment with the governing specification.
