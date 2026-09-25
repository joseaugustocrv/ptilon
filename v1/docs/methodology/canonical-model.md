# Ptilon Canonical Model

## 1. Purpose

This document defines the canonical concepts and rules that govern the Ptilon
methodology. Other Ptilon documentation, templates, prompts, and examples must
remain consistent with this model.

This is a methodological contract, not a project-specific implementation
plan.

## 2. Core Principle

> **Make intent explicit before implementation, keep it traceable throughout
> development, and verify the delivered result against that intent.**

Ptilon uses AI as an engineering participant. AI can propose, transform,
analyze, implement, and verify artifacts, but it does not become the authority
for business intent, approved requirements, risk acceptance, or final release
decisions.

## 3. Canonical Lifecycle

The Ptilon lifecycle is:

```text
Intent
  ↓
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

Clarification, impact analysis, checklists, security analysis, quality review,
code review, and other reviews are **activities or gates within the lifecycle**.
They are not additional lifecycle stages unless a project explicitly defines
a project-specific extension.

The lifecycle is iterative and recursive in practice. Work performed at a
downstream point may reveal information that requires controlled revision of an
upstream artifact. This does not create a second lifecycle; it creates an
evolution loop that returns to the authoritative source, evaluates impact, and
revalidates the affected downstream artifacts.

### Lifecycle progression and human validation

By default, progression from one lifecycle activity to the next is gated by
human validation according to project governance. An AI-generated artifact is a
proposal until an authorized human review establishes it as approved and
authoritative. Approval may be recorded through the project's normal governance
mechanism.

AI may prepare downstream draft artifacts before an upstream gate is approved
when doing so is useful for analysis, impact discovery, or planning. Such drafts
remain provisional and must not be treated as current, approved, authoritative,
or Implementation Ready. Generating a downstream draft does not constitute
approval of its upstream inputs.

If a downstream activity discovers a material unresolved question that affects an
upstream artifact, progression beyond the affected gate stops. The question is
recorded, resolved through the clarification or change process, the authoritative
source is updated and approved, and affected downstream artifacts are
revalidated before they become current again.

## 4. Lifecycle Concepts

### Intent

The desired outcome, problem, objectives, constraints, and other information
that establishes why the work exists. Intent is the upstream expression of why
the work exists and what outcome is desired; it should not unnecessarily
prescribe the solution.

The reusable structure for recording Intent is defined by the Ptilon Intent
Template.

### Requirements

Approved statements of what the solution must provide or constrain. Ptilon
uses specialized requirement identifiers for functional, security, and quality
requirements.

Requirements may be organized into **engineering units** when the scope is
large enough that a single requirements artifact would become difficult to
understand, review, or maintain.

### Specification

The approved description of intended behavior, scope, acceptance criteria,
constraints, and relevant domain rules needed to guide implementation.

A specification may be organized into one or more engineering units. Each unit
covers a coherent scope derived from the approved requirements and remains
traceable to those requirements.

### Architecture & Design

The approved technical description of how the specified behavior is realized,
including system boundaries, components, interfaces, data, security, quality
concerns, and significant decisions.

### Plan

The approved implementation approach that organizes work, dependencies,
sequencing, constraints, and verification strategy before task execution.

### Tasks

Concrete implementation units derived from approved upstream artifacts. Tasks
must not silently redefine requirements or architectural decisions.

### Implementation

The construction or modification of the software and related artifacts.

### Verification

Activities and evidence demonstrating that implemented behavior satisfies the
applicable requirements and acceptance criteria and that relevant security and
quality controls are satisfied.

Verification is evidence-producing work. A test definition, successful
execution result, review record, scan result, or other evidence must not be
treated as proof merely because the artifact exists.

### Convergence

The explicit comparison of intent, approved artifacts, implementation, and
verification evidence to identify and resolve remaining discrepancies.
Convergence may produce additional tasks; it does not authorize silent changes
to requirements or architecture.

### Release

The controlled decision to deliver the verified result, subject to applicable
release criteria, residual-risk decisions, and approvals.

## 5. Cross-Cutting Activities

Clarification, analysis, checklists, security analysis, quality review, code
review, and other reviews are activities or gates performed at the relevant
point in the lifecycle. They do not create additional lifecycle stages.

### Clarification

Clarification is used whenever ambiguity, missing information, conflicting
statements, or newly discovered domain facts could affect implementation or
verification. It can be initiated from any lifecycle activity, including
Architecture, Plan, Tasks, Implementation, or Verification.

A clarification has two distinct states:

1. **Question** — an unresolved issue identified during engineering. It is
   represented by `QST-###` and remains non-authoritative.
2. **Clarification record** — the resolved interpretation, represented by
   `CLR-###`, including the question, resolution, authority, affected artifacts,
   and date.

Clarification output is not authoritative merely because an answer exists.
The authorized resolution must be incorporated into the appropriate
authoritative artifact before downstream work relies on it.

