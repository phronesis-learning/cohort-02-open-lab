# Egypt Pharma Pricing Open Dataset (EPPOD v1) — Schema & Data Policy

This repository uses a sanitized educational snapshot of Egyptian pharmaceutical pricing and shortage data (**Egypt Pharma Pricing Open Dataset (EPPOD v1)**).

## 1. Two-Tier Data Policy

| Tier | Path | Visibility | Purpose |
| :--- | :--- | :--- | :--- |
| **Public Sample** | `data/sample/eppod_sample_300.csv` | **Committed to GitHub** | 300-row stratified sample for quickstart, local development, and CI tests |
| **Full Educational Snapshot** | `data/raw/eppod_edu_v1.csv` | **Strictly Gitignored (Private)** | Distributed privately to enrolled Cohort 02 fellows only — **NEVER commit `data/raw/` to GitHub** |

> **Important:** Code in this repository is licensed under the [MIT License](../LICENSE), whereas the Egypt Pharma Pricing Open Dataset (EPPOD v1) is provided **strictly for educational and non-commercial use** within Phronesis cohorts.

## 2. Sanitized Schema (17 Columns)

| # | Column | Type | Description / Allowed Values |
| :--- | :--- | :--- | :--- |
| 1 | `drug_code` | string | Anonymized catalog identifier (e.g., `DRUG-00001`) |
| 2 | `commercial_name_en` | string | Commercial product name (English) |
| 3 | `commercial_name_ar` | string | Commercial product name (Arabic) |
| 4 | `active_ingredients` | string | Generic active substance(s) |
| 5 | `manufacturer` | string | Pharmaceutical manufacturer |
| 6 | `dosage_form` | string | Dosage form (Tablet, Syrup, Vial, Cream, etc.) |
| 7 | `units` | string / int | Package unit count / presentation |
| 8 | `category` | enum | `prescription` \| `cosmetic` \| `supplement` \| `infant_formula` |
| 9 | `imported` | enum | `local` \| `imported` |
| 10 | `therapeutic_class` | string | Therapeutic classification |
| 11 | `previous_price_egp` | float | Previous official price (EGP) |
| 12 | `current_price_egp` | float | Current official price (EGP) |
| 13 | `price_change_pct` | float | Percentage price change |
| 14 | `price_updated_date` | date | UTC date of recorded price update (`YYYY-MM-DD`) |
| 15 | `is_missing` | boolean | Whether the product is currently reported missing (`true` / `false`) |
| 16 | `shortage_status` | string | Shortage status indicator |
| 17 | `uses_ar` | string | Arabic informational usage summary |

## 3. Non-Medical-Advice Disclaimer

This dataset snapshot and all models/assistants built on top of it are curated strictly for **informational pricing, shortage analytics, and active-ingredient lookup only**. They must **never** be used for medical diagnosis, prescribing, dosage recommendations, or clinical decision-making.
