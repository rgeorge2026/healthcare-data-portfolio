# Healthcare Data Portfolio

A portfolio of Python + SQL projects built on public and synthetic healthcare data, covering the full analytics stack: data exploration, data analysis, data modeling, data science, and biostatistics.

Built over a 4-week, 1-hour-a-day plan as a demonstration of intermediate-level data skills applied to real-world healthcare questions.

## Skills demonstrated

- **Python**: pandas, numpy, matplotlib/seaborn, scikit-learn, lifelines, scipy.stats
- **SQL**: SQLite/PostgreSQL — joins, aggregations, window functions, schema design (DDL)
- **Data engineering**: cleaning, merging, and validating messy real-world data; ETL into a normalized relational schema
- **Data science**: feature engineering, classification modeling, model evaluation
- **Biostatistics**: hypothesis testing, epidemiological measures (odds ratio / relative risk), survival analysis (Kaplan-Meier, log-rank test)

## Projects

| # | Category | Project | Dataset | Key techniques |
|---|----------|---------|---------|-----------------|
| 1 | Data Exploration | [Chronic Disease Indicators EDA](01-data-exploration/chronic-disease-indicators-eda/) | CDC U.S. Chronic Disease Indicators | Cleaning, reshaping, merging, missing-data handling |
| 2 | Data Analysis | [Medicare Chronic Conditions SQL Analysis](02-data-analysis/medicare-chronic-conditions-sql/) | CMS Medicare Chronic Conditions PUF | Window functions, cohort/trend analysis |
| 3 | Data Modeling | [Synthea EHR Relational Schema](03-data-modeling/synthea-ehr-schema/) | Synthea synthetic patient records | ER design, normalization, ETL, referential integrity |
| 4 | Data Science | [Heart Failure Mortality Prediction](04-data-science/heart-failure-mortality-prediction/) | UCI Heart Failure Clinical Records | Feature engineering, classification, model evaluation |
| 5 | Biostatistics | [Heart Failure Survival Analysis](05-biostatistics/heart-failure-survival-analysis/) | UCI Heart Failure Clinical Records | Hypothesis testing, odds/risk ratios, Kaplan-Meier |

Each project folder has its own README with the question it answers, the approach taken, key findings, and the tradeoffs/decisions made along the way.

## Setup

```bash
git clone https://github.com/<your-username>/healthcare-data-portfolio.git
cd healthcare-data-portfolio
python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements.txt
```

Each project's README notes where to download its raw data from (data files themselves are not committed — see `.gitignore`).

## About

Built by [Your Name] as a self-directed learning project to strengthen applied data analysis skills in the healthcare domain. See the [full 4-week build plan](#) for how this repo was developed day by day.
