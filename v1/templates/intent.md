# Ptilon Intent Template

## 1. Purpose

Define the intent that establishes why a software change or project exists,
what outcome is desired, and the initial boundaries and constraints that should
guide downstream engineering artifacts.

Intent should express the desired outcome without prematurely prescribing the
solution.

---

## 2. Context

### Problem or Opportunity

[Describe the problem, need, opportunity, or situation that motivates the work.]

### Objective

[Describe the desired outcome.]

---

## 3. Stakeholders

| Stakeholder | Role / Interest |
| --- | --- |
| [Stakeholder] | [Role or interest] |

---

## 4. Scope

### In Scope

- [Item]

### Out of Scope

- [Item]

Only state boundaries that are known at the intent level. Detailed functional
and technical scope belongs in downstream artifacts.

---

## 5. Desired Outcomes

Describe the observable or meaningful outcomes expected from the work.

- [Outcome]

---

## 6. Known Constraints

Record constraints that are already established.

- [Constraint]

---

## 7. Known Assumptions

Record assumptions that materially affect the intent and are not yet confirmed.

| ID | Assumption | Validation |
| --- | --- | --- |
| ASM-001 | [Assumption] | [How / when validated] |

---

## 8. Open Questions

Record questions that must be clarified before downstream decisions can be
made.

| ID | Question | Owner | Status |
| --- | --- | --- | --- |
| QST-001 | [Question] | [Owner] | Open |

---

## 9. Traceability

The intent is the upstream source for the requirements and subsequent
engineering artifacts derived from it.

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

---

## 10. Intent Status

**Status:** [Draft / Approved / Superseded]

**Version:** [Version]

**Owner:** [Owner]

**Last updated:** [Date]

---

## 11. Quality Gate

Before the intent is used as an approved upstream artifact, verify that:

- the problem or opportunity is understandable;
- the desired outcome is explicit;
- relevant stakeholders are identified;
- known scope boundaries are visible;
- known constraints are recorded;
- material assumptions are visible;
- material open questions are identified;
- the intent does not unnecessarily prescribe implementation details;
- the intent is suitable to guide requirements engineering.

---

## 12. Clarification

Clarification is a cross-cutting activity and is not a lifecycle stage.

When ambiguity, missing information, or conflicts materially affect downstream
engineering, use the Ptilon clarification activity to identify questions.
Resolved decisions must be incorporated into the appropriate authoritative
artifact before downstream work relies on them.
