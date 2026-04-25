# Git Capability

Apply git discipline without blocking work unnecessarily.

## Branching

For `/spec`:

1. If outside a git repo, continue without branch creation and report it.
2. If inside a dirty git repo, stop before creating a branch or spec.
3. If clean, create or switch to `delivery/feature/<slug>` unless the user asked not to.

## Dirty State

Before edits, inspect status. Never revert user changes without explicit instruction.

If unrelated dirty changes exist, work around them. If they overlap the task, account for them or ask if they make progress unsafe.

## Commit Messages

Generate commit messages from staged diff only unless the user asks for unstaged changes too.
