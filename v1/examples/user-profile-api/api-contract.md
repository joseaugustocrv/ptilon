# User Profile API Contract

This document is the authoritative API contract for the User Profile API
example. It supplies the concrete interface details intentionally delegated by
the specification.

## 1. Authentication

Protected operations require a valid authenticated user context. The contract
does not prescribe the identity-provider technology.

## 2. Operations

| Operation | Method | Path | Purpose |
| --- | --- | --- | --- |
| Retrieve profile | GET | `/v1/profile` | Retrieve the authenticated user's profile |
| Update profile | PATCH | `/v1/profile` | Update permitted profile fields |

The authenticated identity determines the profile resource. A client must not
select another user's identity as an authorization mechanism.

## 3. Profile Representation

The response contains only the profile fields defined by the application.
Credentials, authentication tokens, secrets, and other sensitive security data
are excluded.

## 4. Update Rules

Only explicitly permitted profile fields may be updated. Input is validated before
persistence. Invalid input does not modify stored profile data.

## 5. Error Contract

| Condition | HTTP Status |
| --- | --- |
| Missing or invalid authentication | `401` |
| Authenticated but not authorized | `403` |
| Invalid request data | `400` |
| Profile not found where applicable | `404` |
| Unexpected processing failure | `500` |

Error responses use a consistent JSON structure with a machine-readable error
code and human-readable message. Internal implementation details and sensitive
data must not be exposed.

## 6. Compatibility

The `/v1` path identifies the supported contract version. Changes that alter
request or response semantics require impact analysis and an approved change.

## 7. Traceability

The contract realizes `REQ-001` through `REQ-006`, `SEC-001` through `SEC-003`,
and `QLT-003`. It is reviewed against the specification and architecture before
implementation.
