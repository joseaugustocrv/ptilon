# Release Checklist — User Profile API Example

## 1. Purpose

This checklist defines the minimum verification required before releasing
the User Profile API example.

## 2. Specification

- [ ] Requirements are documented in `specification.md`.
- [ ] Acceptance criteria are defined and testable.
- [ ] Requirement-to-test traceability is complete.
- [ ] No unresolved requirement ambiguity remains.

## 3. Architecture

- [ ] The implementation follows the boundaries defined in
  `architecture.md`.
- [ ] Authentication and authorization responsibilities are preserved.
- [ ] Data ownership rules are enforced server-side.
- [ ] Any material architectural deviation has been documented through
  an ADR.

## 4. Implementation

- [ ] All tasks in `tasks.md` are completed.
- [ ] Profile retrieval works for authenticated users.
- [ ] Permitted profile updates work correctly.
- [ ] Unauthorized cross-user access is rejected.
- [ ] Input validation is enforced.
- [ ] Protected fields cannot be modified through unsupported requests.
- [ ] Error handling follows the defined API behavior.

## 5. Testing

- [ ] Unit tests pass.
- [ ] Integration tests pass.
- [ ] API tests pass.
- [ ] Negative tests pass.
- [ ] Security tests pass.
- [ ] Acceptance criteria have been verified.
- [ ] No known critical or high-severity defect remains unresolved.
- [ ] Test results are reproducible.

## 6. Security

- [ ] Authentication is enforced for protected operations.
- [ ] Authorization is based on server-side ownership rules.
- [ ] Input validation is active.
- [ ] Sensitive data is not unnecessarily exposed in responses.
- [ ] Sensitive data is not unnecessarily exposed in logs.
- [ ] Error responses do not expose implementation details or secrets.
- [ ] Threat-model controls have been verified.

## 7. Observability

- [ ] Relevant application failures can be diagnosed.
- [ ] Diagnostic information does not expose sensitive data.
- [ ] Required operational logging or telemetry is available.
- [ ] Failure conditions can be correlated with the affected operation
  where supported.

## 8. Compatibility

- [ ] API behavior matches the defined contract.
- [ ] Existing supported behavior has not been unintentionally changed.
- [ ] Response structures remain compatible with documented consumers.
- [ ] Any intentional breaking change has been explicitly documented.

## 9. Documentation

- [ ] API behavior is documented.
- [ ] Security expectations are documented.
- [ ] Relevant configuration is documented.
- [ ] Test and verification evidence is available.
- [ ] Material implementation decisions are recorded.

## 10. Release Decision Record

**Release candidate:** ____________________

**Version:** ____________________

**Verification date:** ____________________

**Verified by:** ____________________

**Open issues / exceptions:**

- ______________________________________
- ______________________________________

**Release status:**

- [ ] Ready for release
- [ ] Not ready for release

Any exception to this checklist shall be explicitly documented with its
rationale, impact, owner, and follow-up action.
