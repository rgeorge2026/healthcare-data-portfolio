# Project 2 — Medicare Chronic Conditions: SQL-Driven Cohort Analysis

**Category:** Data Analysis · **Built:** Week 2, Days 8–13 (~6 hours)

## Question

How does chronic condition prevalence and associated spending differ across Medicare beneficiary cohorts (age band, sex, dual-eligibility status), and how have these measures trended over the available years?

## Dataset

[CMS Chronic Conditions Public Use File](https://www.cms.gov/data-research/statistics-trends-and-reports/basic-stand-alone-medicare-claims-public-use-files/chronic-conditions-puf) — state/county-level Medicare chronic condition prevalence and spending, broken out by demographic subgroup. Download from the CMS link above (not committed — see `.gitignore`).

## Approach

1. **Load** the flat file(s) into a local SQLite (or Postgres) database.
2. **Foundational SQL** — filtering and `GROUP BY` aggregations comparing prevalence/spending across cohorts.
3. **Window functions** — rank states/counties by an indicator; compute year-over-year change with `LAG`/`LEAD`; running averages.
4. **Cohort & trend analysis** — define cohorts (e.g. age band) and track them across the available years; cross-check a subset of results against a quick pandas aggregation.
5. **Descriptive stats** — mean/median/IQR per cohort in Python; flag outlier states/counties.

## Tools

SQL (SQLite/Postgres — window functions, CTEs), Python (pandas for cross-checks and charts).

## What "done" looks like

- `sql/` — the queries, roughly in the order written (foundational → window functions → cohort analysis), each with a one-line comment on what it answers
- `notebooks/` — cross-checks and 2–3 visualizations of the cohort/trend results
- A findings write-up below

## Findings

_(Fill in after completing the project: which cohorts show the highest prevalence/spending, and how trends differ across them.)_
