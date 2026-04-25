# /idea

Shape an idea and classify the work level.

## Classification

- **Level 1: Task** - small bug, refactor, copy change, or narrow technical improvement.
- **Level 2: Feature** - user-visible feature, workflow, integration, or meaningful behavior change.
- **Level 3: Product** - new app, startup, commercial product, major pivot, or broad product strategy.

## Workflow

1. Read `_delivery/context/index.md` if present.
2. Load product and standards context only if they clarify the idea.
3. Classify level and state why.
4. Brainstorm practical scope, users, goals, non-goals, risks, and open questions.
5. Run research only if requested or clearly useful:
   - Level 1: rarely.
   - Level 2: when competitors, APIs, libraries, compliance, pricing, or current facts matter.
   - Level 3: usually.
6. Save `_delivery/ideas/<slug>.md`.
7. Save `_delivery/research/<slug>.md` only when research was actually performed.

## Artifact

Use `references/templates/idea.md`.

## Output

Summarize the level, saved artifact path, research decision, and recommended next command.
