---
name: agent-delivery-workflow
description: Full software delivery workflow for AI coding agents. Use when the user invokes /setup-project, /idea, /spec, /design, /plan, /implement, /review, /status, or /commit-message; asks for Spec Driven Development; wants project setup, feature shaping, implementation planning, execution, review, or commit support.
---

# Agent Delivery Workflow

Use this skill as a lightweight orchestrator for the software lifecycle. It chooses the right rigor level, loads only the context needed for the command, and routes to specialized capabilities when they add clear value.

## Core Model

- **Level 1: Task** - bugs, small changes, refactors. Flow: intent -> mini-plan -> implement -> review.
- **Level 2: Feature** - normal product features. Flow: idea -> spec -> optional design -> plan -> implement -> review.
- **Level 3: Product** - new apps, commercial products, major pivots. Flow: setup -> idea -> research -> product context -> roadmap -> specs -> designs -> plans.

Levels describe the work. Capabilities are optional tools selected by the orchestrator.

## Persistent Context

Read `_delivery/context/index.md` first when present. It should point to the relevant context files:

```text
_delivery/context/
  index.md
  product.md
  tech.md
  standards.md
  decisions.md
  skills.md
```

Do not load every long context file by default. Load only what the active command needs.

## Artifacts

Create artifacts only when useful for the level and command:

```text
_delivery/ideas/<slug>.md
_delivery/research/<slug>.md
_delivery/specs/<slug>.md
_delivery/designs/<slug>.md
_delivery/plans/<slug>.md
_delivery/reviews/<slug>.md
```

## Command Routing

Treat these user messages as command invocations:

- `/setup-project` -> read `references/commands/setup-project.md`
- `/idea <idea>` -> read `references/commands/idea.md`
- `/spec <slug-or-idea>` -> read `references/commands/spec.md`
- `/design <slug>` -> read `references/commands/design.md`
- `/plan <slug>` -> read `references/commands/plan.md`
- `/implement <slug>` -> read `references/commands/implement.md`
- `/review <slug>` -> read `references/commands/review.md`
- `/status` -> read `references/commands/status.md`
- `/commit-message` -> read `references/commands/commit-message.md`

The text after the command name is `$ARGUMENTS`. If the user asks in natural language, choose the matching command and level.

## Capability Routing

Read capability guidance only when relevant:

- Research: `references/capabilities/research.md`
- UX design: `references/capabilities/ux-design.md`
- Visual design: `references/capabilities/visual-design.md`
- External skills: `references/capabilities/external-skills.md`
- Git discipline: `references/capabilities/git.md`

Do not install external skills automatically. If a useful skill is missing, recommend it and use the internal fallback.

## Global Rules

- Keep `SKILL.md` small; put detailed workflows in `references/commands/*.md`.
- Do not make every phase mandatory.
- Do not create every folder/file for every task.
- Stop on dirty git state before creating a new feature branch.
- Use feature branches named `delivery/feature/<slug>` when `/spec` runs in a clean git repo.
- Generate commit messages from staged changes.
- Do not overwrite user changes.
