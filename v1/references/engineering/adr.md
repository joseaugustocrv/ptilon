# Architecture Decision Records (ADR)

## 1. Purpose

Document how Architecture Decision Records (ADRs) are used within Ptilon to
preserve significant technical and architectural decisions, their context, and
their consequences.

ADRs provide durable decision evidence and reduce the loss of architectural
reasoning over time.

---

## 2. Role in Ptilon

ADRs support:

- architectural traceability;
- decision transparency;
- consistent technical evolution;
- onboarding;
- impact analysis;
- maintenance;
- governance of significant technical choices.

Ptilon treats ADRs as a lightweight mechanism. Not every technical decision
requires an ADR.

---

## 3. When to create an ADR

An ADR should be considered when a decision:

- has significant architectural impact;
- affects multiple components;
- introduces a meaningful technology dependency;
- affects security;
- affects quality attributes;
- creates important operational consequences;
- is difficult or costly to reverse;
- establishes a project-wide convention;
- resolves a significant technical trade-off.

Routine implementation choices generally do not require an ADR.

---

## 4. ADR lifecycle

A decision typically progresses through:

Proposed → Accepted → Superseded / Deprecated / Rejected

The exact status vocabulary may be adapted to project needs.

An accepted ADR represents the decision governing the relevant context at that
point in time.

A later decision should supersede an earlier ADR rather than silently rewriting
historical reasoning.

---

## 5. Recommended ADR structure

A Ptilon ADR should generally contain:

```text
# ADR-NNNN: Title

## Status

Proposed | Accepted | Rejected | Superseded | Deprecated

## Context

What problem or decision requires attention?

## Decision

What was decided?

## Alternatives Considered

What meaningful alternatives were evaluated?

## Consequences

What benefits, costs, risks, and trade-offs result?

## Related Requirements

Which requirements, constraints, or concerns are affected?

## Related Decisions

Which ADRs or decisions are related?

## Evidence

What evidence supports or validates the decision?
```

Projects may extend this structure when necessary.

---

## 6. Decision quality

An ADR should make the reasoning understandable without requiring the reader to
reconstruct the original discussion.

Where relevant, document:

- assumptions;
- constraints;
- alternatives;
- trade-offs;
- risks;
- expected consequences;
- rejected alternatives;
- reversibility.

The objective is not to document every discussion. It is to preserve the
decision and the reasoning necessary to understand it.

---

## 7. AI-assisted decision making

AI may assist with:

- identifying alternatives;
- summarizing trade-offs;
- analyzing risks;
- drafting ADRs;
- identifying affected components;
- checking consistency with existing decisions.

AI-generated analysis must be reviewed by the responsible decision-maker.

The final decision must remain attributable to a human authority.

AI output must not be treated as an independent source of architectural
authority.

---

## 8. ADRs and requirements

Architectural decisions should remain connected to the requirements and
constraints that motivated them.

A useful relationship is:

Requirement / Concern → ADR → Architecture → Implementation → Evidence

When an ADR is driven by a quality or security requirement, the relationship
should be explicit when practical.

---

## 9. ADRs and architecture descriptions

ADRs explain **why** significant architectural decisions were made.

Architecture descriptions explain **what the resulting architecture is**.

They are complementary.

An architecture document should not need to contain the full historical
reasoning for every decision when the reasoning is already preserved in ADRs.

---

## 10. ADRs and change

When an architectural decision changes:

1. identify the existing ADR;
2. assess its current status;
3. create a new ADR when a materially different decision is made;
4. mark the previous decision as superseded or otherwise obsolete;
5. update affected architecture and implementation artifacts;
6. verify downstream impacts.

Historical ADRs should generally remain immutable except for status or
administrative metadata.

---

## 11. ADRs in the Ptilon workflow

ADRs may be created or updated during:

Clarify → Plan → Analyze → Implement → Converge

They are particularly relevant when:

- clarification exposes a structural decision;
- planning identifies architectural alternatives;
- analysis reveals a technical trade-off;
- implementation discovers a significant constraint;
- convergence requires an architectural correction.

---

## 12. ADRs and quality

Architectural decisions may directly affect ISO/IEC 25010 quality
characteristics.

Examples:

- performance;
- reliability;
- security;
- maintainability;
- compatibility;
- scalability;
- interaction capability.

When a quality requirement materially influences an architectural decision, the
ADR should identify the relevant concern.

---

## 13. ADRs and security

Security-related architectural decisions should be documented when they have
significant impact.

Examples include:

- authentication architecture;
- authorization model;
- trust boundaries;
- encryption strategy;
- secrets management;
- isolation;
- security logging;
- external security dependencies.

Security decisions should remain consistent with the project's security
requirements and applicable secure development practices.

---

## 14. ADRs and AI-generated architecture

When AI proposes an architectural alternative:

1. identify the decision to be made;
2. validate the proposal against requirements and constraints;
3. compare meaningful alternatives;
4. assess quality and security implications;
5. document the human decision in the ADR;
6. preserve relevant evidence when necessary.

The ADR records the engineering decision, not merely the AI suggestion.

---

## 15. Repository organization

A project may organize ADRs as:

```text
docs/
└── architecture/
    └── adr/
        ├── 0001-title.md
        ├── 0002-title.md
        └── ...
```

The exact location may vary, but ADRs should remain version controlled and easy
to discover.

---

## 16. Ptilon principles

Ptilon applies the following ADR principles:

1. significant decisions should be explicit;
2. decision context should be preserved;
3. meaningful alternatives should be considered when appropriate;
4. consequences should be documented;
5. decisions should remain traceable;
6. historical decisions should not be silently rewritten;
7. AI may assist analysis but does not own decisions;
8. ADR rigor should be proportional to decision impact.

---

## 17. References

- Michael Nygard — Documenting Architecture Decisions
- ISO/IEC/IEEE 42010 — Architecture description:
  <https://www.iso.org/standard/50508.html>
- Ptilon Architecture: `references/standards/iso-42010.md`
- Ptilon Governance: `docs/governance/README.md`
- Ptilon Methodology: `docs/methodology/README.md`

---

## 18. Status

This document defines ADRs as a recommended architectural governance practice
within Ptilon.

Projects should establish their own ADR numbering, storage location, review
responsibilities, and status conventions.
