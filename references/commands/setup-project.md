# /setup-project

Initialize persistent delivery context for the repository.

## Inputs To Capture

Ask only for missing information that cannot be inferred safely:

- Project type: learning, freelance, internal tool, SaaS, startup, or other.
- Stack and package manager.
- Default rigor: task-heavy, feature-heavy, or product-heavy.
- Design needs: none, light UI, full UI/UX.
- Research depth: none, light web research, structured market research.
- Git preferences: branch naming, commit style, review expectations.

## Workflow

1. Inspect existing files before creating anything.
2. Create `_delivery/context/` only if it is missing.
3. Create missing context files from `references/templates/`.
4. Preserve user content in existing context files.
5. Populate concise, repo-specific defaults from discovered files.
6. Create `_delivery/context/skills.md` from `references/templates/skills.md` with installed, recommended, and fallback capabilities.

## Required Files

- `_delivery/context/index.md`
- `_delivery/context/product.md`
- `_delivery/context/tech.md`
- `_delivery/context/standards.md`
- `_delivery/context/decisions.md`
- `_delivery/context/skills.md`

## Output

Report created and updated files, inferred assumptions, and any questions that still affect future workflow quality.
