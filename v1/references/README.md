# Ptilon — References

## 1. Purpose

Provide a curated reference map for the standards, frameworks, methodologies,
and engineering practices that support Ptilon.

This directory contains supporting references and analyses. It does not replace
the normative Ptilon methodology.

---

## 2. Reference categories

Ptilon organizes references into the following categories:

- **Standards** — formal standards that provide lifecycle, requirements,
  architecture, and quality foundations;
- **Security frameworks** — established security development frameworks and
  practices;
- **SDD** — Specification-Driven Development references and tooling;
- **Engineering practices** — established software engineering practices;
- **Quality** — testing, verification, and quality engineering references;
- **Governance** — decision-making, traceability, and lifecycle governance
  references.

---

## 3. Primary reference set

The initial Ptilon reference baseline includes:

| Reference | Primary purpose |
| --- | --- |
| ISO/IEC/IEEE 12207 | Software lifecycle processes |
| ISO/IEC/IEEE 29148 | Requirements engineering |
| ISO/IEC 25010 | Product quality |
| ISO/IEC/IEEE 42010 | Architecture description |
| NIST SSDF | Secure software development |
| GitHub Spec Kit | Specification-Driven Development workflow |

These references form the foundation of the methodology but are applied
according to project context.

---

## 4. Reference selection principles

References included in Ptilon should be:

- established and relevant to software engineering;
- sufficiently authoritative for their intended use;
- applicable to AI-assisted development;
- clearly scoped;
- maintained or historically significant where appropriate;
- used without overstating their authority.

A reference should not be included merely because it is popular.

---

## 5. Reference versus requirement

A reference does not automatically create a project obligation.

The project must explicitly determine whether a reference is:

- informative;
- recommended;
- adopted as an engineering practice;
- contractually required;
- regulatorily required;
- formally adopted as a conformance target.

This distinction is essential for accurate governance and compliance claims.

---

## 6. Version and currency

Reference documents should identify their relevant edition or version when
applicable.

Ptilon should periodically review important references for:

- new editions;
- withdrawn standards;
- revised guidance;
- changes in tooling;
- significant changes in industry practice.

When a reference changes materially, affected Ptilon artifacts should be
reviewed.

---

## 7. Evidence and provenance

Reference-based decisions should preserve sufficient provenance to explain:

- which reference was used;
- which version or edition applied;
- which principle or requirement was relevant;
- how it influenced the resulting decision;
- whether the reference was mandatory or advisory.

This supports traceability without requiring unnecessary documentation.

---

## 8. Recommended repository structure

Reference material may be organized as follows:

```text
references/
├── README.md
├── standards/
│   ├── iso-12207.md
│   ├── iso-29148.md
│   ├── iso-25010.md
│   └── iso-42010.md
├── security/
│   └── nist-ssdf.md
├── sdd/
│   └── github-spec-kit.md
└── engineering/
    ├── tdd.md
    ├── bdd.md
    ├── adr.md
    └── cicd.md
```

Reference files should summarize the relevant concepts and explain their
relationship to Ptilon. They should not reproduce copyrighted standards.

---

## 9. Copyright and licensing

Ptilon should not reproduce proprietary or copyrighted standards in full.

Reference documents should contain:

- bibliographic information;
- official links;
- concise summaries;
- interpretation relevant to Ptilon;
- documented relationships to Ptilon practices.

Official sources should be preferred whenever available.

---

## 10. Relationship with Ptilon methodology

The relationship is:

External references → Ptilon methodology → Project-specific rules →
Implementation evidence

External references inform Ptilon.

Ptilon organizes those references into an integrated development methodology.

Projects then adapt the methodology to their own context and obligations.

---

## 11. Reference maintenance

Reference maintenance should be treated as part of methodology governance.

When a primary reference changes, assess:

1. whether the change affects Ptilon principles;
2. whether affected methodology documents require revision;
3. whether templates require revision;
4. whether prompts require revision;
5. whether examples require revision;
6. whether existing projects require migration guidance.

Significant changes should be recorded in version control.

---

## 12. Status

This document defines the organization and governance of Ptilon references.

Detailed reference analyses should be added under this directory as the
methodology evolves.
