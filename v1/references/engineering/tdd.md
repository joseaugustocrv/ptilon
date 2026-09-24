# Test-Driven Development (TDD)

## 1. Purpose

Document how Test-Driven Development (TDD) is used as an engineering practice
within Ptilon.

TDD is a development technique that uses executable tests to establish expected
behavior before or alongside implementation.

---

## 2. Role in Ptilon

TDD provides a feedback loop between expected behavior and implementation.

The fundamental cycle is:

Red → Green → Refactor

Where:

- **Red** — define a test that currently fails;
- **Green** — implement the minimum behavior required to pass;
- **Refactor** — improve the implementation while preserving behavior.

TDD is an engineering practice, not a mandatory requirement for every type of
change.

---

## 3. Relationship with Ptilon

Ptilon's broader workflow is:

Specify → Clarify → Plan → Tasks → Implement → Converge

TDD operates primarily inside the implementation and verification activities.

A typical relationship is:

Requirement → Acceptance Criterion → Test → Implementation → Evidence

TDD therefore complements Specification-Driven Development rather than
replacing it.

---

## 4. When to use TDD

TDD is particularly useful when:

- behavior can be expressed clearly as executable expectations;
- business logic is complex;
- regression risk is significant;
- interfaces have well-defined contracts;
- implementation benefits from rapid feedback;
- refactoring safety is important.

TDD may be less practical when the primary challenge is exploratory discovery,
visual design, infrastructure experimentation, or other work where behavior is
not yet sufficiently understood.

---

## 5. The Red phase

The Red phase establishes the expected behavior before implementation.

A good test should:

- express one meaningful behavior;
- fail for the expected reason;
- provide useful feedback;
- remain understandable to future maintainers.

A failing test should not be created merely to increase coverage.

---

## 6. The Green phase

The Green phase implements the minimum behavior necessary to satisfy the test.

The objective is to establish correctness before optimization or extensive
refactoring.

Implementation should remain consistent with:

- approved requirements;
- architecture;
- security constraints;
- project conventions.

Passing a test does not justify violating higher-level constraints.

---

## 7. The Refactor phase

Refactoring improves internal structure without changing externally observable
behavior.

Possible activities include:

- removing duplication;
- improving naming;
- simplifying control flow;
- improving modularity;
- extracting abstractions;
- improving maintainability.

The test suite provides regression protection during refactoring.

---

## 8. Test quality

TDD depends on useful tests.

Tests should generally be:

- deterministic;
- focused;
- readable;
- maintainable;
- independently meaningful;
- fast enough for the feedback loop.

Tests should avoid unnecessary coupling to implementation details.

---

## 9. Unit tests

TDD is commonly associated with unit tests.

Unit tests should verify behavior at the smallest practical level while
maintaining meaningful isolation.

Typical targets include:

- domain logic;
- validation;
- transformations;
- calculations;
- decision logic;
- small service components.

The appropriate unit boundary depends on the architecture.

---

## 10. Integration and higher-level tests

TDD does not eliminate other levels of testing.

Integration and end-to-end tests remain appropriate when behavior depends on:

- databases;
- external services;
- APIs;
- message brokers;
- authentication systems;
- deployment environments.

The testing strategy should reflect the risk and architecture of the system.

---

## 11. AI-assisted TDD

AI may assist with:

- generating initial tests;
- identifying edge cases;
- proposing test scenarios;
- generating test data;
- analyzing failures;
- suggesting refactorings.

AI-generated tests require validation.

A generated test may encode an incorrect assumption or merely reproduce the
implementation's behavior rather than independently verifying the requirement.

The expected behavior must remain grounded in the governing requirement or
acceptance criterion.

---

## 12. TDD and requirements

TDD should be driven by intended behavior rather than implementation details.

A useful sequence is:

Requirement → Acceptance Criterion → Test → Implementation

When a test reveals that the expected behavior is unclear, the appropriate
action is to clarify the requirement rather than arbitrarily choosing an
implementation behavior.

---

## 13. TDD and security

Security behavior can also be developed using TDD.

Examples include:

- authentication failures;
- authorization boundaries;
- input validation;
- access control;
- sensitive-data handling;
- error behavior.

Security tests should be traceable to security requirements or identified
threats when appropriate.

---

## 14. TDD and refactoring

A healthy TDD workflow enables continuous refactoring.

Refactoring should not alter the behavior established by the specification and
tests.

When refactoring exposes a requirement or architecture problem, the
appropriate governing artifact should be updated rather than hiding the issue
inside implementation code.

---

## 15. TDD and coverage

Code coverage is a useful measurement but is not a substitute for test
quality.

High coverage can coexist with:

- weak assertions;
- duplicated tests;
- untested business scenarios;
- missing edge cases;
- incorrect expected behavior.

Ptilon therefore treats coverage as supporting evidence rather than the sole
quality criterion.

---

## 16. TDD evidence

Relevant evidence may include:

- test cases;
- test execution results;
- coverage reports;
- pull request checks;
- defect history;
- regression results.

Evidence should be proportional to project risk and compliance requirements.

---

## 17. Ptilon principles

Ptilon applies the following TDD principles:

1. tests should express meaningful expected behavior;
2. failing tests should provide useful feedback;
3. implementation should satisfy established behavior;
4. refactoring should preserve verified behavior;
5. tests should remain independent from unnecessary implementation details;
6. AI-generated tests require validation;
7. security behavior should be tested when relevant;
8. coverage should not be treated as the sole measure of test quality.

---

## 18. References

- Kent Beck — Test-Driven Development: By Example
- Ptilon Requirements Engineering:
  `references/standards/iso-29148.md`
- Ptilon Quality:
  `references/standards/iso-25010.md`
- Ptilon Security:
  `references/security/nist-ssdf.md`
- Ptilon Workflow:
  `docs/workflow/README.md`

---

## 19. Status

This document defines TDD as a recommended engineering practice within Ptilon.

Projects should determine where TDD provides sufficient value and define the
appropriate testing strategy for their context.
