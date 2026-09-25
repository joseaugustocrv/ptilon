# Example: User Profile API

## 1. Scenario

This example demonstrates the Ptilon documentary workflow for adding a REST API
capability that allows an authenticated user to retrieve and update their own
profile.

The example is intentionally small so that the relationships between
specification, architecture, tasks, testing, security, traceability, and release
artifacts remain visible.

---

## 2. Scope

The feature provides:

- Retrieval of the authenticated user's profile.
- Update of permitted profile fields.
- Validation of submitted data.
- Authorization so a user can access only their own profile.
- Authentication for protected profile operations.
- Documented error handling.
- Protection of sensitive authentication information.
- Automated verification.

Out of scope:

- User registration.
- Password management.
- Administrative profile management.
- Profile deletion.

---

## 3. Engineering Unit

**Unit:** `user-profile`

This example represents one engineering unit. Its requirements and specification
describe the unit's coherent scope.

Architecture, tasks, test planning, security analysis, and release artifacts are
shown as shared downstream artifacts for this example. A larger project may add
other engineering units without automatically duplicating those artifacts.

---

## 4. Workflow Demonstrated

```text
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

## 5. Example Artifacts

The complete example contains:

```text
examples/user-profile-api/
├── README.md
├── specification.md
├── api-contract.md
├── architecture.md
├── plan.md
├── tasks.md
├── test-plan.md
├── verification.md
├── threat-model.md
├── traceability.md
├── definition-of-done.md
└── release-checklist.md
```

Each artifact remains traceable to the requirements defined in the
specification.

---

## 6. Requirements

### REQ-001 — Retrieve Own Profile

The system shall provide an authenticated operation that returns the profile
associated with the authenticated user.

### REQ-002 — Update Own Profile

The system shall provide an authenticated operation that updates only profile
fields explicitly permitted by the API contract.

### REQ-003 — Authorization

The system shall prevent an authenticated user from retrieving or modifying
another user's profile.

### REQ-004 — Input Validation

The system shall validate profile update input according to the validation rules
defined by the API contract.

Invalid input shall not modify the stored profile.

### REQ-005 — Authentication

Profile operations shall require an authenticated user.

Unauthenticated requests shall be rejected according to the API authentication
contract.

### REQ-006 — Error Handling

The API shall return documented error responses for applicable authentication,
authorization, validation, and resource failures.

### Security Requirements

- **SEC-001:** Authorization shall be evaluated using the authenticated user's
  identity and shall prevent access to another user's profile.
- **SEC-002:** Credentials, secrets, authentication tokens, and other sensitive
  security data shall not be exposed through the profile API.
- **SEC-003:** Untrusted profile input shall be validated before persistence.

### Quality Requirements

- **QLT-001:** The API behavior defined by the functional and security
  requirements shall be covered by automated tests.
- **QLT-002:** Operationally relevant failures shall generate sufficient
  diagnostic information without exposing sensitive data.
- **QLT-003:** The API shall preserve the documented request and response
  contract for the supported version.

---

## 7. Acceptance Criteria

### ACC-001 — Retrieve Profile

Given an authenticated user with an existing profile, when the user requests
their profile, the API returns the profile associated with that authenticated
identity.

### ACC-002 — Update Profile

Given an authenticated user with an existing profile, when the user submits valid
permitted profile data, the API persists the update and returns the documented
response.

### ACC-003 — Prevent Cross-User Access

Given an authenticated user, when the request attempts to access another user's
profile, the API denies the operation.

### ACC-004 — Reject Invalid Input

Given an authenticated user, when invalid profile data is submitted, the API
rejects the request and does not persist the invalid data.

### ACC-005 — Reject Unauthenticated Access

Given an unauthenticated request, when a profile operation is attempted, the API
rejects the request according to the authentication contract.

### ACC-006 — Protect Sensitive Data

Given any successful profile response, sensitive authentication information is
not included in the response.

### ACC-007 — Return Consistent Error Responses

Given an applicable authentication, authorization, validation, resource, or
processing failure, the API returns the documented error structure and status
without exposing unnecessary implementation details or sensitive information.

### ACC-008 — Maintain Automated Verification Coverage

Given the approved functional and security acceptance criteria, each applicable
criterion has an automated verification scenario.

### ACC-009 — Preserve API Compatibility

Given the supported API version, documented request and response behavior remains
compatible with the approved API contract unless an intentional breaking change
is explicitly approved.

---

## 8. Traceability Example

| Requirement | Acceptance Criteria | Task | Test |
| --- | --- | --- | --- |
| REQ-001 | ACC-001 | TSK-001 | TST-001 |
| REQ-002 | ACC-002 | TSK-002 | TST-002 |
| REQ-003 | ACC-003 | TSK-003 | TST-003 |
| REQ-004 | ACC-004 | TSK-002 | TST-004 |
| REQ-005 | ACC-005 | TSK-001 | TST-005 |
| REQ-006 | ACC-004, ACC-005, ACC-007 | TSK-004 | TST-008 |
| SEC-001 | ACC-003 | TSK-003, TSK-005 | TST-003 |
| SEC-002 | ACC-006 | TSK-005 | TST-006 |
| SEC-003 | ACC-004 | TSK-002, TSK-005 | TST-004 |
| QLT-001 | ACC-008 | TSK-006 | TST-009 |
| QLT-002 | ACC-007 | TSK-006, TSK-007 | TST-007 |
| QLT-003 | ACC-009 | TSK-007 | TST-010 |

---

## 9. Implementation Readiness

Before implementation, this example demonstrates the Ptilon
`Implementation Ready` state:

- requirements are approved and traceable;
- acceptance criteria are observable;
- architecture and significant decisions are documented;
- the plan establishes sequencing and dependencies;
- tasks identify objectives, sources, completion criteria, and verification;
- security and quality controls have verification methods;
- no material question remains unresolved.

## 10. Engineering Notes

The implementation should explicitly address:

- Authentication context.
- Authorization boundaries.
- Input validation.
- Error handling.
- Protection of sensitive information.
- Automated tests.
- Operational observability.

Any architectural decision beyond the existing project architecture should be
documented through an ADR.

---

## 11. Ptilon Demonstration

This example illustrates several core Ptilon principles:

1. Requirements are defined before implementation.
2. Acceptance criteria are testable.
3. Security behavior is part of the specification.
4. Tasks are traceable to requirements.
5. Tests are traceable to requirements and acceptance criteria.
6. Architecture remains connected to requirements.
7. Security analysis contributes to requirements and verification.
8. AI can assist each engineering activity without becoming the authority for
   the requirements.
9. Final convergence verifies the complete chain before release.
