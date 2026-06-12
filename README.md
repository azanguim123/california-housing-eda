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
california-housing-eda/
├── data/                # raw dataset (read-only)
├── notebooks/           # Jupyter analysis
├── outputs/             # cleaned data & generated reports
├── src/                 # script version of the analysis
├── requirements.txt
└── README.md

## ⚙️ Installation
```bash
conda create --name california python=3.11
conda activate california
pip install -r requirements.txt
```

## 🔍 Analysis Workflow
- [x] **Step 0** — Setup & first look at the data
- [x] **Step 1a** — Data integrity checks (missing values, duplicates, dtypes)
- [ ] Step 1b — Outlier detection (IQR method)
- [ ] Step 2 — Descriptive statistics & correlation
- [ ] Step 3 — Visualizations
- [ ] Step 4 — Linear regression model
- [ ] Step 5 — Export & HTML report