---
name: GenAI Track Task
about: Propose or assign a Generative AI engineering task for Cohort 02
title: "[GenAI] "
labels: track:genai, cohort-02
assignees: ""
---

## Objective
<!-- Clear engineering goal (e.g., bilingual Arabic/English RAG retriever, MCP tool, guardrail layer, eval suite). -->

## Scope & Architecture
- Components involved: <!-- Retriever / Reranker / Agent / MCP Server / Guardrails / Evaluator -->
- Dataset / Knowledge Base: `DrugShift × Phronesis Educational Snapshot v1` (or specify)

## Acceptance Criteria
- [ ] Clean modular code inside `tracks/generative-ai/<module>/`
- [ ] Zero hardcoded API keys (`.env.example` provided)
- [ ] Handles both Arabic and English queries (including common Egyptian spelling variations)
- [ ] Strict **non-medical-advice guardrail** tested against adversarial diagnosis/dosage prompts
- [ ] Evaluation script reporting accuracy/faithfulness and latency on at least 20 test cases

## Rubric Focus
- Retrieval quality, guardrail reliability, and measurable evaluation results.
