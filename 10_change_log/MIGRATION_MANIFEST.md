Migration Manifest

Source notes split into this vault

RESEARCH_STRATEGY.md supplied the canonical research funnel, scoring
dimensions, reject criteria, and contribution types.

AI_WORKFLOW.md supplied AI role separation, evidence states, PDF reading
workflow, anti-hallucination rules, and artifact preferences.

REUSABLE_PROMPTS.md supplied the ten-stage prompt set. Topic-specific
parameters were removed from the reusable templates and preserved in the
project vault as an applied configuration.

The original source material is also retained unchanged in the combined
migration package under _original_source_snapshot so the migration can
be audited.

Release 04 -> Release 05 migration (2026-09-10)

Previous state: the feasibility-pilot gate and independent-replication
principle existed only as written policy, with no confirmed execution
anywhere in this system's project history.

New state: the companion Thesis Research Project executed the gate for
real once (not replicated yet). This migration:

1.  Added a new folder, `12_execution_validation/`, numbered to follow
    the existing `11_session_history/` without renaming or colliding
    with any prior folder.
2.  Rewrote [[../VERSION_BRIEF]], [[../README]], [[../RELEASE_HISTORY]]
    to reflect the new folder and the confirmed-vs-open distinction;
    superseded Release 04 wording is preserved as clearly labeled
    historical text within those files, not deleted.
3.  Appended (did not overwrite) status notes to
    [[../08_quality_gates/FEASIBILITY_PILOT_GATE]] and
    [[../08_quality_gates/INDEPENDENT_REPLICATION_VALIDATION]].
4.  Added [[../CURRENT_STATE]] at the repository root, which did not
    exist at Release 04.
5.  Left untouched: all governance, pipeline, evidence, AI-role, stage-
    contract, scoring, prompt, artifact, and publication material from
    Releases 01-04.

Reason: this system's own audit history (preserved in the companion
Thesis Research Project) explicitly flagged that post-v5 lessons should
be generalized here only once they had real execution evidence behind
them, not copied wholesale from thesis-specific content ahead of time.
Release 05 is that generalization step, done honestly - including
stating plainly what is still an open gap (independent replication)
rather than only reporting the success.

Compatibility: no folder was renamed, removed, or renumbered.

------------------------------------------------------------------------
