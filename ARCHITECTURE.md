---
type: architecture
status: active
updated: 2026-09-22
note: "This file is a full rewrite for Release 06, describing the current architecture directly rather than as a diff against Release 05."
related:
  - "[[README]]"
  - "[[VERSION_BRIEF]]"
  - "[[13_gate_extension_validation/PRE_IMPLEMENTATION_GATE_EXTENSION]]"
---

# Architecture — Release 06 Update

## Updated flow

```
Research Goal --> Evidence Lock --> Dataset Gate --> Mini Feasibility Pilot
--> Pre-Implementation Gate Extension --> Compact Feature Store
--> Controlled Baselines --> Evaluation --> Release
```

The single new stage is **Pre-Implementation Gate Extension**, inserted
between the Mini Feasibility Pilot (confirmed at Release 04/05: one
instance, real execution, real evidence) and the Compact Feature Store /
Controlled Baselines stages (full-scale implementation).

## What the new stage requires

A project reaches this stage only after its feasibility pilot has
already passed on a single instance. It does not replace the pilot; it
sits after it. The stage has two parts, which a project may run in
parallel if it has the resourcing to split them:

1. **Compute-feasibility measurement** — run a real, representative
   pass of the heaviest planned processing stage and measure wall-clock
   time, memory, and accelerator usage directly, rather than budgeting
   compute from an assumption about which stage needs an accelerator.
   See [[13_gate_extension_validation/COMPUTE_FEASIBILITY_MEASUREMENT_PRINCIPLE]].
2. **Multi-instance generalization check** — re-run any alignment,
   offset, or defect check confirmed during the single-instance pilot
   against the full target population, and report it as a distribution
   across instances rather than a single verdict. See
   [[13_gate_extension_validation/MULTI_INSTANCE_GENERALIZATION_CHECK]].

Both parts produce evidence that can change the plan (a compute budget,
a hard-coded constant, an exclusion list) before that plan is written
into shared pipeline code.

## Why this sits before the Compact Feature Store stage, not inside it

Feature extraction and baseline training are the first stages that
consume compute and alignment assumptions at full scale. Placing the
gate extension immediately before them means a wrong compute budget or
an unverified single-instance offset is caught before it is paid for
across the whole dataset, not partway through.

## Stage ownership

Like the rest of this workflow, the Pre-Implementation Gate Extension is
a research-discipline stage, not a software component. It produces
Markdown evidence records and (optionally) small validation scripts; it
does not require a running service.

## Unchanged

Every other stage in the flow, the AI-role separation rules, the stage
contracts, and the quality gates are unchanged from Release 05. See the
existing `ARCHITECTURE.md` body (carried forward) for those sections.
