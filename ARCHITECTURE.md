# Architecture

## Status
Release 04 is the current documented operating system plus lightweight release-validation tooling. It is not an autonomous research platform.

## End-to-end flow

```text
Research goal
→ discovery
→ primary verification
→ adversarial evidence lock
→ dataset release + alignment gate
→ mini feasibility pilot
→ compact feature store
→ controlled baselines
→ full evaluation
→ concise research communication
→ Git release / publication
```

## Large-data execution pattern

```text
Large raw source
→ stream/process once
→ validate alignment
→ compact model-ready artifacts
→ repeated lightweight training
```

## Replication pattern

```text
Pinned pilot inputs
→ teammate A run
→ teammate B run
→ compare event counts / tensor shapes / windows / validator outputs
→ structural agreement required before scaling
```

## Main components

1. [[01_pipeline/LARGE_MULTIMODAL_DATA_PIPELINE]]
2. [[08_quality_gates/FEASIBILITY_PILOT_GATE]]
3. [[08_quality_gates/INDEPENDENT_REPLICATION_VALIDATION]]
4. [[02_evidence/SOURCE_RECONCILIATION_RULE]]
5. [[07_artifacts/CONCISE_PROPOSAL_AND_SOURCE_AUDIT_PATTERN]]
6. [[07_artifacts/GIT_READY_RESEARCH_RELEASE]]
