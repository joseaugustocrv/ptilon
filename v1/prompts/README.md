# Ptilon Prompts

## 1. Purpose

This directory contains version-controlled prompts used to support repeatable
AI-assisted software engineering activities within Ptilon.

Prompts are engineering artifacts and should be maintained with the same
discipline applied to other project assets.

---

## 2. Prompt Categories

Prompts may support the following activities:

- Specification
- Clarification
- Planning
- Task decomposition
- Architecture
- Testing
- Security
- Code review
- Quality review
- Traceability
- Release
- Convergence

---

## 3. Prompt Lifecycle

A production prompt follows this lifecycle:

1. **Draft** — initial construction.
2. **Review** — technical and methodological review.
3. **Evaluate** — validation against representative scenarios.
4. **Adopt** — used in the workflow.
5. **Maintain** — updated when the workflow or requirements change.
6. **Retire** — removed from active use when no longer appropriate.

---

## 4. Naming Convention

Use descriptive, lowercase filenames with hyphens.

Examples:

```text
specification-review.md

requirements-clarification.md

architecture-review.md

test-generation.md

security-review.md

convergence-check.md
```

---

## 5. Required Prompt Metadata

Each reusable prompt must identify:

- `PRM-###` prompt identifier;
- version;
- status;
- purpose;
- workflow activity;
- inputs;
- authority;
- constraints;
- expected output;
- validation criteria;
- related methodology artifact.

The metadata template is defined in [`prompt-version-metadata.md`](prompt-version-metadata.md).

---

## 6. Authority and Traceability

All prompts follow the upstream-authority model defined in
[`../docs/methodology/canonical-model.md`](../docs/methodology/canonical-model.md).

Approved upstream artifacts govern intended behavior. Downstream artifacts may
refine implementation details but must not silently override approved intent.

When sources conflict, the prompt must surface the conflict instead of choosing
an invented resolution.

AI-generated requirements, security requirements, quality requirements,
decisions, evidence, and approvals are proposals until approved according to
project governance.

Where applicable, prompts should require references to the artifacts supporting
each significant conclusion or proposal.

---

## 7. Validation

A prompt should be considered suitable for repeatable use only after its
output has been evaluated for:

- Correctness
- Completeness
- Consistency
- Traceability
- Unsupported assumptions
- Output-format compliance

Material changes to a prompt should trigger re-evaluation.

---

## 8. Human Accountability

AI-generated outputs remain subject to human review and approval according to
the applicable workflow.

A prompt must never be treated as authorization to:

- Change an approved requirement.
- Accept a security risk.
- Approve production deployment.
- Override engineering governance.
- Replace required human decisions.

---

## 9. Relationship with GitHub Spec Kit

Ptilon prompts may complement GitHub Spec Kit workflows.

Ptilon does not attempt to replace Spec Kit's specification-driven development
mechanisms. Instead, prompts in this directory should support the broader
Ptilon methodology, including engineering quality, security, governance,
traceability, and lifecycle integration.

See:

- `../references/sdd/github-spec-kit.md`
- `../docs/workflow/README.md`
- `../docs/methodology/README.md`

---

## 10. Principles

1. Prompts are version-controlled artifacts.
2. Prompt behavior must be testable and reviewable.
3. Prompts should reduce ambiguity rather than hide it.
4. Missing information must be surfaced rather than invented.
5. AI output must remain traceable to authoritative project artifacts.
6. Human accountability remains explicit.
