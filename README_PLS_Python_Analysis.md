# 📊 Public Library Survey FY2018 — Python Exploratory Data Analysis
### Analyzing Physical Infrastructure, Operational Capacity, and Community Reach of U.S. Public Libraries

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)
![EDA](https://img.shields.io/badge/Analysis-Exploratory%20Data%20Analysis-success.svg)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Wrangling-lightgrey.svg)
![Visualization](https://img.shields.io/badge/Visualization-Matplotlib%20%7C%20Seaborn-yellow.svg)

---

## 🎯 CSAR Framework Overview

| | |
|---|---|
| **Challenge** | The FY2018 Public Library Survey is a massive federal census — 17,478 outlets × 37 coded variables — that is unusable for insight in its raw form: missing values, invalid negatives, cryptic codes, and no derived metrics. |
| **Situation** | As the foundational analysis layer of a larger data-science initiative, this project had to transform raw IMLS survey data into a clean, feature-engineered, statistically characterized dataset — and extract national benchmarks on library infrastructure and access. |
| **Action** | Executed a structured 5-stage analytical workflow in Jupyter: data loading → initial exploration → cleaning & feature engineering (incl. engineered `HOURS_PER_WEEK` metric) → executive summary statistics → visualization of outlet-type composition with Matplotlib/Seaborn. |
| **Result** | Produced a fully cleaned, analysis-ready national dataset; established national benchmarks (**median 6,550 sq ft**, **2,174 hrs/year**, **51.4 weeks/year**); surfaced **6 statistically supported key findings**, including a significant size↔hours correlation and the fact that **94% of US library access flows through Branch + Central outlets**. |

---

## 🔴 The Challenge

Federal open data is powerful but hostile to direct analysis. The FY2018 Public Library Survey (PLS) from the **US Institute of Museum and Library Services (IMLS)** arrived as:

- **17,478 rows × 37 columns** of mixed-type survey data.
- **Coded categorical fields** (`OUTLET_TYPE`, `LOCALE_CAT`) unreadable without domain mapping.
- **Data-quality defects**: missing values, duplicate records, and physically impossible values (negative square footage / hours).
- **No normalized operational metric** — hours and weeks had to be combined into a comparable measure before any fair analysis of "operational capacity" could begin.

The challenge: convert this raw census into a clean, trustworthy analytical foundation — and answer *"What does America's public library infrastructure actually look like?"*

---

## 🟠 The Situation

This repository contains the **Python/Jupyter analysis layer** of the Public Library Survey project — the rigorous data-preparation and exploratory backbone on which downstream machine learning and dashboarding depend.

| Attribute | Detail |
|---|---|
| Dataset | `pls_fy18_outlet_pud18i.csv` (FY2018 Public Library Survey) |
| Source | US Institute of Museum and Library Services (IMLS) |
| Scale | 17,478 library outlets, 37 variables — a complete national census |
| Companion Artifact | Full analytical report: *"Analyzing Physical Infrastructure, Operational Capacity, and Community Reach of U.S. Public Libraries"* (PDF, included in repo) |

---

## 🟡 The Action

A disciplined, reproducible 5-stage workflow (Jupyter Notebook):

### 1️⃣ Setup & Data Loading
- Loaded the 17,478 × 37 CSV with `pandas` (handling `latin1` encoding and mixed dtypes).
- Documented dataset provenance, shape, and survey year.

### 2️⃣ Initial Data Exploration
- Profiled missing values, data types, and basic descriptive statistics.
- Assessed overall data quality to scope the cleaning effort.

### 3️⃣ Data Cleaning & Feature Engineering
- **Deduplicated** records and **filtered invalid rows** (negative sizes/hours).
- **Engineered `HOURS_PER_WEEK`** — a normalized operational-capacity metric enabling fair cross-library comparison.
- **Decoded survey codes** (`OUTLET_TYPE` → Central/Branch/Bookmobile; `LOCALE_CAT` → City/Suburban/Town/Rural) into human-readable categories.

### 4️⃣ Executive Summary Statistics
- Computed library **density per state**, outlet-type breakdowns, and national benchmarks:
  - Median library size: **6,550 sq ft**
  - Average operation: **2,174 hours/year** across **51.4 weeks/year**
- Quantified the relationship between county population and operating hours.

### 5️⃣ Visualization
- Built clear, publication-quality charts with **Matplotlib & Seaborn** to communicate outlet-type composition and geographic patterns to non-technical audiences.

---

## 🟢 The Results

### Quantified Outcomes
- ✅ Transformed **17,478 × 37 raw federal records** into a clean, fully decoded, analysis-ready dataset with a newly engineered operational metric.
- 📏 Established national infrastructure benchmarks: **6,550 sq ft median size**, **2,174 avg hours/year**, **51.4 avg weeks/year**.
- 🔍 Delivered **6 statistically supported key findings** on national library infrastructure.

### The 6 Key Findings
1. **Branch + Central libraries = 94% of all US library outlets** — the backbone of national access.
2. **Suburban areas hold the most library outlets overall.**
3. **City libraries are larger AND open more hours** than their rural counterparts.
4. **County population positively predicts library operating hours.**
5. **Facility size and operating hours are statistically significantly correlated.**
6. **82%+ of libraries operate all 52 weeks a year** — near-universal year-round access.

### Impact
This analysis serves as the **validated data foundation** for the companion machine-learning repository (Random Forest prediction, K-Means segmentation, Power BI dashboarding) — demonstrating the complete analyst skill set: wrangling messy real-world federal data, engineering meaningful features, and communicating findings with statistical rigor.

---

## 🛠️ Tech Stack

| Category | Tools |
|---|---|
| Language | Python |
| Data Wrangling | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Environment | Jupyter Notebook |
| Deliverable | Jupyter Notebook + Full PDF Analytical Report |

---

## 🚀 How to Run

```bash
git clone https://github.com/jschouhan007/Public-Library-Survey-FY-2018-US-Data-Science---Python-Analysis.git
cd Public-Library-Survey-FY-2018-US-Data-Science---Python-Analysis
pip install pandas numpy matplotlib seaborn jupyter
jupyter notebook "Jupyter Notebook Project Final DS.ipynb"
```
*(Place `pls_fy18_outlet_pud18i.csv` — available from [IMLS](https://www.imls.gov/research-evaluation/data-collection/public-libraries-survey) — in the working directory.)*

---

## 📝 ATS Keywords
`Exploratory Data Analysis` `EDA` `Data Cleaning` `Data Wrangling` `Feature Engineering` `Python` `Pandas` `NumPy` `Matplotlib` `Seaborn` `Jupyter Notebook` `Statistical Analysis` `Descriptive Statistics` `Data Quality` `Federal Open Data` `IMLS` `Data Visualization` `Analytical Reporting`

## 💼 CV-Ready Bullets
- Performed end-to-end exploratory data analysis on the FY2018 US Public Library Survey (**17,478 outlets × 37 variables**), cleaning and decoding raw federal census data and engineering a normalized `HOURS_PER_WEEK` operational-capacity metric.
- Established national library infrastructure benchmarks (**6,550 sq ft median size; 2,174 hours/year; 51.4 weeks/year**) and surfaced 6 statistically supported findings on geographic access and operational patterns.
- Authored a full analytical report and publication-quality visualizations (Matplotlib/Seaborn), creating the validated data foundation for downstream machine-learning modeling and Power BI dashboarding.