If the resolution changes approved intent or intended behavior rather than merely
clarifying existing meaning, it is a material change and must follow the Change
process.

Review is not a lifecycle stage between Convergence and Release. Reviews occur
where their subject matter requires them, for example:

- requirements review;
- specification review;
- architecture review;
- security review;
- quality review;
- task review;
- code review;
- test review;
- release-readiness review.

A review may act as a quality gate, but it does not change the canonical
lifecycle order.

## 6. Authority and Precedence

Ptilon uses an **upstream-authority model**. A downstream artifact refines an
upstream artifact; it does not silently override it.

The general relationship is:

```text
Approved intent and requirements
        ↓
Approved specification
        ↓
Approved architecture and decisions
        ↓
Approved plan and tasks
        ↓
Implementation
        ↓
Verification evidence
```

The following rules apply:

1. Approved requirements and explicit approved decisions govern intended
   behavior.
2. Specification refines approved requirements and cannot silently contradict
   them.
3. Architecture and ADRs explain and decide how approved behavior is realized;
   they cannot silently change what the system is required to do.
4. Plans and tasks derive executable work from approved upstream artifacts.
5. Test results and implementation evidence are evidence, not authority for
   changing requirements.
6. When two authoritative sources conflict, the conflict must be surfaced and
   resolved by an authorized human decision.
7. A downstream artifact must not be treated as an implicit change request.

Prompts may define contextual input precedence for a specific activity, but
that precedence must not contradict these general rules.

## 7. Decomposition and Incremental Evolution

Ptilon supports decomposition when the requirements or specification for a
project or change become too large or heterogeneous to manage reliably as a
single unit.

An **engineering unit** is a project-local, coherent scope used to organize
related requirements and specifications. It is not a lifecycle stage, a new
artifact type, or a mandatory architectural boundary.

The following rules apply:

1. A small project or change may use a single implicit engineering unit without
   introducing explicit unit structure.
2. The project or change Intent remains the upstream expression of the overall
   desired outcome.
3. Requirements may be grouped into engineering units when decomposition
   improves clarity, reviewability, ownership, or traceability.
4. Specifications may be divided into corresponding engineering units.
5. An engineering unit should have a stable project-local name or key. It does
   not introduce a new canonical identifier prefix.
6. Decomposition does not require duplicating the downstream lifecycle.
7. Architecture, Plan, Tasks, Verification, and other downstream artifacts
   remain project-level by default and are updated when the affected units
   require changes.
8. A new or changed unit must be assessed for impact on existing architecture,
   plans, tasks, verification, security, quality, and release artifacts.
9. A unit may require no downstream change, a revision of an existing artifact,
   or creation of an additional artifact when project scope or governance
   genuinely requires it.
10. Relationships between units must be explicit when one unit depends on or
   constrains another.
11. Decomposition must preserve traceability from the Intent through the
    applicable requirements and specifications into downstream engineering
    artifacts.

A typical project may therefore use:

```text
Intent
  ↓
Requirements
  ├── Unit A
  ├── Unit B
  └── Unit C
       ↓
Specification
  ├── Unit A
  ├── Unit B
  └── Unit C
       ↓
Architecture
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

The existence of multiple units does not imply that every downstream artifact
must be duplicated for every unit.

## 8. Human and AI Authority

AI may generate proposals, analyses, drafts, code, tests, and other derived
artifacts. AI-generated changes to requirements, security requirements, quality
requirements, architecture decisions, risk acceptance, exceptions, or release
decisions remain proposals until approved according to project governance.
Human validation is therefore a progression gate, not merely a final review.
Each lifecycle activity may produce a candidate artifact, but an artifact must
be approved before it becomes the authoritative basis for the next lifecycle
activity.

When an AI analysis identifies a missing or potentially necessary requirement,
the result must be marked as **proposed** until an authorized human approves it.

AI must not invent missing requirements, decisions, evidence, test results,
external facts, or approvals. If necessary information is missing, the output
must identify the gap.

## 9. Project Constitution and Tool Workflows

A project may adopt a project Constitution to establish project-level
principles, constraints, and governance. A Constitution is a governance
artifact, not a Ptilon lifecycle stage.

When Ptilon is used with GitHub Spec Kit, Spec Kit may use its Constitution
mechanism before feature-level specification. That mechanism is mapped into
Ptilon governance and does not alter the canonical Ptilon lifecycle.

External tools may introduce their own workflow stages or commands. Those
mechanisms must be interpreted as operational activities within the Ptilon
lifecycle rather than as replacements for the canonical lifecycle.

## 10. Canonical Identifiers

Ptilon lifecycle artifact identifiers use exactly three uppercase letters, a
hyphen, and a three-digit sequence.

| Prefix | Meaning |
| --- | --- |
| `REQ` | Requirement |
| `BUS` | Business Rule |
| `ASM` | Assumption |
| `QST` | Open Question |
| `CLR` | Clarification Record |
| `ACC` | Acceptance Criterion |
| `SEC` | Security Requirement |
| `QLT` | Quality Requirement |
| `TSK` | Implementation Task |
| `TST` | Test |
| `ADR` | Architecture Decision Record |
| `CHG` | Change Request |
| `THR` | Threat |
| `MIT` | Mitigation |
| `PRM` | Reusable Prompt |

Examples:

```text
REQ-001
ACC-001
SEC-001
QLT-001
TSK-001
TST-001
ADR-001
CHG-001
THR-001
MIT-001
PRM-001
```

Legacy two-letter or longer prefixes must not be introduced in new Ptilon
artifacts.

## 11. Requirement Relationships

Security and quality requirements are specialized requirements. They use their
own identifiers but participate in the same traceability discipline.

The minimum expected relationship for a verifiable requirement is:

```text
REQ / SEC / QLT
      ↓
    ACC
      ↓
    TST
