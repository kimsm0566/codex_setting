# Experiments Directory

This directory is organized by research attempt.

## Folder Naming Rule

Use this pattern:

- `YYYY-MM-DD_HH-MM_vNN_short-slug`

Examples:

- `2026-04-03_22-00_v01_reasoning-triggered-comm`
- `2026-04-05_09-10_v02_mask-overhead-recheck`

## Standard Files

Each substantial experiment folder should usually contain:

- `PLAN.md`
  - collaboration-first draft before execution
- `SPEC.md`
  - agreed fixed conditions and validation path
- `WORKLOG.md`
  - commands, progress notes, blockers, decisions
- `RESULT.md`
  - current or final outcome

## Lifecycle

1. Create the folder.
2. Draft `PLAN.md`.
3. Review and refine the plan.
4. Convert the agreed plan into `SPEC.md`.
5. Run smoke validation first.
6. Run matched comparison only after the path is stable.
7. Record the outcome in `RESULT.md` and `RESULTS_LEDGER.md`.

## Language Policy

- Write new experiment artifacts in Korean by default unless the project explicitly uses another convention.
- Keep file and folder names ASCII-friendly.
