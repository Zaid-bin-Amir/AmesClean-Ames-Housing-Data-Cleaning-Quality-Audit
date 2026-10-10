# AmesClean

**Data Cleaning & Data Quality Audit for the Ames Housing dataset**
NeuroFive Internship, Week 1, Machine Learning (Regression Track)

## Contents

| File | Purpose |
|---|---|
| `AmesClean_Data_Quality_Audit_executed.ipynb` | Notebook with all outputs and charts already shown |
| `AmesClean_Data_Quality_Audit.ipynb` | Clean notebook to re-run in Google Colab |
| `DATA_QUALITY_REPORT.md` | Every data-quality decision with its justification, plus figures |
| `ames_cleaned.csv` | Cleaned dataset (1,460 rows) |
| `missing_value_report.csv` | Count and percent of missing values for every column |
| `figures/` | The five charts used in the notebook and the report |

## How to re-run

1. Download `train.csv` from https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/data
2. Open `AmesClean_Data_Quality_Audit.ipynb` in Google Colab
3. Runtime > Run all, then upload `train.csv` when asked

## Method in one paragraph

Missing values are treated by meaning (absent feature -> category `None`, genuine gaps -> median or mode plus indicator column), exact duplicates are removed, near-duplicates are reviewed, outliers are detected with the IQR and z-score rules and flagged instead of deleted, and types are corrected (codes to categories, quality ratings to ordered categories). `SalePrice` is never used in a cleaning decision. Scaling, encoding and splitting are left for Week 2.
