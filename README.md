# Agent Delivery Workflow

Portable software delivery workflow skill for AI coding agents.

This repository packages a lightweight workflow for shaping ideas, writing specs, planning implementation, executing changes, reviewing work, checking status, and drafting commit messages. It is designed to be agent-agnostic: agents should load `SKILL.md`, then route detailed commands through the markdown files under `references/`.

## Structure

```text
SKILL.md
agents/openai.yaml
references/commands/
references/capabilities/
references/templates/
```

## Workflow

The skill uses `_delivery/` inside the target project for persistent context and generated artifacts:

```text
_delivery/context/
_delivery/ideas/
_delivery/research/
_delivery/specs/
_delivery/designs/
_delivery/plans/
_delivery/reviews/
```

For feature work, `/spec` creates or switches to `delivery/feature/<slug>` when the git repository is clean.

## Commands

- `/setup-project` initializes persistent delivery context.
- `/idea <idea>` shapes and classifies work.
- `/spec <slug-or-idea>` creates or updates a spec.
- `/design <slug>` creates a focused UI/UX design artifact when useful.
- `/plan <slug>` creates an implementation plan.
- `/implement <slug>` executes an accepted plan.
- `/review <slug>` reviews implementation against artifacts and context.
- `/status` summarizes active delivery state.
- `/commit-message` drafts a commit message from staged changes.

## Distribution Notes

- `name: agent-delivery-workflow`
- Display name: `Agent Delivery Workflow`
- Persistent project workspace: `_delivery/`
- Feature branches: `delivery/feature/<slug>`
- The workflow is intended for any AI coding agent that can read markdown instructions and project files.
