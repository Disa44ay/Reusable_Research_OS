---
type: reusable-principle
status: confirmed-by-one-real-execution
generalized_from: "companion Thesis Research Project, pre-implementation Gate E extension run"
related:
  - "[[PRE_IMPLEMENTATION_GATE_EXTENSION]]"
  - "[[../12_execution_validation/MULTIMODAL_SYNCHRONIZATION_PRINCIPLE]]"
---

# Multi-Instance Generalization Check

## The rule

A defect or pattern confirmed on one instance of a dataset (one file,
one match, one document, one session) is confirmed for that instance
only. Before treating it as a property of the dataset as a whole —
and especially before hard-coding a fixed correction for it — test it
against every other instance the project will actually use, not a
convenient subset.

## Why this needs to be a named rule rather than "test more later"

[[../12_execution_validation/MULTIMODAL_SYNCHRONIZATION_PRINCIPLE]]
already established, at Release 05, that two data sources sharing a
nominal frame rate can still be offset by a fixed amount. That was
confirmed on one match, one half. It would have been reasonable to
assume the same fixed offset applied everywhere and bake it into the
alignment code as a constant. A companion project instead re-ran the
same check across its full ten-match, twenty-half dataset before
implementation began, and found the offset was present in a little
over two-thirds of the halves and absent in the rest — not a universal
constant. The same extended check also surfaced an unrelated,
previously undocumented defect (a short but consistent tail of missing
video in roughly half the halves) that the single-instance pilot had no
opportunity to find, because it only touched one half.

## The validation step this principle requires

Before generalizing any single-instance finding into a project-wide
rule or a hard-coded constant:

1. Re-run the same check against every instance in the target
   population the project will actually use — not a sample chosen for
   convenience.
2. Report the check as a distribution across instances (present in N
   of M, absent in the rest), not as a single confirmed/not-confirmed
   verdict.
3. Treat any instance the check cannot classify (a partial or
   ambiguous result) as unresolved, not as passing by default.
4. Expect and record new findings the single-instance pilot could not
   have surfaced, since a larger population exercises code paths and
   edge cases the pilot never touched.
5. Only after this pass should a fixed constant, an exclusion list, or
   a per-instance correction table be written into shared pipeline
   code.

## What this looks like as a project-agnostic gate addition

This principle is the direct successor to
[[../12_execution_validation/MULTIMODAL_SYNCHRONIZATION_PRINCIPLE]]: that
principle established *how* to test alignment on one instance; this one
establishes that passing on one instance is a reason to test the rest,
not a reason to stop.

## Evidence status

Confirmed by one real execution, in one companion project, extending a
Release-05-era single-instance finding across a ten-item, twenty-unit
population. The extension changed the finding from "a fixed offset
exists" to "a fixed offset exists in most, but not all, instances, and
a second, previously unknown defect exists in about half" — a
materially different and more useful result than the single-instance
version. Treat as a strong candidate for a standard step whenever a
project moves from a pilot instance to full-population implementation.
