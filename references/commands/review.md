# /review

Review the implementation against context, spec, design, and plan.

## Workflow

1. Inspect git status and diff.
2. Read `_delivery/context/index.md` if present.
3. Load standards and tech context relevant to the diff.
4. Read `_delivery/specs/<slug>.md` and `_delivery/plans/<slug>.md` when a slug is supplied.
5. Read `_delivery/designs/<slug>.md` when the diff touches UI/UX.
6. Review only evidence in the diff unless the user asks for broader analysis.
7. Create `_delivery/reviews/` if a slug is supplied or the user asks to save the review.
8. Save `_delivery/reviews/<slug>.md` using `references/templates/review.md` when applicable.

## Review Standard

Findings first, ordered by severity. Focus on:

- Bugs and behavioral regressions.
- Missing requirements.
- Security, privacy, and data integrity risks.
- Accessibility and responsive UI issues.
- Missing or weak tests.
- Maintainability issues that affect the changed behavior.

If no issues are found, say so and note residual risk or test gaps.

## Output

Return findings with file and line references where possible, then open questions, then a brief summary.
