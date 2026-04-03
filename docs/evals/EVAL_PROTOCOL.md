# Evaluation Protocol

This file defines how to evaluate changes without overstating results.

## Evaluation Objective

The target is not accuracy alone.

Canonical evaluation asks:

- does a change improve the communication-performance frontier?
- does the gain hold under matched experimental conditions?
- does the gain survive variation across seeds and channel conditions?

## Primary Metrics

- final test accuracy
- cumulative communication cost in MB

## Secondary Metrics

- accuracy over rounds
- loss over rounds
- multi-SNR accuracy curve
- average and worst-case SNR performance
- seed mean and seed standard deviation

## Evaluation Levels

- Level 0: static validation
- Level 1: smoke run
- Level 2: matched comparison
- Level 3: robustness evaluation

## Comparison Contract

Do not compare runs as if they were equivalent when any of the following changed without being explicitly controlled for:

- default hyperparameters
- result schema
- data partition semantics
- evaluation behavior
- seed set
- communication accounting logic

## Claim Language

- smoke only: "runs successfully" or "promising"
- single matched run: "candidate improvement"
- repeated matched runs with stable gains: "supported improvement"

Avoid strong claim language when the comparison contract is not satisfied.
