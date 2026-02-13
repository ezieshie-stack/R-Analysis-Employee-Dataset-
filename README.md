# 📈 Employee Compensation Analysis — Statistical Modeling in R

[![Project Status: Complete](https://img.shields.io/badge/Project%20Status-Complete-green.svg)](https://github.com/ezieshie-stack/R-Analysis-Employee-Dataset-)
[![Language: R](https://img.shields.io/badge/Language-R-276DC3.svg?logo=r&logoColor=white)](https://www.r-project.org/)

## 📌 Problem Statement

Understanding **what drives employee compensation** is critical for HR teams making equitable pay decisions. This project analyzes an employee salary dataset to identify the key factors influencing monthly salary — specifically, how experience, department, and age interact to determine pay levels.

## 🎯 Objectives

1. Explore and clean the employee salary dataset
2. Identify relationships between experience, department, age, and compensation
3. Quantify the correlation between experience and salary using Pearson's method
4. Build a reproducible analysis pipeline in R with a train/test framework

## 📊 What Was Done

### Phase 1: Data Wrangling & Cleaning
- Loaded and inspected the dataset structure (columns, types, dimensions)
- Checked for and removed missing values and duplicate records
- Created derived variables: **Annual Salary** (Monthly × 12), **Experience Level** categories (Junior / Mid-Level / Senior)
- Renamed columns for clarity and sorted by salary

### Phase 2: Exploratory Analysis
- **Departmental Analysis**: Calculated average salary by department to identify pay disparities
- **Experience Filtering**: Isolated IT employees with 10+ years of experience for targeted analysis
- **Data Reshaping**: Separated dependent (salary) and independent (experience, age) variables and demonstrated join operations

### Phase 3: Statistical Analysis & Modeling
- Computed **mean, median, mode, and range** of salary distribution
- Calculated **Pearson correlation** between experience and salary
- Created a **70/30 train/test split** using a seeded random number generator for reproducibility

### Phase 4: Visualization
- **Scatter Plot**: Experience vs. Salary — visualizing the positive correlation
- **Bar Chart**: Average Salary by Department — identifying which departments pay more

## 🔑 Key Findings & Results

| Metric | Result |
|--------|--------|
| **Experience ↔ Salary Correlation** | Positive (Pearson's r) — more experience = higher pay |
| **Highest-Paying Departments** | Identified via grouped bar chart |
| **Data Quality** | Clean dataset — no missing values or duplicates found |
| **Train/Test Split** | 70% training, 30% testing (seed = 123 for reproducibility) |

### Insights:
- **Experience is the strongest predictor** of monthly salary
- **Departmental pay gaps exist** — some departments consistently pay above average
- The **Junior → Mid-Level transition** (around 5 years) shows the steepest salary increase

## 🏗️ Project Structure

```
R-Analysis-Employee-Dataset/
│
├── assignment_2.Rmd                        # Full R Markdown analysis (reproducible)
├── Employee Dataset R analysis report.pdf  # Rendered PDF report with all outputs
├── employee_salary_dataset.csv             # Source data
└── README.md
```

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| **R** | Statistical computing and analysis |
| **dplyr** | Data wrangling, filtering, and summarization |
| **ggplot2** | Data visualization (scatter plots, bar charts) |
| **tidyr** | Data reshaping and tidying |
| **R Markdown** | Reproducible report generation |

## 🚀 Getting Started

1. **Open in RStudio:**
   ```r
   # Open assignment_2.Rmd in RStudio
   # Click "Knit" to render the full report
   ```

2. **Or run from the command line:**
   ```bash
   Rscript -e "rmarkdown::render('assignment_2.Rmd')"
   ```

## 👤 Author

> *"Every dataset has a story. My job is to find it, prove it, and make it actionable."*

**David Ezieshi** — Business Analyst & Data Analytics  
[LinkedIn](https://www.linkedin.com/in/david-ezieshi/) | [GitHub](https://github.com/ezieshie-stack)
