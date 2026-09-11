Architecture

Status

Release 05 is the current documented operating system plus lightweight
release-validation tooling. It is not an autonomous research platform.
As of this release, the feasibility-pilot gate below has been confirmed
by one real execution (in a companion project); the replication pattern
below remains policy only, with zero confirmed executions to date - see
[[12_execution_validation/FEASIBILITY_FIRST_WORKFLOW_VALIDATED]] and
[[12_execution_validation/INDEPENDENT_REPLICATION_STATUS]].

End-to-end flow

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

Large-data execution pattern

    Large raw source
    → stream/process once
    → validate alignment
    → compact model-ready artifacts
    → repeated lightweight training

Replication pattern

    Pinned pilot inputs
    → teammate A run
    → teammate B run
    → compare event counts / tensor shapes / windows / validator outputs
    → structural agreement required before scaling

Main components

1.  [[01_pipeline/LARGE_MULTIMODAL_DATA_PIPELINE]]
2.  [[08_quality_gates/FEASIBILITY_PILOT_GATE]]
3.  [[08_quality_gates/INDEPENDENT_REPLICATION_VALIDATION]]
4.  [[02_evidence/SOURCE_RECONCILIATION_RULE]]
5.  [[07_artifacts/CONCISE_PROPOSAL_AND_SOURCE_AUDIT_PATTERN]]
6.  [[07_artifacts/GIT_READY_RESEARCH_RELEASE]]
7.  [[12_execution_validation/MULTIMODAL_SYNCHRONIZATION_PRINCIPLE]] -
    new at Release 05.

------------------------------------------------------------------------
