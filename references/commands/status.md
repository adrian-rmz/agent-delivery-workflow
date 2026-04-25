# /status

Summarize active project delivery state without loading every artifact.

## Workflow

1. Read `_delivery/context/index.md` if present.
2. List artifact directories shallowly:
   - `_delivery/ideas/`
   - `_delivery/research/`
   - `_delivery/specs/`
   - `_delivery/designs/`
   - `_delivery/plans/`
   - `_delivery/reviews/`
3. Inspect git branch and status if in a git repo.
4. Read only short index or title sections from active artifacts when needed.
5. Do not load long specs, plans, designs, or reviews unless the user asks for detail.

## Output

Include:

- Project context availability.
- Active branch and dirty/clean state.
- Recent or active artifacts.
- Suggested next command.
- Missing setup files, if any.
