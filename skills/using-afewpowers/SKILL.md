---
name: using-afewpowers
description: Use at the start of software development that creates or changes behavior. Route the work through brainstorming before implementation, test-driven development during implementation, and code review after implementation.
---

# Using afewpowers

Follow this workflow in order. Invoke each skill when its phase begins; do not search for workflows that are not included in this skill set.

## 1. Brainstorm before implementing

Invoke `brainstorming` before changing production code.

- Understand the problem, constraints, and existing context.
- Compare viable approaches and agree on a design.
- Record acceptance criteria that tests and review can verify.
- Obtain the user's approval before implementation.

After the design is approved, return to this workflow and proceed directly to TDD.

## 2. Implement with TDD

Invoke `test-driven-development` before writing implementation code.

- Work in small red-green-refactor cycles.
- Confirm each new test fails for the expected reason before making it pass.
- Implement only the behavior required by the approved design.
- Keep the relevant test suite green after every refactor.

Follow the TDD skill's exception guidance when a change has no meaningful executable behavior to test.

## 3. Review after implementing

When the implementation is complete and tests pass:

1. Invoke `requesting-code-review` and compare the implementation with the approved design, acceptance criteria, tests, and diff.
2. Invoke `receiving-code-review` before acting on the feedback.
3. Fix verified blocking or important issues using TDD, then rerun the relevant tests.
4. Repeat review when fixes materially change the implementation.

Use an independent reviewer or subagent when one is available. Otherwise, perform a focused self-review using the same requirements and evidence.

## Completion gate

Do not report implementation complete until:

- the design and scope were approved;
- behavioral changes were developed with TDD;
- relevant tests pass;
- code review is complete; and
- verified blocking and important review findings are resolved.

Direct user instructions take precedence over this workflow.
