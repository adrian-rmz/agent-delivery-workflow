# /spec

Create or update a spec for a task, feature, or product slice.

## Git Gate

Follow `references/capabilities/git.md`.

Before creating a new spec:

1. Check whether the directory is a git repo.
2. If not a git repo, continue without branch creation and report that no branch was created.
3. If it is a git repo and dirty, stop before creating a branch or spec. Ask the user to commit or stash changes.
4. If it is a clean git repo, create `delivery/feature/<slug>` unless already on that branch or the user asked not to.

## Workflow

1. Read `_delivery/context/index.md` if present.
2. Load product, tech, standards, and decisions only as needed.
3. Read `_delivery/ideas/<slug>.md` when it exists.
4. Determine level if no idea artifact exists.
5. Create `_delivery/specs/` if missing.
6. Create or update `_delivery/specs/<slug>.md`.
7. Use `_delivery/specs/template.md` if present; otherwise use `references/templates/spec.md`.
8. Include goals, non-goals, requirements, edge cases, acceptance criteria, and validation.
9. Keep design and implementation details brief unless they are requirements.

## Output

Report branch action, spec path, assumptions, and recommended next command: `/design <slug>` when UI/UX matters, otherwise `/plan <slug>`.
