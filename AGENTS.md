# AGENTS.md

## Mission

This repository should support research that improves the communication-performance trade-off under communication constraints.

Primary objective:

- increase or preserve task performance while reducing communication cost

Secondary objective:

- improve robustness across channel conditions, SNR regimes, and random seeds

Treat all performance claims as comparative. A change is only an improvement if it beats a matched baseline under controlled conditions.

## How To Use This File

- Use this file as the short entry point, not the full manual.
- Keep detailed process, experiment, and evaluation guidance under `docs/`.
- Keep Markdown documentation under `docs/`, not under `src/`, unless there is a strong reason not to.

## Repository Reality

- Code should live under `src/`.
- Documentation should live under `docs/`.
- If documentation and code disagree, trust observable code behavior and update the relevant docs in the same task.

## Read First

- `docs/agent_behavior_rules.md`
- `docs/research_harness_summary.md`

## Research Workflow

1. Start from a clear hypothesis.
2. For substantial experiments or behavior-changing code work, use a dated, versioned folder under `docs/experiments/`.
3. Draft `PLAN.md` before execution so the user can review and refine the approach.
4. After alignment, write or update `SPEC.md` with agreed fixed conditions and validation path.
5. Make the smallest code change that tests one concrete idea.
6. Run the smallest feasible validation before broad sweeps.
7. Record meaningful runs in a results ledger.
8. Report wins, regressions, and unknowns.

## Reproducibility Rules

When changing training or evaluation logic, preserve or explicitly re-document:

- dataset
- partition type
- number of clients
- client data size
- batch size
- number of local epochs
- number of rounds
- algorithm
- model type
- channel type
- training SNR or SNR range
- compressed dimension
- pruning threshold
- beta schedule
- seed set
- result path

Do not silently change defaults that would invalidate earlier comparisons.

## Evaluation Rules

- Do not claim improvement from a single-seed run unless the task is explicitly a smoke test.
- Always report communication cost with accuracy.
- Prefer matched comparisons with the same seed set and run budget.
- If fixed conditions differ from the baseline, label the run exploratory rather than claim-making.

## Validation Expectations

- Docs-only changes: verify links, paths, and cross-references.
- Python changes: run `python -m py_compile` on touched files.
- Training or eval logic changes: run the smallest feasible smoke check and state exactly what was and was not validated.

## Documentation Policy

- `AGENTS.md` should stay short and stable.
- Detailed operational knowledge belongs in `docs/`.
- Plans are first-class artifacts.
- Keep file and folder names ASCII-friendly even when document bodies are written in Korean.
