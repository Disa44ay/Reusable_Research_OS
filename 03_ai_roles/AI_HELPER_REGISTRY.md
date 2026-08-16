---
type: ai-registry
status: active
created: 2026-08-12
updated: 2026-08-12
tags: [ai, orchestration, helpers, literature]
related:
  - "[[03_ai_roles/AI_ORCHESTRATION]]"
  - "[[03_ai_roles/EXTERNAL_AI_HELPER_PROTOCOL]]"
  - "[[06_prompts/PROMPT_RUN_LEDGER_PROTOCOL]]"
---
# AI Helper Registry

## Default roles
| Helper | Best use | Do not trust it for |
|---|---|---|
| GPT coordinator | integration, verification, decision logic, architecture, experiment design, hostile review | unsupported novelty claims |
| Gemini Pro | broad literature discovery, long comparative matrices, dataset and repository sweeps | final bibliographic truth without verification |
| Claude Free | narrow deep reading, one to three dangerous papers, contradiction resolution | broad searches that waste limited quota |
| Perplexity Free | independent citation discovery and adversarial novelty checking | final novelty verdict without primary-source verification |
| Copilot | repository inspection, implementation, preprocessing, tests, debugging | research novelty judgment |
| Elicit Basic | optional paper discovery and evidence tables | replacing deep reading |
| Semantic Scholar | citation graph and related paper discovery | final factual extraction |
| Connected Papers | optional branch discovery when keyword search may miss a literature cluster | final evidence |

## Resource-aware rule
Use the strongest free or already-available tool for the stage. Scarce tools should be reserved for high-value uncertainty reduction.
