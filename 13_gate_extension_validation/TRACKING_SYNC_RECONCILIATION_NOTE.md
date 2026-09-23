---
type: reusable-principle
status: open-gap
generalized_from: "companion Thesis Research Project, dual claude.ai-Project / local-git-vault tracking setup"
related:
  - "[[PRE_IMPLEMENTATION_GATE_EXTENSION]]"
  - "[[../00_governance/MEMORY_AND_PERSISTENCE_POLICY]]"
---

# Tracking-System Reconciliation Note

## The situation this generalizes from

A companion project maintains two separate durable records of its own
state: a chat-based project workspace, and a local git-tracked vault on
the researcher's own machine with its own automated daily state check.
The automated check can only see what has been pushed to the git
remote. Work relayed directly in a chat session — including dated,
specific, measured results — can be real and current in the chat-based
record while the automated git-based check still reports the
corresponding gate as "not yet run," simply because nothing has been
pushed yet.

## The rule

When two durable tracking systems for the same project can disagree
because one of them can only observe a subset of where work actually
happens, do not let either system silently overrule the other. Record
both states explicitly, dated, side by side, and name the gap as a
sync item — not as a contradiction to resolve by picking a winner.

## Why this needs to be a named rule

The instinctive move is to trust whichever record is "more automated"
or "more recent," since that feels more objective. Both are wrong ways
to resolve this. An automated check that can only see a git remote is
not more truthful than a session-relayed record — it is differently
scoped. A chat-relayed record with specific dated numbers is not
automatically more truthful than an automated check either — it can be
stale relative to work that continued elsewhere. The only safe move is
to say what each record shows, as of when, and to flag the gap between
them explicitly until something (a push, a manual review, a diff) closes
it.

## The validation step this principle requires

1. When a project has more than one durable tracking surface, identify
   what each one can and cannot observe (e.g., "sees pushed commits
   only," "sees this conversation's own record only").
2. When they disagree on a status, state both, with their dates and
   scopes, rather than merging them into one claimed status.
3. Do not treat an automated check's silence about something ("no file
   with this name exists on the remote") as evidence the thing did not
   happen — only as evidence it has not been pushed there.
4. Name the specific action that would close the gap (a push, a
   file-by-file diff, a manual confirmation), and leave it open until
   that action is actually taken.

## What this looks like as a project-agnostic addition

This is a direct extension of
[[../00_governance/MEMORY_AND_PERSISTENCE_POLICY]]'s existing rule that
conversation context is a temporary working buffer and the vault is the
authoritative record — refined for the specific case of a project that
has *two* candidate authoritative records that can each be current in
their own scope and stale in the other's.

## Evidence status

Confirmed by one real, ongoing instance in a companion project: an
automated daily remote-check record and a session-relayed record of two
resolved feasibility gates disagree as of the date this was written, for
exactly the reason described above (nothing pushed yet). Both records
are preserved in the companion project rather than one overwriting the
other. Not yet tested on a project with more than two tracking
surfaces.
