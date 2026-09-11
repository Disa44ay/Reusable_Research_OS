---
type: reusable-principle
status: confirmed-by-one-real-execution
generalized_from: "companion Thesis Research Project, Release 05"
related:
  - "[[../08_quality_gates/DATASET_RELEASE_AND_ALIGNMENT_GATE]]"
  - "[[FEASIBILITY_FIRST_WORKFLOW_VALIDATED]]"
---

# Multimodal Synchronization Principle

## The rule

When fusing two or more data sources that each carry their own implicit
or explicit time axis (video, sensor logs, tracking data, audio,
annotation timestamps), **do not assume that a shared nominal sample
rate implies a shared index space.** Two sources can report the same
frame rate, have nearly identical total frame/sample counts, and still
be offset from each other by a fixed amount because their respective
timelines start from different reference points.

## Why this needs to be a named rule rather than "use common sense"

A frame-count comparison alone is not sufficient evidence of alignment.
In the confirming instance (a companion project fusing tracking data
with video), two sources differed by only 0.04% in total frame count
(25 frames out of 67,650) — close enough that a count-only check could
easily be read as "basically matching, proceed." The actual cause was a
fixed one-second offset in one source's presentation timeline relative
to the other's declared zero point. A frame-count check would not have
caught this; a direct alignment test did.

## The validation step this principle requires

Before fusing any two timestamped modalities:

1. Do not rely on frame/sample count similarity as evidence of aligned
   clocks.
2. Independently establish each source's actual timestamp origin (e.g.,
   query the container/stream metadata for presentation timestamps;
   check whether an annotation format's time field is absolute or
   resets per segment).
3. Run a **direct, human-checkable overlay or comparison test** at a
   known reference point — for spatial data, this can be a visual
   overlay of one source's known positions onto the other source's
   frame at the claimed-matching index; for other modality pairs, an
   analogous ground-truth spot check. A first-principles empirical test
   beats a metadata-only check every time metadata could plausibly be
   wrong or ambiguous.
4. If a naive index-equality mapping and a timestamp-based mapping
   disagree, trust the timestamp-based mapping and treat the naive
   mapping as a rejected control, not a fallback.
5. Record the discovered offset (if any) explicitly, and do not assume
   it is a universal constant across every file in the dataset until
   checked on more than one instance.

## What this looks like as a project-agnostic gate addition

This principle sharpens, rather than replaces,
[[../08_quality_gates/DATASET_RELEASE_AND_ALIGNMENT_GATE]]: the existing
gate asks whether a dataset release/schema/alignment has been validated
at all; this principle specifies *how* to validate temporal alignment
between two timestamped modalities specifically, since count-matching is
an insufficient test that can pass while alignment is still wrong.

## Evidence status

Confirmed by exactly one real execution, in one companion project, on
one representative data file. Treat as a strong candidate for a
universal step in any future multimodal project's feasibility pilot,
not yet as a proven-across-many-domains law. If a future project applies
this principle and it does *not* catch anything, that is also useful
evidence and should be recorded rather than left unmentioned.

------------------------------------------------------------------------
