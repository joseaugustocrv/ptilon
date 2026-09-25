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

Clarification, analysis, checklists, security analysis, quality review, code
review, and other reviews are **activities or gates within the lifecycle**.
They are not additional lifecycle stages unless a project explicitly defines
a project-specific extension.

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

### Convergence

The explicit comparison of intent, approved artifacts, implementation, and
verification evidence to identify and resolve remaining discrepancies.

### Release

The controlled decision to deliver the verified result, subject to applicable
release criteria, residual-risk decisions, and approvals.

## 5. Cross-Cutting Activities

Clarification, analysis, checklists, security analysis, quality review, code
review, and other reviews are activities or gates performed at the relevant
point in the lifecycle. They do not create additional lifecycle stages.

### Clarification

Clarification is used when ambiguity, missing information, or conflicting
statements could affect implementation or verification. It produces questions,
identified assumptions, and surfaced conflicts for human resolution.

Clarification output is not itself authoritative. Resolved decisions must be
incorporated into the appropriate authoritative artifact, such as Intent,
Requirements, or Specification, before downstream work relies on them.

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
| `CLR` | Clarification |
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

## 12. Changes

A material change to intended behavior follows:

```text
CHG
 ↓
Impact Analysis
 ↓
Update source of intent
 ↓
Revalidate affected requirements / specification units
 ↓
Assess downstream artifacts
 ↓
Update implementation and verification
 ↓
Converge
 ↓
Release
```

A change to one engineering unit does not automatically require duplication or
recreation of Architecture, Plan, Tasks, or Verification artifacts. Those
artifacts are updated according to the identified impact.

A change must not be implemented only by editing a downstream artifact while
leaving the authoritative source unchanged.

## 13. Ptilon Core and Ptilon Governed

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

## 14. Methodology Change

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
