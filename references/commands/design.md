# /design

Create a focused UI/UX design artifact only when user experience, flows, layout, visual direction, responsiveness, or accessibility materially affect success.

## When To Use

Use for:

- New screens or workflows.
- Complex interaction states.
- Visual redesigns.
- Accessibility-sensitive UI.
- Mobile or responsive behavior.

Skip for:

- Backend-only changes.
- Small bug fixes.
- Internal refactors.
- UI changes already fully specified elsewhere.

## Workflow

1. Read `_delivery/context/index.md` if present.
2. Load product and standards context relevant to UI.
3. Read `_delivery/specs/<slug>.md`.
4. Read `_delivery/ideas/<slug>.md` if useful.
5. Route to UX or visual capabilities only when they add value.
6. Create `_delivery/designs/` if missing.
7. Save `_delivery/designs/<slug>.md` using `references/templates/design.md`.

## Output

Report design path, major UX decisions, unresolved questions, and recommended next command.
