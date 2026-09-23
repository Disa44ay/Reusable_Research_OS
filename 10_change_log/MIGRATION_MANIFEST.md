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

# Migration Manifest — Release 06 Addition

## Old structure (Release 05)

```
Reusable_Research_OS/
├── 00_governance/ ... 12_execution_validation/
├── docs/diagrams/workflows/feasibility_gate_confirmed_r05.md
├── ARCHITECTURE.md
├── CURRENT_STATE.md
├── FILE_INTEGRITY_SHA256.txt
├── GRAPH_AUDIT.md
├── README.md
├── RELEASE_HISTORY.md
└── VERSION_BRIEF.md
```

## New structure (Release 06)

```
Reusable_Research_OS/
├── 00_governance/ ... 12_execution_validation/         (unchanged)
├── 13_gate_extension_validation/                        (NEW)
│   ├── PRE_IMPLEMENTATION_GATE_EXTENSION.md
│   ├── COMPUTE_FEASIBILITY_MEASUREMENT_PRINCIPLE.md
│   ├── MULTI_INSTANCE_GENERALIZATION_CHECK.md
│   └── TRACKING_SYNC_RECONCILIATION_NOTE.md
├── docs/diagrams/workflows/
│   ├── feasibility_gate_confirmed_r05.md                (unchanged)
│   └── gate_extension_confirmed_r06.md                  (NEW)
├── ARCHITECTURE.md                                       (rewritten)
├── CURRENT_STATE.md                                      (rewritten)
├── FILE_INTEGRITY_SHA256.txt                             (regenerated)
├── GRAPH_AUDIT.md                                        (rewritten)
├── README.md                                             (rewritten)
├── RELEASE_HISTORY.md                                    (new row)
└── VERSION_BRIEF.md                                      (rewritten)
```

## Migration path

1. No folder was renamed, moved, or removed. `13_gate_extension_validation/`
   is a new sibling folder using the next free top-level number after
   `12_execution_validation/`, following the same numbering convention
   established at Release 04/05.
2. No content inside `00_governance/` through `12_execution_validation/`
   changed. A Release 05 checkout remains valid; Release 06 only adds to
   it.
3. Root-level files listed as "rewritten" above replace the equivalent
   Release 05 file in full; their Release 05 versions remain readable
   inside `Reusable_Research_OS_Release_05_COMPLETE_CONTEXT.txt`.

## Compatibility considerations

- Any external link or reference to a Release 05 path
  (`12_execution_validation/...`, `docs/diagrams/workflows/feasibility_gate_confirmed_r05.md`)
  continues to resolve unchanged.
- New wikilinks introduced at Release 06 point only to files that exist
  in this release; see `GRAPH_AUDIT.md` for the re-audit.
- `FILE_INTEGRITY_SHA256.txt` at Release 06 lists a hash for every file
  in this complete Release 01-06 snapshot, including files unchanged
  since earlier releases; see `HOW_TO_VERIFY_RELEASE_06_PACKAGES.md`.
