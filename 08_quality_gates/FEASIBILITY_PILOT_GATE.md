Feasibility Pilot Gate

Before consuming a limited paid accelerator budget, prove the complete
raw-to-prediction pipeline on a small slice.

Required pilot outputs

-   pinned data manifest
-   compact structured tensor
-   frozen visual feature file
-   aligned event table
-   training/evaluation window manifest
-   a tiny trained checkpoint
-   resource usage log
-   sample predictions

Required checks

1.  Raw structured data can be streamed without whole-file loading.
2.  Temporal alignment works across all modalities.
3.  Raw video can be sampled and converted to frozen features.
4.  Training loss is finite and decreases on a tiny run.
5.  Predictions contain the correct output schema.
6.  Actual runtime/storage/memory measurements can be extrapolated
    conservatively.

A feasibility pilot is not evidence of scientific performance. It is
evidence that the intended experiment can be executed within resource
constraints.

Release 05 confirmation note (2026-09-10)

This gate was exercised for real for the first time in this system's
project history, by the companion Thesis Research Project, on match
117093 of a multimodal football dataset. The pilot surfaced a genuine
defect (a fixed presentation-timestamp offset between two modalities
nominally at the same frame rate) that a frame-count-only check would
not have caught, and reached a scoped GO decision after resolving it.
See `Reusable_Research_OS/12_execution_validation/FEASIBILITY_FIRST_WORKFLOW_VALIDATED.md`
for the generalized account. This confirms the gate's design intent but
is one execution, not a general proof; the gate's required checks above
are unchanged.

------------------------------------------------------------------------
