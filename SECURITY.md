# Ptilon Security Policy

## Scope

Ptilon is a methodology and documentation repository. Security issues may affect:

- repository automation;
- GitHub Actions workflows;
- templates and prompts;
- documentation that defines security practices;
- examples containing security guidance;
- dependencies used by repository tooling.

## Reporting a Security Issue

Do not disclose sensitive security details in a public GitHub issue.

Report suspected security vulnerabilities through the repository's private security reporting mechanism when available.

Include:

- affected artifact or workflow;
- description of the vulnerability;
- reproduction steps, when safe to provide;
- potential impact;
- relevant logs or evidence;
- suggested mitigation, if known.

## Handling

Security reports should be evaluated for:

1. exploitability;
2. affected scope;
3. confidentiality, integrity, and availability impact;
4. exposure of secrets or sensitive information;
5. required remediation;
6. need for broader repository review.

Do not publish exploit details until the issue has been appropriately assessed and remediated.

## Repository Security Practices

Contributors should:

- never commit credentials, tokens, private keys, or other secrets;
- use GitHub-provided secret mechanisms for workflow credentials;
- minimize workflow permissions;
- pin or regularly review third-party GitHub Actions;
- keep dependencies and actions reasonably current;
- avoid unnecessary network access in automation;
- review changes to security-sensitive documentation and workflows.

## Scope Limitation

This policy describes repository-level security reporting and maintenance.

It does not replace the threat-modeling, secure-development, or security-engineering
practices defined elsewhere in Ptilon.
