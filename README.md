# 🚗 BMW Global Sales — Exploratory Data Analysis (2010–2024)

Exploratory data analysis, visualization, and reporting on a BMW global sales dataset spanning 2010–2024, covering 50,000 sales records across 11 models and 6 global regions.

![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![Pandas](https://img.shields.io/badge/pandas-data%20analysis-150458.svg)
![Matplotlib](https://img.shields.io/badge/matplotlib-visualization-11557c.svg)
![Seaborn](https://img.shields.io/badge/seaborn-charts-4c72b0.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

---

## 📋 Overview

This project explores a BMW sales dataset to uncover trends in sales volume, regional performance, model popularity, pricing, and a High/Low sales classification label. The full workflow — data cleaning, descriptive statistics, visualization, and correlation analysis — is implemented in a single, ready-to-run Jupyter/Google Colab notebook, with a companion Word report summarizing the findings.

**Dataset:** `BMW_sales_data__2010-2024_.csv`
**Records:** 50,000
**Time span:** 2010 – 2024
**Fields:** `Model`, `Year`, `Region`, `Color`, `Fuel_Type`, `Transmission`, `Engine_Size_L`, `Mileage_KM`, `Price_USD`, `Sales_Volume`, `Sales_Classification`

---

## 🎯 Objectives

- Assess data quality — completeness, consistency, structure
- Quantify overall sales trends across 2010–2024
- Compare performance across regions, models, fuel types, transmissions, and colors
- Examine relationships between price, mileage, engine size, and sales volume
- Characterize the High vs. Low sales classification
- Summarize findings with clear, reproducible visualizations

---

## 🗂️ Repository Structure

```
├── BMW_sales_data__2010-2024_.csv     # Raw dataset
├── BMW_Sales_EDA.ipynb                # Full EDA notebook (Colab-ready, pre-executed)
├── BMW_Sales_EDA_Report.docx          # Written project report with embedded charts
├── assets/                            # Exported chart images used in this README
└── README.md
```

---

## 🛠️ Tools & Libraries

- **Python 3.10+**
- `pandas` — data loading, cleaning, aggregation
- `numpy` — numerical operations
- `matplotlib` / `seaborn` — static visualizations
- **Google Colab** / Jupyter — notebook environment

---

## 🚀 Getting Started

### Run in Google Colab (recommended)

1. Open [Google Colab](https://colab.research.google.com/) and upload `BMW_Sales_EDA.ipynb`.
2. Upload `BMW_sales_data__2010-2024_.csv` to the Colab session (or mount Google Drive).
3. Run all cells: **Runtime → Run all**.

### Run locally

```bash
git clone <your-repo-url>
cd <your-repo-folder>
pip install pandas numpy matplotlib seaborn jupyter
jupyter notebook BMW_Sales_EDA.ipynb
```

---

## 📊 Analysis Highlights

### 1. Sales Trend Over Time
Total annual sales volume fluctuates between ~16.3M and ~17.9M units per year, with no sustained upward or downward trend.

![Yearly sales trend](assets/01_yearly_trend.png)

### 2. Regional Performance
Sales volume is nearly evenly distributed across all six regions (within ~3.5% of each other).

![Sales by region](assets/02_region_sales.png)

### 3. Model-Level Performance
All 11 models post similar total sales volumes and near-identical average prices (~$74k–$76k).

![Sales by model](assets/03_model_sales.png)

### 4. Correlation Analysis
Engine size, mileage, price, and sales volume show essentially no correlation with one another (all |r| < 0.005).

![Correlation heatmap](assets/04_correlation_heatmap.png)

### 5. High vs. Low Sales Classification
~30% of records are labeled "High" and ~70% "Low"; this split is broadly consistent across models.

![Classification by model](assets/05_classification_by_model.png)

*See the [notebook](BMW_Sales_EDA.ipynb) for the full set of 13 visualizations, including fuel type/transmission breakdowns, price/mileage/engine distributions, color preferences, and region×model heatmaps.*

---

## 🔍 Key Findings

| Metric | Value |
|---|---|
| Total sales volume (all years) | 253,375,653 units |
| Best-performing region | Asia (42.97M units) |
| Best-performing model | 7 Series (23.79M units) |
| Average price (all models) | ~$75,000 |
| Max correlation with Sales_Volume | \|r\| = 0.004 (Mileage_KM) |
| High-classification share | 30.5% of records |

> **Note on data authenticity:** Totals and averages are nearly identical across every categorical breakdown (region, model, fuel type, transmission, color), and no numeric field correlates meaningfully with sales volume. This uniformity is more consistent with a synthetically/randomly generated dataset than real-world sales records. The EDA workflow and findings remain valid as a demonstration of technique, but business conclusions should be treated as illustrative rather than reflective of actual BMW market performance.

---

## 📄 Full Report

A detailed write-up with methodology, all charts, and discussion is available in [`BMW_Sales_EDA_Report.docx`](BMW_Sales_EDA_Report.docx).

---

## 🔮 Future Work

- Run formal statistical tests (ANOVA across regions/models, chi-square on classification vs. categorical fields) to confirm the absence of significant relationships
- Source a verified real-world BMW sales dataset for genuine market insight
- Extend with time-series decomposition and a predictive model for the sales classification label

---

## 👤 Author

**Mohd Shahan Ansari**
📧 [Shahanansarimoto@gmail.com](mailto:Shahanansarimoto@gmail.com)
🔗 [LinkedIn](https://www.linkedin.com/in/mohd-shahan-ansari-100479259/) · [GitHub](https://github.com/shahanansari-creator)

---

## 📜 License

This project is available under the [MIT License](LICENSE).
