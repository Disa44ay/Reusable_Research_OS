---
type: workflow
status: active
tags: [ai, orchestration, research]
updated: 2026-08-09
---
# AI Orchestration

The project originally assigned tools by role. Treat these as workflow defaults, not scientific evidence and not permanent claims about product capability.

## Discovery role, originally Gemini Pro
Use for broad research landscape, dataset discovery, paper discovery, recent literature search, link collection, and initial comparative tables.

## Deep-reading role, originally Claude
Use for actual PDF or paper reading, systematic literature matrices, limitation extraction, gap validation, synthesis across papers, scientific writing, and paper-quality critique.

Never ask the deep-reading role to invent missing evidence.

## Synthesis role, originally GPT
Use for integrating verified findings, topic scoring, architecture, experiment design, implementation planning, and reviewer-style critique.

## Coding role, originally GitHub Copilot
Use after architecture and research contribution are fixed. Ask for module implementation, tests, refactoring, debugging, and documentation. Do not delegate final topic selection to a coding assistant.

## Deep PDF workflow
1. Identify the exact paper from title and authors.
2. Use an official, DOI, publisher, or arXiv source.
3. Read the actual paper.
4. Extract structured evidence.
5. Quote only when necessary.
6. Distinguish paper claims from inference.
7. Record dataset access.
8. Record compute implications.
9. Extract explicit limitations and future work.
10. Assign confidence or evidence state.

## Handoff rule
Each AI stage must consume structured artifacts from the prior stage instead of relying on a long chat transcript.
