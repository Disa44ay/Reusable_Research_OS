---
type: quality-gate
status: active
created: 2026-08-14
updated: 2026-08-14
tags: [feasibility, pilot, compute-budget, go-no-go]
related:
  - "[[QUALITY_GATES]]"
  - "[[DATASET_RELEASE_AND_ALIGNMENT_GATE]]"
  - "[[../07_artifacts/GIT_READY_RESEARCH_RELEASE]]"
---
# Feasibility Pilot Gate

Before consuming a limited paid accelerator budget, prove the complete raw-to-prediction pipeline on a small slice.

## Required pilot outputs
- pinned data manifest
- compact structured tensor
- frozen visual feature file
- aligned event table
- training/evaluation window manifest
- a tiny trained checkpoint
- resource usage log
- sample predictions

## Required checks
1. Raw structured data can be streamed without whole-file loading.
2. Temporal alignment works across all modalities.
3. Raw video can be sampled and converted to frozen features.
4. Training loss is finite and decreases on a tiny run.
5. Predictions contain the correct output schema.
6. Actual runtime/storage/memory measurements can be extrapolated conservatively.

A feasibility pilot is not evidence of scientific performance. It is evidence that the intended experiment can be executed within resource constraints.