```

Where implementation work is applicable:

```text
REQ / SEC / QLT
      ↓
    ACC
      ↓
    TSK
      ↓
    TST
      ↓
Verification Evidence
```

Not every requirement requires every artifact, but any omitted relationship
must be justified by the nature of the requirement.

## 12. Changes and Evolution

Ptilon distinguishes **clarification** from **change**.

A clarification resolves uncertainty while preserving the approved meaning.
A change modifies approved intent, scope, behavior, constraints, or another
authoritative decision.

A material change follows:

```text
CHG
 ↓
Impact Analysis
 ↓
Update authoritative source
 ↓
Revalidate affected requirements / specification units
 ↓
Assess downstream artifacts
 ↓
Revise affected architecture / plan / tasks / tests / security / evidence
 ↓
Re-run applicable quality gates
 ↓
Implementation / Verification
 ↓
Converge
 ↓
Release
```

A downstream activity may discover a gap without being authorized to resolve it
by assumption. Instead:

```text
Any lifecycle activity
        ↓
      QST
        ↓
Clarification / analysis
        ↓
      CLR
        ↓
Does the resolution change approved intent?
       / \
     No   Yes
     ↓     ↓
Update    CHG
source    ↓
as needed Impact Analysis
     \     /
      Revalidate
          ↓
   Continue downstream work
```

When a material unresolved question is discovered, the affected lifecycle
gate is blocked from progression until the question is resolved or explicitly
accepted as non-blocking by the authorized human authority. Downstream drafts may
be produced for analysis, but they remain provisional while the blocking issue is
unresolved.

The source artifact must be updated before affected downstream artifacts are
treated as current. The impact analysis must identify both direct and indirect
effects, including dependencies, interfaces, data, security, quality,
verification, operations, documentation, and release evidence.

Affected downstream artifacts are considered **not revalidated** until their
impact has been assessed and the required revisions or explicit no-change
decisions have been recorded.

A change to one engineering unit does not automatically require duplication or
recreation of Architecture, Plan, Tasks, or Verification artifacts. Those
artifacts are updated according to the identified impact.

A change must not be implemented only by editing a downstream artifact while
leaving the authoritative source unchanged.

## 13. Readiness for Implementation

`Implementation Ready` is a quality state, not a lifecycle stage.

A scope is Implementation Ready only when:

1. approved intent and applicable requirements are current;
2. material questions affecting implementation are resolved or explicitly
   accepted as non-blocking;
3. the specification is approved and contains observable acceptance criteria;
4. relevant architecture and significant decisions are approved;
5. the implementation plan is complete enough to establish dependencies and
   sequencing;
6. tasks are actionable, dependency-aware, traceable, and independently
   verifiable;
7. security and quality requirements have corresponding controls or
   verification methods where applicable;
8. required cross-artifact consistency analysis is clean or has approved,
   documented exceptions;
9. no affected downstream artifact is awaiting impact assessment or
   revalidation;
10. required test strategy and acceptance verification are defined.

Implementation Ready does not mean that the software is implemented or that
release is approved.

## 14. Ptilon Core and Ptilon Governed

Ptilon has one methodological core. Governance depth is proportional to risk.

### Ptilon Core

Suitable for small applications and personal projects. The essential chain is
maintained with lightweight artifacts and reviews:

```text
Intent → Requirements → Specification → Architecture → Plan → Tasks
→ Implementation → Verification → Convergence → Release
```

### Ptilon Governed

For larger or higher-risk projects, the same core may add stronger controls such
as ADRs, change requests, formal review records, security assessments, quality
gates, approval records, and durable verification evidence.

These are governance controls around the same methodology, not a different
engineering lifecycle.

## 15. Methodology Change

Changes to the Ptilon methodology itself must be evaluated for impact across:

- lifecycle definitions;
- identifier taxonomy;
- authority rules;
- templates;
- prompts;
- examples;
- references;
- automation and quality gates.

The canonical model should be updated before dependent artifacts are changed.
