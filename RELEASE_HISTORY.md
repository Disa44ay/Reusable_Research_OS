Public Release Mapping

The repositories preserve the original historical v1-v5 snapshots, but
the Git-facing public history is grouped into synchronized semantic
releases.

  -----------------------------------------------------------------------
  Public release          Historical basis        Milestone
  ----------------------- ----------------------- -----------------------
  Release 01              v1-v2 period            Foundation and Scope
                                                  Formation

  Release 02              v3                      Evidence-Driven
                                                  Candidate Validation

  Release 03              v4                      Scientific Lock and
                                                  Re-verification

  Release 04              v5 plus verified        Execution-Ready
                          post-v5 work through    Proposal and
                          2026-08-16              Feasibility

  Release 05              Release 04 plus         Feasibility Gate
                          generalized lessons     Validated in
                          from the companion      Practice
                          thesis project's
                          executed pilot,
                          2026-08-16 to
                          2026-08-20

  Release 06              Release 05 plus         Pre-Implementation
                          reusable principles     Gate Extension
                          generalized from the
                          companion thesis
                          project's Gate H
                          (compute feasibility)
                          and Gate E (multi-
                          match generalization)
                          pre-tasks, 2026-09-10
                          to 2026-09-17
  -----------------------------------------------------------------------

The public grouping does not erase the original version history.
Historical v1-v5 remain provenance checkpoints, while the public
releases are milestone labels for GitHub and synchronized project
communication.

See [[VERSION_BRIEF]] for the state represented by this snapshot.

## Release 06 note

Release 06 does not claim a new pipeline stage was added to the core
research workflow. It records that a gap left open at Release 05 — what
happens between a passed single-instance pilot and full-scale
implementation — was answered by a real, two-part pre-task, and
generalizes both parts as reusable steps in `13_gate_extension_validation/`.
The companion project's own execution details (dataset sizes, match
identifiers, exact timings) stay out of this repository by design; see
the Preservation notes in [[VERSION_BRIEF]] and
[[13_gate_extension_validation/PRE_IMPLEMENTATION_GATE_EXTENSION]].
