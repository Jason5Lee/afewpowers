# afewpowers

`afewpowers` is a simplified version of [superpowers](https://github.com/obra/superpowers) software-development skill set. Today's models are so advanced that many are unnecessary, so it keeps three quality gates from superpowers and removes the rest:

```text
brainstorm -> implement with TDD -> review -> done
```

The entry skill, `using-afewpowers`, guides an agent through those gates in order.

## Included skills

| Skill                       | Purpose                                                                                                 |
| --------------------------- | ------------------------------------------------------------------------------------------------------- |
| `using-afewpowers`        | Routes development work through the complete workflow.                                                  |
| `brainstorming`           | Clarifies requirements, compares approaches, and produces an approved design before code changes begin. |
| `test-driven-development` | Implements the approved behavior in red-green-refactor cycles.                                          |
| `requesting-code-review`  | Reviews the completed implementation against its design, tests, and diff.                               |
| `receiving-code-review`   | Verifies review feedback before applying it and provides a disciplined way to resolve findings.         |

## Workflow

1. **Brainstorm:** inspect the context, resolve ambiguity, choose an approach, define acceptance criteria, and get design approval.
2. **Implement with TDD:** write a failing test, confirm the failure, add the minimum implementation, confirm the tests pass, and refactor while green.
3. **Review:** request an independent review when possible, evaluate the feedback, fix verified issues through TDD, and rerun the tests.

Read-only questions and tasks that do not create or change software behavior do not require the full workflow.

## Installation

Copy or symlink each directory under `skills/` into the skills directory used by your coding agent. For Codex, that is normally `$CODEX_HOME/skills`, or `~/.codex/skills` when `CODEX_HOME` is not set.

For example:

```sh
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
cp -R skills/* "${CODEX_HOME:-$HOME/.codex}/skills/"
```

Restart or reload the agent so it discovers the skills. Then start a development task normally or explicitly ask it to use `using-afewpowers`.

## Design intent

The set is intentionally opinionated and compact: agree on what to build, prove behavior incrementally, and inspect the result before declaring it complete. Deleted planning, worktree, debugging, and orchestration skills are not prerequisites for this workflow.
