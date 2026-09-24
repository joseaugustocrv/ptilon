# Bug Report Template

## 1. Purpose

This template defines the standard structure for reporting, analyzing, reproducing,
resolving, and verifying software defects.

A bug report should describe observable behavior and provide enough evidence to support independent reproduction.

---

## 2. Bug Metadata

- **Bug ID:** `<BUG-ID>`
- **Title:** `<short title>`
- **Reported by:** `<person/team>`
- **Date:** `<YYYY-MM-DD>`
- **Environment:** `<environment>`
- **Version / Build:** `<version>`
- **Status:** `New | Triaged | In Progress | Resolved | Verified | Closed`

---

## 3. Related Artifacts

- **Specification:** `<path or reference>`
- **Requirement:** `<REQ-ID>`
- **Acceptance criterion:** `<ACC-ID>`
- **Test:** `<TST-ID>`
- **Change request:** `<CR-ID>` if applicable
- **Release:** `<release>` if applicable

---

## 4. Summary

Describe the observed problem in one or two precise sentences.

`<summary>`

---

## 5. Expected Behavior

Describe what should happen according to the approved specification or acceptance criteria.

`<expected behavior>`

---

## 6. Actual Behavior

Describe what actually happened.

`<actual behavior>`

---

## 7. Reproduction

### Preconditions

- `<condition>`

### Steps

1. `<step>`
2. `<step>`
3. `<step>`

### Reproduction Result

`<result>`

### Reproducibility

`Always | Frequent | Intermittent | Unable to Reproduce`

---

## 8. Evidence

Attach or reference objective evidence where available:

- Logs
- Screenshots
- Recordings
- Error messages
- Stack traces
- Request / response samples
- Test execution results
- Monitoring data

References:

- `<evidence>`

Do not include secrets or unnecessary personal data in evidence.

---

## 9. Impact

Describe the observable impact.

- **Affected functionality:** `<functionality>`
- **Affected users / components:** `<scope>`
- **Business impact:** `<impact>`
- **Technical impact:** `<impact>`

### Severity

`Blocker | Critical | Major | Minor | Trivial`

Severity should follow the project's approved classification criteria.

---

## 10. Initial Analysis

### Suspected Cause

`<cause or hypothesis>`

### Supporting Evidence

`<evidence>`

### Related Components

- `<component>`

Do not present an unverified hypothesis as the confirmed root cause.

---

## 11. Resolution

### Root Cause

`<confirmed root cause>`

### Corrective Action

`<implemented correction>`

### Preventive Action

`<additional action to reduce recurrence>`

### Implementation Reference

`<commit / PR / change reference>`

---

## 12. Verification

- [ ] Original reproduction steps no longer fail.
- [ ] Expected behavior is verified.
- [ ] Relevant regression tests pass.
- [ ] New tests were added where appropriate.
- [ ] Related acceptance criteria remain satisfied.
- [ ] No unintended behavior was introduced.
- [ ] Evidence was retained.

**Verification reference:** `<test/report>`

---

## 13. Closure

- **Verified by:** `<person/team>`
- **Verification date:** `<YYYY-MM-DD>`
- **Release containing fix:** `<release>`
- **Final status:** `Verified | Closed`

---

## 14. AI Assistance

AI may assist with:

- Structuring bug reports.
- Identifying missing reproduction information.
- Suggesting candidate causes.
- Generating regression test scenarios.
- Reviewing consistency with specifications and acceptance criteria.

AI-generated hypotheses must be validated through evidence and reproducible technical analysis.

---

## 15. Principles

Ptilon defect management follows these principles:

1. Describe observable behavior before proposing causes.
2. Compare actual behavior with approved requirements and acceptance criteria.
3. Preserve objective reproduction evidence.
4. Distinguish hypotheses from confirmed root causes.
5. Verify fixes against the original defect and relevant regression scenarios.
6. Maintain traceability from defect to requirement, implementation, and verification.
7. Use AI to accelerate analysis without treating generated hypotheses as facts.
