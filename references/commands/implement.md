# /implement

Implement from an existing plan.

## Workflow

1. Read `_delivery/plans/<slug>.md`.
2. Read `_delivery/specs/<slug>.md`.
3. Read `_delivery/designs/<slug>.md` if referenced or relevant.
4. Read `_delivery/context/index.md` and only the context files needed for the work.
5. Inspect current git status before editing.
6. Implement tasks in plan order, adapting when the codebase requires it.
7. Update plan checkboxes as tasks are completed.
8. Update the spec or design if implementation reveals accepted requirement changes.
9. Run relevant tests, builds, linters, or manual checks.

## Rules

- Keep changes scoped to the accepted plan.
- Do not overwrite user changes.
- If the plan is stale, update it before continuing.
- If a missing external skill would help but is not installed, recommend it and continue with the fallback.

## Output

Summarize changed files, completed plan tasks, validation results, and any follow-up needed.
