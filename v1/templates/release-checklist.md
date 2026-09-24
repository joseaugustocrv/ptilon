# Release Checklist Template

## 1. Purpose

This checklist defines the minimum verification required before releasing a
software change.

A release must be traceable to an approved specification, verified against its
acceptance criteria, and evaluated for quality, security, operational
readiness, and rollback capability.

---

## 2. Release Metadata

- **Release:** `<name/version>`
- **Specification:** `<path or reference>`
- **Change / Feature:** `<name>`
- **Release owner:** `<person/team>`
- **Target environment:** `<environment>`
- **Planned release date:** `<YYYY-MM-DD>`
- **Status:** `Planned | Ready | Released | Rolled Back`

---

## 3. Specification and Scope

- [ ] Specification is approved.
- [ ] Scope is clearly identified.
- [ ] Acceptance criteria are defined.
- [ ] Changes from the approved specification are documented.
- [ ] Out-of-scope items are explicitly recorded.
- [ ] Traceability to requirements is complete.

---

## 4. Implementation

- [ ] All planned tasks are completed.
- [ ] Code review is completed.
- [ ] Required architectural decisions are documented.
- [ ] Database or schema changes are reviewed.
- [ ] Configuration changes are documented.
- [ ] Dependencies and version changes are recorded.

---

## 5. Testing

- [ ] Unit tests pass.
- [ ] Integration tests pass.
- [ ] System tests pass where applicable.
- [ ] Acceptance tests pass.
- [ ] Regression tests pass.
- [ ] Relevant non-functional tests pass.
- [ ] Security tests are completed where applicable.
- [ ] Known test limitations are documented.
- [ ] Test evidence is retained.

**Test plan:** `<path or reference>`

---

## 6. Quality

- [ ] Quality requirements have been verified.
- [ ] Critical defects are resolved or formally accepted.
- [ ] No unexplained test failures remain.
- [ ] Code quality checks pass.
- [ ] Static analysis checks pass where applicable.
- [ ] Observability requirements are satisfied.
- [ ] Technical debt introduced by the change is documented.

---

## 7. Security

- [ ] Security requirements have been verified.
- [ ] Secrets are not present in source control.
- [ ] Access permissions are appropriate.
- [ ] Dependencies have been checked for relevant vulnerabilities.
- [ ] Security-sensitive configuration has been reviewed.
- [ ] Threat-model changes have been assessed where applicable.

---

## 8. Deployment Readiness

- [ ] Deployment procedure is documented.
- [ ] Required infrastructure is available.
- [ ] Required configuration is available.
- [ ] Required migrations are prepared and ordered correctly.
- [ ] Deployment dependencies are identified.
- [ ] Deployment can be monitored.
- [ ] Rollback procedure is documented and viable.

---

## 9. Data and Migration

- [ ] Data migration is required: `Yes | No`
- [ ] Migration has been tested where applicable.
- [ ] Backup requirements are satisfied.
- [ ] Data integrity checks are defined.
- [ ] Backward compatibility has been assessed.
- [ ] Rollback implications for data have been assessed.

---

## 10. Operational Readiness

- [ ] Logs are available and useful.
- [ ] Metrics are available where required.
- [ ] Alerts are configured where required.
- [ ] Health checks are available.
- [ ] Runbook or operational documentation is updated.
- [ ] Support team has required information.
- [ ] Known operational risks are documented.

---

## 11. Communication

- [ ] Release scope has been communicated to relevant stakeholders.
- [ ] Known limitations are communicated.
- [ ] User-facing changes are documented where applicable.
- [ ] Operational changes are communicated where applicable.
- [ ] Support and escalation contacts are identified.

---

## 12. Rollback

### Rollback Trigger

Define the conditions that require rollback.

- `<condition>`

### Rollback Procedure

1. `<step>`
2. `<step>`
3. `<step>`

### Rollback Verification

- [ ] Application is restored to the expected state.
- [ ] Data integrity is verified.
- [ ] Critical functionality is available.
- [ ] Monitoring confirms system stability.

---

## 13. Final Approval

- **Technical approval:** `<person/team>`
- **Quality approval:** `<person/team>`
- **Security approval:** `<person/team>` (if applicable)
- **Business/product approval:** `<person/team>` (if applicable)
- **Approval date:** `<YYYY-MM-DD>`

### Release Decision

`Approved | Approved with Exceptions | Not Approved`

Exceptions:

- `<exception>`

---

## 14. Post-Release Verification

- [ ] Deployment completed successfully.
- [ ] Health checks passed.
- [ ] Critical user journeys were verified.
- [ ] Monitoring shows expected behavior.
- [ ] No unexpected critical errors were detected.
- [ ] Release evidence was retained.
- [ ] Follow-up actions were recorded.

---

## 15. AI Assistance

AI may assist with:

- Reviewing the checklist against the specification.
- Identifying missing release activities.
- Generating deployment and rollback checklists.
- Reviewing configuration and dependency changes.
- Identifying potential operational risks.

AI-generated recommendations must be validated by the responsible engineering
and operational teams before release approval.

---

## 16. Principles

Ptilon release readiness follows these principles:

1. No release without traceability to approved requirements.
2. Verification precedes deployment.
3. Security and operational readiness are release concerns, not post-release
   activities.
4. Every production change must have a viable rollback or documented recovery
   strategy.
5. Exceptions must be explicit and traceable.
6. Release evidence must be retained.
7. AI assists release preparation but does not replace accountable approval.
