# Generative AI Track (`tracks/generative-ai/`)

Place your Cohort 02 Generative AI modules—bilingual RAG pipelines, AI Agents, MCP tools, safety guardrails, and evaluation harnesses—here.

## Suggested Structure
- `tracks/generative-ai/<issue-slug>/`
  - `src/` — Modular RAG, Agent, or Guardrail implementations
  - `tests/` — `pytest` unit tests (including non-medical-advice & prompt-injection checks)
  - `README.md` — Architecture notes, evaluation metrics, and reproducible setup

> **Guardrail Reminder:** Any assistant using pharmaceutical data must strictly refuse medical diagnosis, prescribing, or dosage advice. See [`../../CONTRIBUTING.md`](../../CONTRIBUTING.md).
