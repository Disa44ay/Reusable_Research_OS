Reusable Research OS

1. Project Overview

Reusable Research OS is a topic-agnostic research workflow for moving
from an unfamiliar domain to a verified question, feasible experiment,
reproducible evidence trail, and publication-ready artifact. Release 06:
Pre-Implementation Gate Extension records two pre-tasks a companion
project ran between its Release 05 feasibility pilot and the start of
its mandatory model matrix — measuring real compute cost, and testing a
single-instance finding against its full target population.

Start with [[VERSION_BRIEF]] for the human-readable history of this
release, and [[CURRENT_STATE]] for what is confirmed vs. still open.

2. Features

1.  Everything in Release 05.
2.  A compute-feasibility measurement principle: budget from a measured
    run, not an assumption — see
    [[13_gate_extension_validation/COMPUTE_FEASIBILITY_MEASUREMENT_PRINCIPLE]].
3.  A multi-instance generalization check: a single-instance finding is
    not a population-wide rule until tested against the full target
    set — see
    [[13_gate_extension_validation/MULTI_INSTANCE_GENERALIZATION_CHECK]].
4.  A tracking-sync reconciliation principle for projects that keep more
    than one durable state record — see
    [[13_gate_extension_validation/TRACKING_SYNC_RECONCILIATION_NOTE]].

3. Tech Stack

1.  Obsidian Markdown for graph-native research memory.
2.  Git/GitHub for diffs, tags, history, and releases.
3.  Primary-source literature as the final evidence authority.
4.  Python/Jupyter where validation or experimental tooling is required.
5.  External AI assistants only in scoped, provenance-tracked roles.

4. Architecture

    Research Goal --> Evidence Lock --> Dataset Gate --> Mini Feasibility Pilot --> Pre-Implementation Gate Extension --> Compact Feature Store --> Controlled Baselines --> Evaluation --> Release

This is a research/knowledge workflow, not a claim of an autonomous
software platform. See [[ARCHITECTURE]] and
[[01_pipeline/END_TO_END_PIPELINE]].

5. Project Structure

The established numbered folders are preserved. Key entry points are:

1.  00_governance/ — research rules and knowledge governance.
2.  01_pipeline/ — end-to-end workflow.
3.  02_evidence/ — evidence and verification rules.
4.  03_ai_roles/ — AI orchestration where present in this release.
5.  04_stage_contracts/ to 09_publication/ — stage exits, scoring,
    prompts, artifacts, quality gates, and publication.
6.  10_change_log/ and 11_session_history/ — provenance and
    chronological evolution.
7.  12_execution_validation/ — Release 05: reusable principles
    confirmed by real execution, plus honest open-gap tracking.
8.  13_gate_extension_validation/ — new at Release 06: the
    pre-implementation gate-extension pattern, compute-measurement
    principle, multi-instance generalization check, and tracking-sync
    reconciliation note.

See [[RELEASE_HISTORY]], the project's existing changelog/version
history, and [[GRAPH_AUDIT]].
