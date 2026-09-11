Reusable Research OS

1. Project Overview

Reusable Research OS is a topic-agnostic research workflow for moving
from an unfamiliar domain to a verified question, feasible experiment,
reproducible evidence trail, and publication-ready artifact. Release 05:
Feasibility Gate Validated in Practice records the first real execution
of the feasibility-pilot gate anywhere in this system's project history.

Start with [[VERSION_BRIEF]] for the human-readable history of this
release, and [[CURRENT_STATE]] for what is confirmed vs. still open.

2. Features

1.  Everything in Release 04.
2.  A feasibility-pilot gate confirmed by one real execution, not just
    documented as policy - see [[12_execution_validation/FEASIBILITY_FIRST_WORKFLOW_VALIDATED]].
3.  A concrete, generalized multimodal-synchronization principle drawn
    from a real defect a project caught using this workflow - see
    [[12_execution_validation/MULTIMODAL_SYNCHRONIZATION_PRINCIPLE]].
4.  An honest open-gap record for independent replication, which has
    not yet been exercised even once - see
    [[12_execution_validation/INDEPENDENT_REPLICATION_STATUS]].

3. Tech Stack

1.  Obsidian Markdown for graph-native research memory.
2.  Git/GitHub for diffs, tags, history, and releases.
3.  Primary-source literature as the final evidence authority.
4.  Python/Jupyter where validation or experimental tooling is required.
5.  External AI assistants only in scoped, provenance-tracked roles.

4. Architecture

    Research Goal --> Evidence Lock --> Dataset Gate --> Mini Feasibility Pilot --> Compact Feature Store --> Controlled Baselines --> Evaluation --> Release

This is a research/knowledge workflow, not a claim of an autonomous
software platform. See [ARCHITECTURE] and
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
7.  12_execution_validation/ — new at Release 05: reusable principles
    confirmed by real execution, plus honest open-gap tracking.

See [[RELEASE_HISTORY]], the project’s existing changelog/version
history, and [[GRAPH_AUDIT]].

------------------------------------------------------------------------
