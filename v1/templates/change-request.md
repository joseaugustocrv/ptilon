# Change Request Template

## 1. Purpose

This template defines the standard structure for proposing, evaluating,
approving, and tracking changes to an approved specification, implementation,
architecture, or release scope.

Changes must be traceable to their origin, impact assessment, decision, and
resulting artifacts.

---

## 2. Change Metadata

- **Change ID:** `CHG-001`
- **Title:** `<short title>`
- **Related specification:** `<path or reference>`
- **Related issue:** `<issue/reference>`
- **Requester:** `<person/team>`
- **Date:** `<YYYY-MM-DD>`
- **Status:** `Proposed | Analyzed | Approved | Rejected | Implemented | Closed`

---

## 3. Change Description

**Affected Engineering Units:** `<unit names / keys>`

### Current State

Describe the currently approved behavior or design.

### Requested Change

Describe precisely what should change.

### Reason

Explain the business, technical, security, quality, or operational reason for
the change.

---

## 4. Impact Analysis

Evaluate the effect on:

- Requirements
- Architecture
- Data
- APIs and integrations
- Security
- Performance
- Testing
- Operations
- Documentation
- Schedule / delivery scope
- Dependencies

### Impact Summary

`Low | Medium | High`

Rationale:

`<analysis>`

---

## 5. Specification Impact

Identify affected requirements and acceptance criteria.

| Artifact | Identifier | Impact |
| --- | --- | --- |
| Requirement | `<REQ-ID>` | `<description>` |
| Acceptance criterion | `<ACC-ID>` | `<description>` |

If the change modifies approved requirements, the specification must be updated
before implementation proceeds.

---

## 6. Alternatives Considered

### Alternative A

`<description>`

**Advantages:** `<advantages>`

**Disadvantages:** `<disadvantages>`

### Alternative B

`<description>`

**Advantages:** `<advantages>`

**Disadvantages:** `<disadvantages>`

---

## 7. Recommended Implementation

Describe the implementation approach that will be evaluated for approval.

`<approach>`

Related architecture decisions:

- `<ADR reference>`

---

## 8. Security and Quality Assessment

Identify changes to:

- Security controls
- Threat model
- Authentication / authorization
- Data protection
- Quality attributes
- Reliability
- Performance
- Observability

Required actions:

- `<action>`

---

## 9. Testing Impact

Identify tests that must be added, modified, or repeated.

- Unit tests: `<impact>`
- Integration tests: `<impact>`
- Acceptance tests: `<impact>`
- Regression tests: `<impact>`
- Security tests: `<impact>`
- Other: `<impact>`

---

## 10. Documentation Impact

Artifacts requiring updates:

- [ ] Specification
- [ ] Architecture documentation
- [ ] ADR
- [ ] API documentation
- [ ] User documentation
- [ ] Operational documentation
- [ ] Test plan
- [ ] Release documentation
- [ ] Other: `<artifact>`

---

## 11. Decision

- **Decision:** `Approved | Rejected | Deferred`
- **Decision date:** `<YYYY-MM-DD>`
- **Decision owner:** `<person/team>`
- **Rationale:** `<reason>`

Conditions or constraints:

- `<condition>`

---

## 12. Implementation and Verification

- [ ] Specification updated.
- [ ] Architecture updated where required.
- [ ] Implementation completed.
- [ ] Tests updated.
- [ ] Regression verification completed.
- [ ] Documentation updated.
- [ ] Release impact assessed.
- [ ] Change evidence retained.

---

## 13. Closure

- **Implementation reference:** `<commit/PR/release>`
- **Verification reference:** `<test report>`
- **Release reference:** `<release>`
- **Closed by:** `<person/team>`
- **Closure date:** `<YYYY-MM-DD>`

---

## 14. AI Assistance

AI may assist with:

- Identifying impacted requirements and artifacts.
- Performing preliminary impact analysis.
- Proposing alternatives.
- Identifying missing tests and documentation.
- Reviewing consistency between the change and existing specifications.

AI-generated analysis is advisory. The change must be reviewed and approved by
accountable human stakeholders.

---

## 15. Principles

Ptilon change management follows these principles:

1. Every significant change must be traceable.
2. Approved specifications are changed deliberately, not implicitly.
3. Impact is assessed before implementation.
4. Changes to requirements trigger corresponding updates to verification and
   documentation.
5. Security and quality impacts are explicitly assessed.
6. Decisions and exceptions are recorded.
7. AI assists analysis but does not authorize changes.
