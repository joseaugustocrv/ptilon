# Threat Model Template

## 1. Purpose

This template defines the standard structure for identifying, analyzing,

mitigating, and tracking security threats associated with a software system or

change.

Threat modeling should be performed early enough to influence requirements,

architecture, and implementation.

---

## 2. System Metadata

- **System / Feature:** `<name>`
- **Specification:** `<path or reference>`
- **Architecture:** `<path or reference>`
- **Owner:** `<person/team>`
- **Date:** `<YYYY-MM-DD>`
- **Status:** `Draft | Reviewed | Accepted`

---

## 3. System Context

### Purpose

`<what the system or feature does>`

### Assets

Identify information, resources, and capabilities that require protection.

- `<asset>`
- `<asset>`

### Trust Boundaries

Identify boundaries between components, users, networks, services, or privilege

levels.

- `<boundary>`

### External Dependencies

- `<service>`
- `<API>`
- `<identity provider>`
- `<infrastructure component>`

---

## 4. Data Flows

Describe the relevant data flows between actors and components.

| Source | Destination | Data | Protocol / Interface | Trust Boundary |
| --- | --- | --- | --- | --- |
| `<source>` | `<destination>` | `<data>` | `<protocol>` | `<boundary>` |

Include authentication, authorization, sensitive data, and external

communication flows where applicable.

---

## 5. Threat Identification

Use a structured threat model such as STRIDE when appropriate.

| Threat | Category | Asset | Component / Flow | Description |
| --- | --- | --- | --- | --- |
| `<threat>` | `<STRIDE category>` | `<asset>` | `<component>` | `<description>` |

Typical STRIDE categories:

- Spoofing
- Tampering
- Repudiation
- Information Disclosure
- Denial of Service
- Elevation of Privilege

---

## 6. Risk Assessment

Assess each relevant threat using the project's approved risk method.

| Threat | Likelihood | Impact | Risk | Rationale |
| --- | --- | --- | --- | --- |
| `<threat>` | `Low/Medium/High` | `Low/Medium/High` | `<level>` | `<reason>` |

The risk method and thresholds should be consistent with the project's

security governance.

---

## 7. Mitigations

For each significant threat, define one or more controls.

| Threat | Mitigation | Requirement / Control | Owner | Status |
| --- | --- | --- | --- | --- |
| `<threat>` | `<control>` | `<reference>` | `<owner>` | `Planned/Implemented/Verified` |

Prefer preventive controls where appropriate, complemented by detection and

recovery mechanisms.

---

## 8. Security Requirements

Convert relevant mitigations into explicit, testable requirements.

| Requirement | Threat Addressed | Verification |
| --- | --- | --- |
| `<SEC-REQ-ID>` | `<threat>` | `<test/control>` |

Security requirements must be traceable to implementation and verification.

---

## 9. Residual Risk

Document threats that remain after mitigation.

| Threat | Residual Risk | Acceptance / Treatment |
| --- | --- | --- |
| `<threat>` | `<level>` | `<decision>` |

Residual risk acceptance must follow the project's governance and authorization

rules.

---

## 10. Verification

- [ ] Security requirements are implemented.
- [ ] Relevant security tests are defined.
- [ ] Authentication controls are verified.
- [ ] Authorization controls are verified.
- [ ] Input validation is verified where applicable.
- [ ] Sensitive data protection is verified.
- [ ] Logging and monitoring requirements are verified.
- [ ] Dependency and configuration risks are reviewed.
- [ ] Relevant findings are tracked to closure.

---

## 11. Change Impact

When modifying an existing system, identify whether the change affects:

- [ ] Assets
- [ ] Trust boundaries
- [ ] Data flows
- [ ] Authentication
- [ ] Authorization
- [ ] Sensitive data
- [ ] External dependencies
- [ ] Attack surface
- [ ] Existing mitigations

If any item changes materially, update the threat model.

---

## 12. Evidence

Record supporting evidence:

- Architecture diagrams
- Data-flow diagrams
- Security requirements
- Test results
- Scan reports
- Configuration reviews
- Code review references
- Relevant ADRs

References:

- `<evidence reference>`

---

## 13. AI Assistance

AI may assist with:

- Identifying candidate threats.
- Reviewing data flows and trust boundaries.
- Suggesting STRIDE categories.
- Identifying missing security requirements.
- Reviewing mitigation coverage.
- Generating candidate security test scenarios.

AI-generated threat analysis must be validated by qualified reviewers and must

not be treated as a complete security assessment by itself.

---

## 14. Review

- **Security reviewer:** `<person/team>`
- **Engineering reviewer:** `<person/team>`
- **Review date:** `<YYYY-MM-DD>`
- **Next review:** `<YYYY-MM-DD or trigger>`

Review is required when significant architecture, data flow, trust boundary,

authentication, authorization, or attack-surface changes occur.

---

## 15. Principles

Ptilon threat modeling follows these principles:

1. Security threats are considered during design, not only after implementation.
2. Threats are derived from concrete assets, components, data flows, and trust
   boundaries.
3. Security requirements must be testable and traceable.
4. Significant residual risks must be explicitly documented and governed.
5. Threat models evolve with the system.
6. AI accelerates threat discovery but does not replace security engineering
   judgment.
