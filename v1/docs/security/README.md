# Security

Security is an engineering concern throughout the software lifecycle.

Ptilon integrates security into requirements, architecture, implementation,
verification, release, and governance rather than treating it solely as a
final validation activity.

## Security Lifecycle

```text
Security Requirements
        ↓
Threat Modeling
        ↓
Security Architecture
        ↓
Secure Implementation
        ↓
Security Testing
        ↓
Security Verification
        ↓
Release Security Gate
        ↓
Operational Feedback
```

## Core Practices

Security activities should include, according to project risk:

- security requirements;
- threat modeling;
- secure architecture review;
- secure coding practices;
- dependency and supply-chain analysis;
- authentication and authorization analysis;
- input validation;
- secrets management;
- security testing;
- vulnerability management;
- security verification evidence.

## Threat Modeling

Threat modeling should identify:

- assets;
- trust boundaries;
- threats;
- attack surfaces;
- security controls;
- residual risks.

The methodology may use established threat-modeling techniques
appropriate to the system and risk profile.

## Application Security Verification

For application security verification, Ptilon references the OWASP
Application Security Verification Standard (ASVS).

See the [OWASP Application Security Verification Standard (ASVS)](https://owasp.org/projects/asvs).

ASVS provides a basis for defining and verifying application security
requirements according to the application's security needs.

## Secure Software Development

Ptilon also references the NIST Secure Software Development Framework
(SSDF) as a foundation for integrating secure development practices into
the software lifecycle.

See `references/security/nist-ssdf.md`.

## Security Requirements

Security requirements should be:

- explicit;
- testable;
- traceable;
- risk-based;
- incorporated into the specification.

Security requirements should map to acceptance criteria and verification
activities whenever applicable.

## Security Gates

Before release, applicable security controls should be verified.

Examples include:

- authentication and authorization;
- input validation;
- sensitive-data protection;
- dependency risks;
- secrets exposure;
- security-relevant configuration;
- known vulnerabilities;
- threat-model mitigations.

## AI-Assisted Security

AI-generated code and documentation require the same security scrutiny as
human-generated artifacts.

AI may assist with:

- threat identification;
- security requirement analysis;
- secure coding review;
- test generation;
- vulnerability analysis;
- security documentation.

Human engineering responsibility remains necessary for risk acceptance,
security decisions, and final verification.

## References

- NIST Secure Software Development Framework (SSDF):
  `references/security/nist-ssdf.md`
- OWASP Application Security Verification Standard (ASVS):
  [OWASP ASVS](https://owasp.org/projects/asvs)
