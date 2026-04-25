# /commit-message

Generate a commit message from staged changes.

## Workflow

1. Confirm the directory is a git repo.
2. Inspect staged changes only.
3. If nothing is staged, say so and do not infer from unstaged changes unless the user asks.
4. Read relevant spec or plan only if staged changes clearly correspond to a known slug.
5. Produce a concise commit message.

## Format

Default to:

```text
type(scope): summary

- Detail 1
- Detail 2
```

Use the project's preferred commit style from `_delivery/context/standards.md` when present.

## Output

Provide the commit message and a short note about what staged evidence it was based on.
