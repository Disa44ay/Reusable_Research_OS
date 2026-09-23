---
type: reusable-workflow
status: confirmed-by-one-real-execution
related:
  - "[[../08_quality_gates/FEASIBILITY_PILOT_GATE]]"
  - "[[../08_quality_gates/INDEPENDENT_REPLICATION_VALIDATION]]"
  - "[[COMPUTE_FEASIBILITY_MEASUREMENT_PRINCIPLE]]"
  - "[[MULTI_INSTANCE_GENERALIZATION_CHECK]]"
---

# Pre-Implementation Gate Extension

## What was policy going into Release 05

The feasibility-pilot gate (`08_quality_gates/FEASIBILITY_PILOT_GATE.md`)
asks a project to prove a pipeline on a small slice before spending paid
accelerator budget. Release 05 confirmed that gate once, on one match,
one half. It did not yet say what has to happen between "the pilot
passed on one instance" and "start full-matrix implementation."

## What was added at Release 06

A companion project used the Release 05 gate as a starting point, not an
end point, and split the remaining risk into two explicit, independently
owned pre-tasks before touching the mandatory model matrix:

1. A **resource-feasibility pre-task** — measure real wall-clock time,
   peak RAM, and peak accelerator usage instead of budgeting from a
   guess. See [[COMPUTE_FEASIBILITY_MEASUREMENT_PRINCIPLE]].
2. A **generalization pre-task** — take a finding confirmed on one
   instance (in this case, a fixed timestamp offset between two
   modalities) and test it against the rest of the target population
   before assuming it is a constant. See
   [[MULTI_INSTANCE_GENERALIZATION_CHECK]].

Both pre-tasks were written as short, self-contained scripts with a
named owner field, a required deliverable (a JSON/CSV artifact plus a
one-line verdict), and an explicit list of what the script can and
cannot conclude — so a partial or failed run is still a usable finding,
not a blocked pipeline.

## Why this is a gate-level addition and not just a thesis note

The single-instance feasibility pilot answers "can this be built at
all." It does not answer "what does it cost at scale" or "does the one
defect I found generalize." Treating a one-match pilot as license to
start the full matrix conflates those three questions. This addition
keeps them separate and requires each to be closed, individually, with
a dated artifact — before implementation begins.

## Evidence status

Confirmed by one real execution in the companion Thesis Research
Project, run as two parallel Colab pre-tasks ahead of the B0-B5
implementation phase. See the companion project's own record of the
measured results — this file states the reusable pattern only, per the
two-vault separation rule.

## What this does not yet confirm

Whether two-owner parallel pre-tasks are the right division of labor
for every project, or specific to a two-person execution team, is
untested outside this one instance.
