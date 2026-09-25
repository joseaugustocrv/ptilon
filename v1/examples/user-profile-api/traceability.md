# Traceability Matrix — User Profile API Example

This matrix connects requirements, acceptance criteria, architecture,
implementation tasks, tests, and security controls.

| ID | Unit | Requirement / Control | Acceptance Criteria | Architecture | Tasks | Test Plan | Threat Model |
| --- | --- | --- | --- | --- | --- | --- | --- |
| REQ-001 | `user-profile` | Retrieve own profile | ACC-001 | Profile Service, Authorization, Repository | TSK-001 | TST-001 | THR-001, THR-002 |
| REQ-002 | `user-profile` | Update permitted profile fields | ACC-002 | Profile Service, Validation, Repository | TSK-002 | TST-002 | THR-006 |
| REQ-003 | `user-profile` | Prevent access to another user's profile | ACC-003 | Authorization | TSK-003 | TST-003 | THR-001 |
| REQ-004 | `user-profile` | Validate profile input | ACC-004 | Validation | TSK-002, TSK-005 | TST-004 | THR-003 |
| REQ-005 | `user-profile` | Require authentication | ACC-005 | Authentication Context | TSK-001, TSK-003 | TST-005 | THR-002 |
| REQ-006 | `user-profile` | Handle expected errors consistently | ACC-004, ACC-005, ACC-007 | API Layer, Profile Service, API Contract | TSK-004 | TST-008 | — |
| SEC-001 | `user-profile` | Enforce ownership authorization | ACC-003 | Authorization | TSK-003, TSK-005 | TST-003 | THR-001 |
| SEC-002 | `user-profile` | Protect sensitive data | ACC-006 | API Layer, Repository | TSK-005 | TST-006 | THR-004 |
| SEC-003 | `user-profile` | Validate untrusted input | ACC-004 | Validation | TSK-005 | TST-004 | THR-003 |
| QLT-001 | `user-profile` | Maintain automated testability | ACC-008 | All relevant components | TSK-006 | TST-009 | — |
| QLT-002 | `user-profile` | Provide observability | ACC-007 | API Layer, observability mechanism | TSK-006, TSK-007 | TST-007 | THR-005 |
| QLT-003 | `user-profile` | Preserve compatibility | ACC-009 | API Layer, API Contract | TSK-007 | TST-010 | — |

## Artifact Dependencies

```text
specification.md
      │
      ├──> api-contract.md
      │
      ├──> architecture.md
      │
      ├──> tasks.md
      │       │
      │       └──> implementation
      │
      ├──> test-plan.md
      │       │
      │       └──> verification evidence
      │
      └──> threat-model.md
              │
              └──> security verification

implementation + tests + security verification
                    │
                    └──> release-checklist.md
```

## Traceability Rules

1. Every functional requirement shall map to at least one acceptance
   criterion.
2. Every acceptance criterion shall have a defined verification method,
   preferably identified by a `TST-###` when repeatable verification is
   applicable.
3. Security requirements shall map to both implementation controls and
   security tests.
4. Material architectural decisions shall be traceable to the affected
   requirements.
5. Tasks shall identify the requirements or controls they implement.
6. Release readiness shall be based on verified requirements, tests, and
   security controls.
7. A change to a requirement shall trigger an impact review across dependent
   architecture, tasks, tests, and release evidence.

## Change Impact

When a requirement changes, review at minimum:

- affected acceptance criteria;
- affected architectural components;
- affected implementation tasks;
- affected tests;
- affected threat-model controls;
- affected documentation;
- release-readiness evidence.

Traceability is considered complete only when each applicable requirement can
be followed from specification through implementation and verification.
