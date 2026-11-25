# Shared Evaluations & Benchmarks (`evals/`)

This directory holds shared evaluation datasets, golden Q&A pairs, guardrail test cases, and regression benchmarks used across Machine Learning and Generative AI Pull Requests.

## Guidelines
- Keep evaluation files lightweight, reproducible, and free of any PII or secrets.
- Name test files `test_*.py` or `*_test.py` so CI automatically discovers and runs them with `pytest`.
