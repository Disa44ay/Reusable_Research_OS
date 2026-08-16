---
type: prompts
status: active
tags: [prompts, reusable, research-os]
updated: 2026-08-09
---
# Reusable Prompt Library

These templates are the topic-agnostic form of the original research prompts. Replace bracketed variables with the active project's constraints. Store the filled project configuration in the project vault.

## Prompt 1. Research landscape
Act as a senior research advisor. Do not suggest final topics yet. Identify and compare promising research domains suitable for [team profile], [compute budget], [dataset policy], [research depth], [implementation balance], [execution window], [portfolio goals], and [publication objective]. For each domain report description, research trend, publication activity, industry relevance, public datasets, baselines, metrics, code, compute, future directions, multimodal opportunities, and feasibility. Separate verified facts from estimates. Provide primary or official links where possible.

## Prompt 2. Dataset discovery
For the shortlisted domains, identify major public datasets. For every dataset provide exact name, official link, access method, size, modalities, classes, labels, annotation quality, benchmark papers, implementations, license, strengths, weaknesses, publication usefulness, implementation difficulty, compute, and industry relevance. Do not invent dataset statistics. If a field cannot be verified, write UNKNOWN.

## Prompt 3. Literature collection
Find important foundational and recent papers for the selected domains. Return title, authors, year, venue, DOI or official link, dataset, model, code, research problem, major contribution, limitation, and future work. Do not fabricate citation counts.

## Prompt 4. Literature matrix
Read the actual papers, not summaries. For every paper extract exact citation, problem, dataset, modalities, methodology, architecture, loss, metrics, baseline, result, strengths, weaknesses, limitations, explicit future work, code, compute, novelty, publication quality, and relevance to project constraints. Label every important claim as DIRECTLY STATED, INFERRED, or UNKNOWN. Never invent missing information.

## Prompt 5. Gap validation
Based only on the verified literature matrix, identify genuine research gaps. Recommend a gap only when supported by multiple papers or explicit recent future work, testable on public data, feasible under the compute and team constraints, and objectively evaluable. For every gap provide evidence papers, evidence type, problem, current failure mode, proposed direction, novelty risk, implementation effort, compute, publication potential, engineering opportunity, and remaining unknowns.

## Prompt 6. Topic selection
Using only verified literature, datasets, and validated gaps, generate candidate research topics. Score novelty, publication potential, dataset availability, compute feasibility, execution-window feasibility, implementation value, engineering opportunity, learning value, multimodal value, industry relevance, reproducibility, and risk. Reject weak ideas. Do not lock a topic while a critical assumption remains unverified.

## Prompt 7. Architecture
For the selected validated topic, design a production-quality system including ingestion, ETL, preprocessing, training, inference, API, authentication if needed, database, caching if justified, experiment tracking, logging, dashboard, deployment, and repository structure. Keep the system proportional to the real project scope.

## Prompt 8. Experiment plan
Design baselines, proposed method, metrics, ablations, hyperparameters, training schedule, compute estimate, risks, error analysis, expected outputs, tables, figures, and reproducibility plan. Do not promise expected numerical improvements.

## Prompt 9. Harsh reviewer
Act as a harsh scientific reviewer. Evaluate novelty, literature grounding, research gap, methodology, dataset validity, baseline fairness, experiments, statistical validity, ablations, reproducibility, writing, figures, tables, and likely reviewer objections. Recommend concrete fixes.

## Prompt 10. Paper writing
Using only verified experimental results and citations, write the manuscript in the required venue style. Do not fabricate results. Do not exaggerate novelty. Flag missing citations and weak arguments. Preserve scientific uncertainty.
