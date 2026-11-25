# Phronesis Open-Source Lab — Cohort 02 (Winter 2026)

[![Built at Phronesis](https://img.shields.io/badge/Built%20at-Phronesis-23453A?style=flat-square)](https://phronesis-tech.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-5F766D?style=flat-square)](LICENSE)

Welcome to the official open-source engineering lab for **Phronesis Cohort 02 (Winter 2026)**. Instead of toy Kaggle notebooks, fellows collaborate via real GitHub Issues, feature branches, automated checks, and instructor-led Pull Request reviews using real Egyptian market datasets (such as the **DrugShift × Phronesis Educational Snapshot**).

## Repository Structure

```text
cohort-02-open-lab/
├── data/
│   ├── README.md                 # Dataset schema, license, and medical/usage disclaimers
│   └── sample/                   # Small public sample CSV for local testing
├── tracks/
│   ├── machine-learning/         # EDA, feature pipelines, XGBoost/LightGBM models, FastAPI services
│   └── generative-ai/            # Bilingual RAG, Agents & MCP tools, Guardrails & Eval harnesses
├── evals/                        # Shared evaluation datasets and regression benchmarks
├── docs/
│   └── STARTER_ISSUES.md         # Curated Round 2 starter issues for ML & GenAI fellows
├── .github/
│   ├── pull_request_template.md  # Mandatory PR checklist
│   └── ISSUE_TEMPLATE/
│       ├── ml-task.md
│       └── genai-task.md
└── CONTRIBUTING.md               # Workflow, branching rules, and Code Review Rubric
```

## Quick Start for Fellows

1. Read [`CONTRIBUTING.md`](CONTRIBUTING.md) and review the **Code Review Rubric**.
2. Pick an unassigned issue from the **Issues** tab (or from [`docs/STARTER_ISSUES.md`](docs/STARTER_ISSUES.md)) and comment to claim it.
3. Fork the repository, create a scoped branch (`feat/<track>-<issue-id>-<short-slug>`), and implement your solution with reproducible steps and tests.
4. Open a Pull Request using the template and address all instructor review comments before merge.

## Safety & Data Policy

- **No Secrets or PII:** Never commit `.env` files, API keys, or private student/user data.
- **Non-Medical-Advice Guardrail:** Any GenAI project built on pharmaceutical pricing data is strictly for **informational price and active-ingredient lookup**. Models must explicitly refuse medical diagnosis, prescription, or dosage advice.

## Links

- Official Website: [phronesis-tech.com](https://phronesis-tech.com/)
- LinkedIn: [Phronesis](https://www.linkedin.com/company/phronesis-learning)
- AI Usage Policy: [phronesis-tech.com/ai-policy](https://phronesis-tech.com/ai-policy)
