# Dataset Information & Usage Policy

Place the **DrugShift × Phronesis Educational Snapshot (`drugshift_edu_v1.csv`)** in this directory (or keep a small 200-row sample in `data/sample/` if the full snapshot is shared privately with Cohort 02 fellows).

## Recommended Educational Schema

| Column | Type | Description |
| :--- | :--- | :--- |
| `drug_id` | string | Anonymized catalog identifier |
| `trade_name_en` | string | Commercial product name (English) |
| `trade_name_ar` | string | Commercial product name (Arabic, if available) |
| `active_ingredient` | string | Generic active substance(s) |
| `dosage_form` | string | Tablet, Syrup, Vial, Cream, etc. |
| `manufacturer_type` | string | Local vs. Imported |
| `old_price_egp` | float | Previous official price (EGP) |
| `new_price_egp` | float | Updated official price (EGP) |
| `price_updated_at` | date | Date of recorded price update |

## Disclaimer

This snapshot is curated strictly for **educational engineering, data science, and information retrieval research** within Phronesis cohorts. It must not be used for clinical decision-making, medical diagnosis, or prescribing.
