# Research Harness Summary

## Core Objective

Improve the communication-performance frontier while preserving reproducibility and evaluation discipline.

## Durable Artifacts

- short root `AGENTS.md`
- `docs/` as the system of record
- dated experiment folders
- evaluation protocol
- results ledger
- literature notes

## Experiment Lifecycle

1. Choose one concrete hypothesis.
2. Create a dated experiment folder:
   - `YYYY-MM-DD_HH-MM_vNN_short-slug`
3. Write `PLAN.md` for collaboration and review.
4. Convert the agreed plan into `SPEC.md`.
5. Implement the smallest code change that tests the hypothesis.
6. Run smoke validation first.
7. Run matched comparison only after the path is stable.
8. Record outcomes in `RESULT.md` and the ledger.

## Evaluation Contract

Primary metrics:

- final test accuracy
- cumulative communication cost in MB

Secondary metrics:

- accuracy over rounds
- loss over rounds
- multi-SNR accuracy curve
- average and worst-case SNR performance
- seed mean and seed standard deviation

Guardrails:

- reproducibility of run configuration
- schema compatibility
- training stability
- interpretability of the claimed gain

## Evaluation Levels

- Level 0: static validation
- Level 1: smoke run
- Level 2: matched comparison
- Level 3: robustness evaluation

## Claim Rules

- Single-seed smoke results are not promotion evidence.
- Short runs can debug trends but should not decide winner claims if the canonical budget is longer.
- A change should only be promoted when it improves accuracy at equal or lower communication cost, or lowers communication cost with justified and negligible accuracy loss under matched conditions.

## Good Operating Habits

- keep docs synchronized with behavior
- prefer small, attributable diffs
- avoid bundled changes that break attribution
- use the repo itself as long-term memory for future agents
