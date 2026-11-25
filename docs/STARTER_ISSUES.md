# Curated Starter Issues — Cohort 02 (Winter 2026)

Copy these directly into your GitHub **Issues** tab to launch Weeks 4–6 of the Open-Source Lab.

---

## Machine Learning Track (`track:ml`)

### Issue #1: `[ML] Clean & Profile the DrugShift Egyptian Medicine Pricing Snapshot`
- **Difficulty:** Starter (Week 4)
- **Objective:** Build a reproducible EDA and data-cleaning script for the educational pharmaceutical pricing snapshot (handling missing active ingredients, Arabic/English naming inconsistencies, dosage extraction, and currency outliers).
- **Deliverable:** `tracks/machine-learning/data_prep/clean_drugshift.py` + summary data-quality report + pytest checks.

### Issue #2: `[ML] Price-Anomaly & Corrupted-Entry Detector`
- **Difficulty:** Intermediate (Week 5)
- **Objective:** Train an unsupervised/semi-supervised anomaly detection pipeline (Isolation Forest / robust z-score per active-ingredient group) that flags abnormal pricing errors (e.g., missing decimal points or pack-size mismatches).
- **Deliverable:** Model pipeline + precision/recall on synthetic injected errors + error analysis.

### Issue #3: `[ML] Price-Shift Risk Classifier (XGBoost / LightGBM)`
- **Difficulty:** Intermediate (Week 5)
- **Objective:** Predict which medicine categories have the highest likelihood of a price revision based on manufacturer type (local vs. imported), therapeutic class, dosage form, and historical shift frequency.
- **Deliverable:** Feature engineering pipeline, stratified CV metrics (ROC-AUC / PR-AUC), and SHAP feature importance summary.

### Issue #4: `[ML] Production FastAPI Service for Therapeutic Alternative Price Ranking`
- **Difficulty:** Capstone (Week 6)
- **Objective:** Expose a FastAPI service (`POST /alternatives`) that takes a medicine name or active ingredient and returns ranked lower-cost local equivalents with price delta and Pydantic schema validation.
- **Deliverable:** FastAPI app, Dockerfile, OpenAPI docs, and automated endpoint tests.

---

## Generative AI Track (`track:genai`)

### Issue #5: `[GenAI] Bilingual Arabic/English Drug Name Normalizer & Query Rewriter`
- **Difficulty:** Starter (Week 4)
- **Objective:** Build a query normalization layer that maps Egyptian colloquial or misspelled Arabic/English medicine queries (e.g., `بنادول اكسترا` / `Panadol Extra`) to canonical catalog entries.
- **Deliverable:** Normalization module + evaluation on 30 noisy Arabic/English test queries.

### Issue #6: `[GenAI] Hybrid RAG Pipeline over the DrugShift Pricing Catalog`
- **Difficulty:** Intermediate (Week 5)
- **Objective:** Implement hybrid retrieval (BM25 + dense embeddings) with metadata filtering (active ingredient, dosage form, price range) that returns grounded answers with exact source row citations.
- **Deliverable:** Indexing + retrieval pipeline + Recall@5 and Faithfulness metrics on 25 test queries.

### Issue #7: `[GenAI] Medical-Safety & Prompt-Injection Guardrails Layer`
- **Difficulty:** Intermediate (Week 5)
- **Objective:** Implement input/output guardrails ensuring the assistant **never** diagnoses symptoms, recommends dosages, or overrides physician advice — while still answering legitimate price and active-ingredient lookup questions cleanly.
- **Deliverable:** Guardrail middleware + adversarial test suite (20 safe queries + 20 unsafe/medical-advice queries) with >= 95% refusal precision.

### Issue #8: `[GenAI] MCP Tool Server for Live Pricing & Alternative Lookup`
- **Difficulty:** Capstone (Week 6)
- **Objective:** Wrap the verified catalog lookup and alternative ranker into a clean **Model Context Protocol (MCP)** server with structured tool schemas, latency logging, and an automated evaluation harness.
- **Deliverable:** MCP server + client demo + latency & tool-call accuracy benchmark report.
