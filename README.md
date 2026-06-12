# California Housing — Exploratory Data Analysis (EDA)

End-to-end EDA and linear-regression project on the California Housing
dataset: predicting median house value from district-level features.

> 🚧 Work in progress — built step by step.

## 📋 Project Description
This project explores the California Housing dataset (17,000 districts, 9 numeric
features) to extract insights about housing prices and build a baseline
linear-regression model predicting `median_house_value`.

## 🛠️ Tech Stack
Python · Pandas · NumPy · Matplotlib · Seaborn · scikit-learn · ydata-profiling

## 📁 Project Structure

```
california-housing-eda/
├── data/            # raw dataset (read-only)
├── notebooks/       # Jupyter analysis
├── outputs/         # cleaned data & generated reports
├── src/             # script version of the analysis
├── requirements.txt
└── README.md
```

## ⚙️ Installation
```bash
conda create --name california python=3.11
conda activate california
pip install -r requirements.txt
```

## 🔍 Analysis Workflow
- [x] **Step 0** — Setup & first look at the data
- [x] **Step 1a** — Data integrity checks (missing values, duplicates, dtypes)
- [x] Step 1b — Outlier detection (IQR method)
- [ ] Step 2 — Descriptive statistics & correlation
- [ ] Step 3 — Visualizations
- [ ] Step 4 — Linear regression model
- [ ] Step 5 — Export & HTML report

## 🧹 Cleaning Decisions

### Missing values & duplicates
The dataset contains **no missing values and no duplicates** — a sanity check
that's still part of the pipeline so the code remains robust on future data.

### Outliers (IQR method)
Outliers were detected on every numeric column using Tukey's 1.5 × IQR rule.
Roughly **5–6%** of districts qualify as outliers on `total_rooms`,
`total_bedrooms`, `population` and `households`. About **5%** of
`median_house_value` outliers correspond to the dataset's capping at $500,001.

**Decision: outliers were kept.** These extreme districts represent real
high-density urban areas (e.g. Los Angeles, San Francisco). Dropping them
would (1) discard up to ~20% of the data, (2) bias the model toward
average-sized districts, and (3) ignore the most economically important
markets. The impact will be re-evaluated visually via the residuals plot
in Step 4.
