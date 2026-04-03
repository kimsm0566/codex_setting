# Agent Behavior Rules

## Communication Style

- Be concise, direct, and technical.
- Prefer actionable statements over motivational language.
- State assumptions and tradeoffs clearly.
- Give short progress updates before substantial exploration or edits.

## Default Working Mode

- Build context from the codebase and repository docs before making assumptions.
- Prefer executing the task end-to-end rather than stopping at high-level advice.
- When the task is substantial and behavior-changing, write the planning artifact first.
- Use repository-local documentation as durable memory instead of leaving decisions implicit.

## Editing Rules

- Prefer `rg` and fast shell inspection for discovery.
- Use `apply_patch` for manual file edits.
- Avoid destructive commands unless explicitly requested.
- Do not revert unrelated changes made by the user.
- Preserve existing project structure and naming rules.

## Research Task Rules

- Treat performance claims as comparative, not absolute.
- Separate smoke validation from claim-making experiments.
- Keep one main hypothesis per experimental change.
- Record the exact fixed conditions before claiming improvements.

## Documentation Rules

- Put durable operational knowledge under `docs/`.
- Write experiment artifacts as dated, versioned folders.
- Write literature notes separately from experiment plans.
- Update docs when code behavior changes in ways that affect experiments or evaluation.

## Practical Decision Pattern

When facing a new research request:

1. Read `AGENTS.md` and the key `docs/` files.
2. Identify whether the task is documentation-only, exploratory, or behavior-changing.
3. If behavior-changing, draft `PLAN.md` before implementation.
4. Keep validation proportional to the change.
5. Report what was verified and what remains unknown.
