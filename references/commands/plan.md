# /plan

Create an implementation plan from the accepted artifacts.

## Workflow

1. Read `_delivery/context/index.md` if present.
2. Load tech, standards, and decisions relevant to implementation.
3. Read `_delivery/specs/<slug>.md`.
4. Read `_delivery/designs/<slug>.md` only if it exists or UI/UX matters.
5. Inspect the codebase enough to make the plan concrete.
6. Create `_delivery/plans/` if missing.
7. Save `_delivery/plans/<slug>.md` using `references/templates/plan.md`.

## Plan Requirements

Include:

- Objective and scope.
- Files or modules likely to change.
- Step-by-step tasks with checkboxes.
- Test and validation strategy.
- Risks and rollback notes.
- Git constraints.

Keep plans proportional. Level 1 may use a mini-plan; Level 2 and 3 slices should be more explicit.

## Output

Report plan path, key implementation decisions, and whether the plan is ready for `/implement <slug>`.
