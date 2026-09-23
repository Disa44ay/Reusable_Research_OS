---
type: reusable-principle
status: confirmed-by-one-real-execution
generalized_from: "companion Thesis Research Project, pre-implementation Gate H run"
related:
  - "[[PRE_IMPLEMENTATION_GATE_EXTENSION]]"
  - "[[../08_quality_gates/FEASIBILITY_PILOT_GATE]]"
---

# Compute Feasibility Measurement Principle

## The rule

A compute budget written before any real run is a guess, not a
measurement. Before committing a project's paid-accelerator budget to a
full experiment matrix, run one representative unit through the actual
pipeline and record real wall-clock time, peak RAM, and peak accelerator
utilization — then extrapolate from that number, labeled clearly as an
extrapolation, rather than from an assumed per-unit cost.

## Why this needs to be a named rule

A project's own planning rule can reserve a large share of its
accelerator budget for a processing stage on the assumption that the
stage is accelerator-bound. A single measured run can show the opposite
— that the accelerator sits idle for nearly the entire run because the
bottleneck is elsewhere (I/O, single-threaded parsing, an artifact
serialization step). Budgeting from the untested assumption would have
reserved paid compute for a stage that, measured, cost close to zero.
The gap between "how the pipeline is described" and "where the wall
clock actually goes" is not visible without an instrumented run.

## The validation step this principle requires

Before allocating accelerator budget to a pipeline stage:

1. Instrument one full representative unit (one match, one document,
   one batch — whatever the project's natural unit is) end to end, not
   a synthetic microbenchmark.
2. Record wall-clock time per stage, peak RAM, and peak
   accelerator (GPU/TPU) utilization, not just total elapsed time.
3. Separate accelerator-bound stages from everything else. A stage that
   shows near-zero accelerator utilization across a full run is a CPU
   or I/O bottleneck, not an accelerator cost, however the pipeline was
   originally described.
4. Extrapolate the full-matrix cost from the measured per-unit cost,
   and label it explicitly as an extrapolation — it is not a second
   measurement.
5. Re-plan the budget split (accelerator-bound work vs. CPU-only work)
   against the measured numbers, not the original plan.

## What this looks like as a project-agnostic gate addition

This principle sharpens
[[../08_quality_gates/FEASIBILITY_PILOT_GATE]]: the existing gate asks
whether the pipeline runs at all; this principle asks specifically
whether the *cost* of running it was measured or assumed, since a
pipeline that runs correctly can still be budgeted incorrectly.

## Evidence status

Confirmed by one real execution, in one companion project, on one
representative processing unit. The measured result there showed the
accelerator-bound stage in that pipeline consuming a small fraction of
the run's wall-clock time, with the rest of the pipeline running
correctly on CPU alone — the opposite of the original budget
assumption. Treat as a strong candidate for a standard step before any
accelerator-budget allocation, not yet as proven across many domains.
