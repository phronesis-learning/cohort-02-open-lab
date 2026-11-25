# Contributing Guide & Code Review Rubric

Every contribution to `cohort-02-open-lab` follows standard production engineering workflow. Your merged Pull Requests become part of your public engineering portfolio and count toward your Phronesis Cohort 02 evaluation.

## 1. Git & Branching Workflow

1. **Claim an Issue First:** Never open an unlinked PR. Comment on an open issue (e.g., `"I'd like to claim this issue"`) and wait for instructor assignment.
2. **Branch Naming:**
   - `feat/ml-12-price-anomaly-detector`
   - `feat/genai-18-arabic-rag-guardrails`
   - `fix/ml-21-fastapi-validation`
   - `docs/genai-04-eval-dataset`
3. **Commit Messages (Conventional Commits):**
   - `feat(ml): add LightGBM price-change baseline with 5-fold CV`
   - `fix(genai): enforce non-medical-advice guardrail on dosage queries`
   - `test(ml): add FastAPI schema validation unit tests`
4. **Keep PRs Focused:** One issue = one Pull Request. Avoid mixing unrelated refactors or committing large binary model weights (`> 10 MB`).

## 2. AI Usage Policy

You are encouraged to use AI coding assistants for brainstorming, debugging, and refactoring — **provided you can explain and defend every line of code in your PR during review and live defense.** Unverified copy-pasted code that you cannot explain will be rejected. See [phronesis-tech.com/ai-policy](https://phronesis-tech.com/ai-policy).

## 3. Instructor Code Review Rubric (10-Point Scale)

Every PR is reviewed by your Track Lead across 5 criteria (0–2 points each, total **10 points**; minimum **7/10** required to merge):

| Criterion | 0 (Needs Revision) | 1 (Acceptable) | 2 (Production-Grade) |
| :--- | :--- | :--- | :--- |
| **1. Correctness & Reproducibility** | Fails to run or hardcoded local paths | Runs with minor manual steps | Runs cleanly from README with pinned dependencies & fixed random seeds |
| **2. Engineering Quality & Structure** | Monolithic notebook / messy script | Modular functions, basic readability | Clean modules, type hints/docstrings, clear separation of data, model, and API |
| **3. Evaluation & Metrics** | No metrics or data leakage present | Basic train/test metric reported | Proper validation split, baseline comparison, and honest error/failure analysis |
| **4. Safety, Edge Cases & Tests** | Crashes on bad input / missing guardrails | Handles happy path + basic validation | Unit tests included; invalid inputs and (for GenAI) medical/prompt-injection guardrails verified |
| **5. Documentation & Git Hygiene** | Empty PR description / giant commit | Basic summary and clean commits | Clear PR template completed, screenshots/metrics included, and review comments addressed cleanly |

## 4. Merge Requirements

- [ ] Linked to an approved Issue (`Closes #<issue-number>`)
- [ ] All checklist items in `.github/pull_request_template.md` completed
- [ ] Zero committed secrets, API keys, or raw unapproved data files
- [ ] At least **1 approving review** from a Phronesis Track Lead
