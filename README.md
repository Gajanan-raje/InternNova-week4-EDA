<p align="center">
  <img src="assets/banner.png" alt="Statistics, Visualization and EDA - InternNova Week 4" width="100%">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas&logoColor=white" alt="Pandas">
  <img src="https://img.shields.io/badge/Matplotlib-Visualization-11557c" alt="Matplotlib">
  <img src="https://img.shields.io/badge/Seaborn-Statistical%20Plots-4c72b0" alt="Seaborn">
  <img src="https://img.shields.io/badge/Google%20Colab-Notebook-F9AB00?logo=googlecolab&logoColor=white" alt="Colab">
  <img src="https://img.shields.io/badge/Status-Completed-brightgreen" alt="Status">
</p>

# Statistics, Data Visualization & Exploratory Data Analysis

**InternNova Data Analytics Internship, Week 4 Assignment (100 marks)**

| | |
|---|---|
| **Author** | Gajanan Harinarayan Raje |
| **College** | MGM's College of Computer Science & IT, Nanded (TYBCA, SRTMU University) |
| **Internship** | InternNova, Data Analytics Intern |
| **Tools** | Python, NumPy, Pandas, Matplotlib, Seaborn, Google Colab |

---

## Table of Contents
1. [Project Overview](#project-overview)
2. [Dataset](#dataset)
3. [Tasks Covered](#tasks-covered)
4. [Key Results](#key-results)
5. [Key Insights](#key-insights)
6. [Business Recommendations](#business-recommendations)
7. [Chart Gallery](#chart-gallery)
8. [Repository Structure](#repository-structure)
9. [How to Run](#how-to-run)
10. [Skills Demonstrated](#skills-demonstrated)

---

## Project Overview

This project applies core statistics, data visualization and exploratory data analysis (EDA) to a retail sales dataset. It covers the full workflow: calculate statistics, detect outliers, build charts with Matplotlib and Seaborn, inspect and clean messy data, find correlations, and turn the findings into data-driven business recommendations.

## Dataset

A **synthetic retail sales dataset** generated with Python (`numpy.random.default_rng(42)`), so results are reproducible. It has 300 orders, plus 8 duplicate rows added on purpose (308 rows, 9 columns before cleaning).

| Column | Description |
|---|---|
| `OrderID` | Order number |
| `Month` | Jan to Jun |
| `Category` | Electronics, Clothing, Grocery, Furniture |
| `Region` | North, South, East, West |
| `Quantity` | Number of items ordered |
| `UnitPrice` | Price per item |
| `AdSpend` | Advertising spend for the order |
| `Sales` | Order revenue |
| `Rating` | Customer rating (1 to 5) |

**Dirty data added deliberately to demonstrate cleaning:** missing values (UnitPrice, Rating), duplicate rows, extreme Sales outliers, inconsistent Category text (`electronics `, `CLOTHING`, `grocery`) and negative Quantity values.

## Tasks Covered

| # | Task | Marks | What was done |
|---|---|---|---|
| 1 | Mean, Median & Mode | 10 | Calculated and explained all three measures |
| 2 | Variance & Standard Deviation | 10 | Calculated and explained the spread of Sales |
| 3 | Correlation & Probability | 10 | AdSpend vs Sales correlation; two probability examples |
| 4 | Outlier Detection | 10 | IQR method, outlier table and box plot |
| 5 | Matplotlib Visualization | 15 | Line, bar, pie, histogram, scatter |
| 6 | Seaborn Visualization | 15 | Count plot, box plot, heatmap, pair plot |
| 7 | EDA: Inspection & Cleaning | 15 | Shape, dtypes, summary, missing values, duplicates, fixes, before/after screenshots |
| 8 | EDA: Correlation & Insights | 10 | Correlation analysis, patterns, 5 insights |
| 9 | Business Recommendations | 5 | 4 recommendations backed by data |

## Key Results

| Metric | Value |
|---|---|
| Mean Sales | 471.16 |
| Median Sales | 433.04 |
| Standard deviation | 302.82 |
| Correlation (AdSpend vs Sales), raw data | 0.22 (weak) |
| P(order is Electronics) | 0.315 |
| P(Rating of 4 or more) | 0.411 |
| Outliers found (IQR method) | 4 |
| Rows before cleaning | 308 |
| Rows used for analysis after cleaning | 296 |

The mean is higher than the median, so Sales is right-skewed because of a few very large orders.

## Key Insights

1. **Quantity** has the strongest relationship with Sales (r = 0.74), followed by **UnitPrice** (r = 0.49).
2. **AdSpend** has a positive correlation with Sales (r = 0.29).
3. **Electronics** earns the highest total sales (42,478); **Furniture** has the fewest orders (46).
4. **Rating** has almost no correlation with Sales (r = -0.02), so ratings do not predict order value.
5. Sales peak in **May** (29,783) and are lowest in **June** (14,725).

## Business Recommendations

1. **Increase and target advertising spend.** Orders with high ad spend average 479 in sales versus 409 for low ad spend (17% higher).
2. **Push bundles and volume discounts.** Orders with 5 or more items average 560 versus 302 for 1 to 4 items (85% higher).
3. **Plan stock and promotions around the top category and the monthly pattern.** Stock more Electronics before May and run offers in June.
4. **Add data validation at order entry.** The raw data had duplicates, negative quantities, inconsistent names, missing values and extreme values that distort revenue reports.

## Chart Gallery

| Matplotlib | Seaborn | EDA |
|---|---|---|
| ![Line](charts/m_line.png) | ![Count](charts/s_count.png) | ![Correlation](charts/e_corr_sales.png) |
| ![Bar](charts/m_bar.png) | ![Box](charts/s_box.png) | ![Patterns](charts/e_patterns.png) |
| ![Pie](charts/m_pie.png) | ![Heatmap](charts/s_heat.png) | ![Recommendations](charts/r_recommendations.png) |
| ![Histogram](charts/m_hist.png) | ![Pair](charts/s_pair.png) | ![Outliers](charts/outliers.png) |
| ![Scatter](charts/m_scatter.png) | | |

### Data cleaning: before and after

![Before](charts/before_cleaning.png)
![After](charts/after_cleaning.png)

## Repository Structure

```
InternNova-Week4-EDA/
├── README.md
├── assets/
│   └── banner.png
├── notebook/
│   └── Week4_Statistics_Visualization_EDA_Gajanan_Raje.ipynb
├── data/
│   ├── sales_raw.csv
│   └── sales_clean.csv
├── charts/
│   └── (all PNG charts)
└── report/
    └── Week4_Report_Gajanan_Raje.pdf
```

## How to Run

1. Open the notebook in [Google Colab](https://colab.research.google.com) (File, Upload notebook) or in Jupyter.
2. Run **Runtime, Run all**. The dataset is generated in code, so no download is needed.
3. Charts and CSV files are saved in an `outputs/` folder.

**Requirements:** `numpy`, `pandas`, `matplotlib`, `seaborn`

```bash
pip install numpy pandas matplotlib seaborn
```

## Skills Demonstrated

- Descriptive statistics, correlation and basic probability
- Outlier detection with the IQR method
- Data visualization with Matplotlib and Seaborn
- Data cleaning: missing values, duplicates, inconsistent and incorrect values
- Turning analysis into insights and business recommendations
- Documentation and reproducible work (fixed random seed)

---

<p align="center">Made by <b>Gajanan Harinarayan Raje</b> · TYBCA · InternNova Data Analytics Internship</p>
