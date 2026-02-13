# 📈 Employee Compensation Analysis — Uncovering Pay Equity Drivers in R

[![Project Status: Complete](https://img.shields.io/badge/Project%20Status-Complete-green.svg)](https://github.com/ezieshie-stack/R-Analysis-Employee-Dataset-)
[![Language: R](https://img.shields.io/badge/Language-R-276DC3.svg?logo=r&logoColor=white)](https://www.r-project.org/)
[![Tools: dplyr + ggplot2](https://img.shields.io/badge/Tools-dplyr%20%2B%20ggplot2-blue.svg)](https://www.tidyverse.org/)

---

## 📌 Problem Statement

Understanding **what determines employee compensation** is one of the most critical questions for any HR department. Is salary primarily driven by years of experience? Does the department you work in matter? Are there hidden pay gaps across age groups?

Without data-driven answers, organizations risk:
- **Pay inequity** — Employees doing similar work at different compensation levels, leading to attrition and legal exposure
- **Misallocated hiring budgets** — Offering too much to juniors or too little to seniors relative to market benchmarks
- **Blind spots in departmental spending** — Some departments may be overpaying or underpaying relative to the value they deliver

This project uses **statistical analysis in R** to isolate and quantify the specific factors that drive employee salary, providing the kind of evidence HR leaders need to make equitable, defensible compensation decisions.

---

## 🎯 Objectives

1. **Profile the workforce** — Understand the distribution of experience, age, department, and salary across the employee population
2. **Identify compensation drivers** — Determine which factors (experience vs. department vs. age) have the strongest influence on pay
3. **Test for statistical relationships** — Use Pearson correlation to quantify the strength and direction of salary predictors
4. **Build a modeling framework** — Create a reproducible train/test split for potential predictive salary modeling
5. **Deliver visual insights** — Generate clear, presentation-ready charts that communicate findings to non-technical stakeholders

---

## 📊 Methodology & Approach

### Phase 1: Data Wrangling & Quality Assurance

The raw `employee_salary_dataset.csv` was loaded and systematically cleaned:
- **Structure inspection** — Reviewed column types, dimensions, and variable names using `str()` and `names()`
- **Missing value check** — Scanned for NAs across all columns; dataset was clean (0 missing values)
- **Duplicate detection** — Checked for and removed any duplicated records to ensure unique employee entries
- **Column renaming** — Standardized column names for clarity (`Monthly_Salary` → `Salary`, `Experience_Years` → `Experience`)
- **Derived variables** — Created `Annual_Salary` (Monthly × 12) for annualized comparisons

### Phase 2: Feature Engineering

Custom business logic was applied to categorize the workforce:
- **Experience Level Classification** — A user-defined function was written to segment employees into:
  - **Junior**: < 5 years experience
  - **Mid-Level**: 5–10 years experience
  - **Senior**: > 10 years experience
- This segmentation enables group-level comparisons that are more meaningful than raw years

### Phase 3: Targeted Data Exploration

Specific business questions were investigated:
- **IT Senior Filter** — Isolated IT department employees with 10+ years of experience to benchmark senior technical compensation
- **Dependent/Independent Variable Identification** — Formally identified `Salary` as the dependent variable and `Experience`, `Age` as independent variables
- **Join Operations** — Demonstrated table separation and `left_join` reunification to validate data integrity

### Phase 4: Statistical Analysis

Rigorous statistical methods were applied:

| Analysis | Method | Purpose |
|----------|--------|---------|
| **Central Tendency** | Mean, Median, Mode | Understanding the "typical" employee salary |
| **Spread** | Range (Min–Max) | How wide is the pay distribution? |
| **Correlation** | Pearson's r (Experience ↔ Salary) | Quantifying the strength of the experience-pay relationship |
| **Model Readiness** | 70/30 train/test split (seed=123) | Preparing data for predictive modeling |

### Phase 5: Visualization

Two key charts were produced to communicate findings visually:
- **Scatter Plot** (Experience vs. Salary) — Visualizes the positive correlation; shows how salary increases with tenure, with some variance
- **Bar Chart** (Average Salary by Department) — Reveals departmental pay differences at a glance, highlighting which departments pay above or below average

---

## 🔑 Key Findings & Results

| Finding | Detail |
|---------|--------|
| **Experience is the #1 salary predictor** | Pearson correlation confirms a positive relationship — more experience consistently means higher pay |
| **The Junior → Mid-Level jump is the steepest** | The biggest salary increase occurs when crossing the 5-year mark, suggesting this is where employees gain the most leverage |
| **Departmental pay gaps are real** | Average salary varies significantly by department — not all roles are compensated equally |
| **Data quality is high** | Zero missing values, zero duplicates — the dataset is production-ready for modeling |
| **70/30 split is prepared** | A reproducible train/test framework is in place for future predictive salary modeling |

---

## 💡 Recommendations

### For HR Teams:
1. **Benchmark mid-level salaries** — The Junior → Mid-Level transition is where pay expectations shift most dramatically. Ensure your offers at the 5-year mark are competitive or risk losing talent during their highest-growth period.
2. **Audit departmental pay equity** — The bar chart reveals clear gaps. Cross-reference department averages with role complexity to ensure pay reflects actual contribution, not just departmental norms.
3. **Use experience bands, not raw years** — The Junior/Mid-Level/Senior categorization is more actionable for policy design than trying to price each individual year of experience.

---

## 🏗️ Project Structure

```
R-Analysis-Employee-Dataset/
│
├── assignment_2.Rmd                        # Full R Markdown analysis (reproducible)
├── Employee Dataset R analysis report.pdf  # Rendered PDF report with all outputs
├── employee_salary_dataset.csv             # Source dataset
└── README.md
```

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| **R** | Statistical computing and analysis |
| **dplyr** | Data wrangling — filtering, grouping, summarizing, joining |
| **ggplot2** | Publication-quality visualizations (scatter plots, bar charts) |
| **tidyr** | Data reshaping and tidying |
| **R Markdown** | Reproducible report generation (code + narrative + output in one document) |

---

## ⚙️ Getting Started

```r
# Option 1: Open in RStudio
# Open assignment_2.Rmd → Click "Knit" to render the full report

# Option 2: Command line
Rscript -e "rmarkdown::render('assignment_2.Rmd')"
```

---

## 👤 Author

> *"Every dataset has a story. My job is to find it, prove it, and make it actionable."*

**David Ezieshi** — Business Analyst & Data Analytics  
[LinkedIn](https://www.linkedin.com/in/david-ezieshi/) | [GitHub](https://github.com/ezieshie-stack)
