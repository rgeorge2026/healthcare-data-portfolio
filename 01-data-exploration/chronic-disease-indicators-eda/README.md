# Project 1 — Chronic Disease Indicators: Exploration & Cleaning

**Category:** Data Exploration · **Built:** Week 1, Days 2–7 (~6 hours)

## Question

How do rates of major chronic diseases (e.g. diabetes, heart disease, obesity) vary across U.S. states and over time, and what data quality issues have to be resolved before that question can even be answered?

## Dataset

[CDC U.S. Chronic Disease Indicators](https://data.cdc.gov/Chronic-Disease-Indicators/U-S-Chronic-Disease-Indicators/hksd-2xuw) — state-level indicators across dozens of chronic disease topics, multiple years, with demographic stratification. Large, real-world-messy (mixed types, many nulls, long format). Download the CSV directly from the link above (not committed to this repo — see `.gitignore`).

Optional cross-reference dataset: state population figures from [data.gov](https://data.gov) or the Census Bureau, used to compute per-capita rates.

## Approach

1. **Profile** the raw file — shape, dtypes, memory footprint, null patterns.
2. **Clean** — resolve inconsistent state codes/names, coerce numeric columns stored as text, decide how to handle indicators with sparse data, and document every decision.
3. **Narrow scope** — filter to a handful of indicators, states, and years to keep the analysis focused and tractable.
4. **Reshape & merge** — pivot from long to wide format where useful; merge in population data to compute per-capita rates; validate the merge (row counts, key coverage).
5. **Visualize** — trend lines for 2–3 indicators across states/regions and over time.
6. **Cross-check in SQL** — load the cleaned data into SQLite and reproduce key pandas aggregations with `GROUP BY`/`HAVING` queries, as a consistency check between the two approaches.

## Tools

Python (pandas, matplotlib/seaborn), SQLite, SQL.

## What "done" looks like

- `src/` — cleaning and profiling scripts (or a well-organized notebook)
- `notebooks/` — exploratory analysis with visualizations
- `sql/` (or inline) — equivalent SQL queries validating the pandas findings
- A findings write-up below covering: what was messy about the raw data, the cleaning decisions made and why, and what the trends show

## Findings

_(Fill in after completing the project: 3–5 sentences on what the data shows, plus any caveats — e.g. reporting gaps by state/year.)_
