# NIST SSDF — Secure Software Development Framework

## 1. Purpose

Document how the NIST Secure Software Development Framework (SSDF) is used as
the primary secure software development reference within Ptilon.

This document provides a Ptilon interpretation and does not reproduce the NIST
publication.

---

## 2. Reference

NIST SP 800-218 — Secure Software Development Framework (SSDF) Version 1.1

Official reference: <https://csrc.nist.gov/pubs/sp/800/218/final>

SSDF provides a core set of secure software development practices that can be
integrated into any software development lifecycle.

---

## 3. Role in Ptilon

Ptilon uses SSDF to integrate security into the software lifecycle rather than
treating security as a final inspection activity.

The SSDF practices complement:

- ISO/IEC/IEEE 12207 for lifecycle processes;
- ISO/IEC/IEEE 29148 for requirements engineering;
- ISO/IEC/IEEE 42010 for architecture;
- ISO/IEC 25010 for product quality.

---

## 4. SSDF practice groups

SSDF organizes practices into four groups:

### PO — Prepare the Organization

Establish organizational capabilities and practices needed to develop secure
software.

Relevant concerns include:

- security roles and responsibilities;
- secure development policies;
- development environments;
- security awareness;
- risk management.

### PS — Protect the Software

Protect software and development artifacts from unauthorized access or
modification.

Relevant concerns include:

- source code protection;
- build environments;
- credentials and secrets;
- software components;
- release artifacts.

### PW — Produce Well-Secured Software

Integrate security practices into software development.

Relevant concerns include:

- security requirements;
- secure architecture and design;
- secure coding;
- security testing;
- vulnerability prevention;
- verification.

### RV — Respond to Vulnerabilities

Identify, assess, and respond to vulnerabilities.

Relevant concerns include:

- vulnerability reporting;
- analysis;
- remediation;
- mitigation;
- communication;
- lessons learned.

---

## 5. Integration with Ptilon

Ptilon maps SSDF concerns across the lifecycle:

| Ptilon activity | Security contribution |
| --- | --- |
| Constitution | Security principles, policies, roles, constraints |
| Specify | Security requirements |
| Clarify | Security ambiguity and risk resolution |
| Plan | Security verification and implementation planning |
| Checklist | Security readiness |
| Tasks | Security work decomposition |
| Analyze | Threats, vulnerabilities, dependencies, and impact |
| Implement | Secure coding and protected development |
| Converge | Security verification and remediation |
| Review | Security evidence and risk review |
| Release | Secure release controls |
| Evolution | Vulnerability response and security maintenance |

This mapping is conceptual. Project-specific controls should be selected
according to risk and context.

---

## 6. Security requirements

Security requirements should be explicit when relevant.

Examples include:

- authentication;
- authorization;
- least privilege;
- confidentiality;
- integrity;
- availability;
- secure session management;
- auditability;
- data protection;
- secure configuration;
- abuse prevention.

Security requirements should have verifiable acceptance criteria whenever
practical.

---

## 7. Secure architecture and design

Security should be considered before implementation when architectural decisions
affect the security posture.

Relevant analysis may include:

- trust boundaries;
- attack surfaces;
- data flows;
- identity and access;
- external interfaces;
- secrets;
- isolation;
- logging;
- recovery;
- dependency risks.

Architectural security decisions should be documented when significant.

---

## 8. Secure implementation

Implementation should apply appropriate secure development practices.

Examples include:

- input validation;
- output encoding where applicable;
- secure error handling;
- least privilege;
- safe dependency management;
- secret management;
- secure configuration;
- protection against known vulnerability classes;
- code review;
- automated security analysis.

Security controls should be appropriate to the technology and threat model.

---

## 9. AI-assisted secure development

AI can assist with:

- security requirement drafting;
- threat identification;
- secure coding suggestions;
- security test generation;
- dependency analysis;
- code review support;
- vulnerability analysis;
- remediation guidance.

AI-generated security artifacts require human validation.

Particular attention should be given to:

- insecure generated code;
- hallucinated security guarantees;
- incomplete threat analysis;
- unsafe dependencies;
- inappropriate cryptographic recommendations;
- exposed secrets;
- missing authorization controls.

AI should not be treated as a security authority.

---

## 10. Software supply chain

The software supply chain should be treated as part of the security boundary.

Projects should consider, as applicable:

- dependency provenance;
- version control;
- vulnerability scanning;
- component updates;
- build integrity;
- artifact integrity;
- third-party services;
- generated code;
- development tooling.

Controls should reflect the project's risk and operational context.

---

## 11. Vulnerability management

Vulnerabilities should follow a controlled lifecycle:

Identify → Assess → Prioritize → Remediate/Mitigate → Verify → Record

Records should provide enough information to understand:

- affected component;
- vulnerability;
- severity or risk;
- treatment decision;
- remediation;
- residual risk;
- verification evidence.

---

## 12. Security verification

Security verification should be integrated with normal engineering verification.

Depending on context, it may include:

- static analysis;
- dependency analysis;
- secret scanning;
- security unit tests;
- integration tests;
- authentication and authorization tests;
- penetration testing;
- configuration verification;
- infrastructure checks.

Not every project requires every technique.

---

## 13. Security evidence

Security activities should produce evidence proportional to risk.

Examples include:

- security requirements;
- threat models;
- architecture decisions;
- automated scan results;
- test results;
- vulnerability records;
- remediation evidence;
- release checks.

Evidence should remain traceable to relevant requirements, risks, changes, or
releases when appropriate.

---

## 14. Release and operational security

Before release, applicable security controls should be verified.

Consider:

- unresolved vulnerabilities;
- secure configuration;
- secrets;
- dependencies;
- deployment controls;
- monitoring;
- logging;
- rollback;
- incident response readiness.

Security requirements that cannot be satisfied should result in an explicit
risk decision rather than an implicit omission.

---

## 15. Conformance

Using NIST SSDF as a reference does not by itself establish conformance to the
framework.

Projects should distinguish between:

- using SSDF as guidance;
- adopting selected SSDF practices;
- establishing organizational SSDF controls;
- making a formal compliance or conformance claim under an external
  requirement.

Claims should be supported by appropriate evidence.

---

## 16. Ptilon implications

SSDF establishes several principles for Ptilon:

1. security is a lifecycle concern;
2. secure development requires organizational and technical practices;
3. security requirements should be explicit;
4. secure architecture and implementation should be verified;
5. software supply chain risks must be considered;
6. vulnerabilities require controlled response;
7. AI-generated security artifacts require human validation;
8. security evidence should be proportional to risk.

---

## 17. References

- NIST SP 800-218 — Secure Software Development Framework (SSDF):
  <https://csrc.nist.gov/pubs/sp/800/218/final>
- NIST SSDF project: <https://csrc.nist.gov/Projects/ssdf>
- Ptilon Security: `docs/security/README.md`
- Ptilon Standards: `docs/standards/README.md`
- Ptilon Methodology: `docs/methodology/README.md`

---

## 18. Status

This document defines the role of NIST SSDF as the primary secure software
development reference within Ptilon.

It should be reviewed when NIST publishes a materially revised SSDF or when
Ptilon's security methodology is materially revised.
