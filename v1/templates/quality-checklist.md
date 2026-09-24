# Ptilon Quality Checklist Template

## 1. Purpose

Provide a reusable quality gate for evaluating whether a specification, change,

or release is sufficiently defined and verified.

This checklist complements the Ptilon workflow and should be adapted to project

risk.

---

## 2. Change Information

**Project:** [Project]

**Change / Feature:** [Name]

**Specification:** [Reference]

**Version:** [Version]

**Reviewer:** [Name / Role]

**Date:** [Date]

---

## 3. Requirements Quality

- [ ] Scope is explicit.
- [ ] In-scope behavior is defined.
- [ ] Out-of-scope behavior is identified where relevant.
- [ ] Requirements are clear and sufficiently precise.
- [ ] Requirements are internally consistent.
- [ ] Material assumptions are documented.
- [ ] Dependencies are identified.
- [ ] Constraints are identified.
- [ ] Acceptance criteria are verifiable.
- [ ] Material ambiguities have been resolved.

---

## 4. Functional Behavior

- [ ] Primary behavior is defined.
- [ ] Alternative flows are considered.
- [ ] Error conditions are defined.
- [ ] Boundary conditions are considered.
- [ ] Relevant business rules are explicit.
- [ ] Expected behavior is distinguishable from implementation detail.

---

## 5. Quality Requirements

- [ ] Relevant quality characteristics have been considered.
- [ ] Performance requirements are defined where relevant.
- [ ] Reliability requirements are defined where relevant.
- [ ] Security requirements are defined where relevant.
- [ ] Maintainability considerations are addressed.
- [ ] Compatibility requirements are addressed where relevant.
- [ ] Operational requirements are addressed where relevant.
- [ ] Quality criteria are measurable or otherwise verifiable when necessary.

---

## 6. Security

- [ ] Authentication requirements were considered.
- [ ] Authorization requirements were considered.
- [ ] Sensitive data was identified.
- [ ] Secret handling was considered.
- [ ] Relevant trust boundaries were considered.
- [ ] Dependency risks were considered.
- [ ] Security verification is defined where required.
- [ ] Known blocking vulnerabilities are addressed or explicitly accepted.

---

## 7. Architecture

- [ ] Architectural impact was assessed.
- [ ] Relevant architectural decisions are documented.
- [ ] Significant trade-offs are recorded.
- [ ] Quality attributes with architectural impact were considered.
- [ ] Security architecture implications were considered.
- [ ] Existing architecture constraints are respected.
- [ ] Required ADRs have been created or updated.

---

## 8. Implementation

- [ ] Implementation tasks are traceable to requirements or decisions.
- [ ] Tasks are sufficiently defined.
- [ ] Dependencies between tasks are understood.
- [ ] Implementation does not silently redefine requirements.
- [ ] AI-generated artifacts were reviewed according to project policy.
- [ ] Relevant code review was completed.

---

## 9. Testing and Verification

- [ ] Appropriate test levels were identified.
- [ ] Unit tests exist where appropriate.
- [ ] Integration tests exist where appropriate.
- [ ] Acceptance verification covers relevant criteria.
- [ ] Security testing was performed where required.
- [ ] Quality-specific verification was performed where required.
- [ ] Regression impact was considered.
- [ ] Test results are available.
- [ ] Failed tests were analyzed rather than simply bypassed.

---

## 10. AI-Assisted Development

- [ ] AI usage complied with project policy.
- [ ] Sensitive information was handled appropriately.
- [ ] AI-generated requirements were validated.
- [ ] AI-generated architecture was reviewed where relevant.
- [ ] AI-generated code was reviewed according to risk.
- [ ] AI-generated tests were validated.
- [ ] AI-generated documentation was checked for accuracy.
- [ ] AI output did not introduce unsupported assumptions.

---

## 11. Traceability

- [ ] Intent is identifiable.
- [ ] Requirements are identifiable.
- [ ] Acceptance criteria are traceable where required.
- [ ] Architecture decisions are traceable where relevant.
- [ ] Tasks are traceable to governing artifacts.
- [ ] Tests provide evidence for relevant requirements.
- [ ] Release evidence is available.

Typical chain:

**Intent → Requirements → Specification → Architecture → Tasks → Implementation

→ Tests → Evidence → Release**

---

## 12. CI/CD

- [ ] Build succeeds.
- [ ] Required automated tests pass.
- [ ] Required quality checks pass.
- [ ] Required security checks pass.
- [ ] Dependency checks pass.
- [ ] Secret scanning passes.
- [ ] Artifact is identifiable and traceable.
- [ ] Deployment controls are satisfied.
- [ ] Rollback or recovery strategy exists where required.

---

## 13. Release Readiness

- [ ] Scope is complete or remaining scope is explicitly documented.
- [ ] Acceptance criteria are satisfied.
- [ ] Blocking defects are resolved or formally accepted.
- [ ] Security risks are resolved or formally accepted.
- [ ] Required quality evidence is available.
- [ ] Documentation is updated where required.
- [ ] Operational readiness is confirmed where applicable.
- [ ] Release approval is recorded.

---

## 14. Exceptions

Record any failed or waived item.

| Item | Reason | Risk | Compensating Control | Approver |
| --- | --- | --- | --- | --- |
| [Item] | [Reason] | [Risk] | [Control] | [Approver] |

---

## 15. Result

**Result:** [Passed / Passed with Exceptions / Not Ready]

**Summary:** [Short summary]

**Required Actions:**

- [Action]
- [Action]

---

## 16. Evidence

List the evidence supporting the checklist result.

- [Test report]
- [Security analysis]
- [Review record]
- [Build]
- [Release artifact]
- [Other evidence]

---

## 17. Approval

**Reviewer:** [Name / Role]

**Decision:** [Approved / Not Approved]

**Date:** [Date]

---

## 18. Ptilon Principle

A checklist is a quality gate, not a substitute for engineering judgment.

The checklist should identify missing evidence, unresolved risks, and quality

gaps. It should not be used as a mechanical scoring system detached from

project context.
