# Project 5 — Heart Failure Survival Analysis & Biostatistics

**Category:** Biostatistics · **Built:** Week 4, Days 25–27 (~3 hours)

## Question

Beyond a binary yes/no prediction, how do survival times differ between patient subgroups, and are commonly cited risk factors statistically associated with mortality in this cohort?

## Dataset

Same as Project 4: [UCI Heart Failure Clinical Records](https://archive.ics.uci.edu/dataset/519/heart+failure+clinical+records) — reused here for its follow-up `time` and `DEATH_EVENT` columns, which make it well suited to survival analysis without needing a new dataset.

## Approach

1. **Hypothesis testing** — compare a clinical variable (e.g. ejection fraction, serum creatinine) between the survived and died groups using a t-test or Mann-Whitney U test (whichever the distribution warrants); report a 95% confidence interval, not just a p-value.
2. **Epidemiological measures** — for a binary risk factor (e.g. anaemia, diabetes, high blood pressure), compute the odds ratio and/or relative risk for the death event, with its 95% CI.
3. **Survival analysis** — fit Kaplan-Meier curves (overall, and stratified by a covariate such as ejection fraction category), run a log-rank test to compare strata, and optionally fit a simple Cox proportional hazards model.

## Tools

Python (scipy.stats for hypothesis tests, [lifelines](https://lifelines.readthedocs.io/) for Kaplan-Meier/Cox/log-rank).

## What "done" looks like

- `src/` — hypothesis test script, epi measures script, survival analysis script
- A Kaplan-Meier plot (overall + stratified)
- A findings write-up below stating each result in plain language, not just statistical output

## Findings

_(Fill in after completing the project: e.g. "Patients with below-median ejection fraction had significantly worse survival, p < 0.05 by log-rank test" — and what the odds ratio for each risk factor was, with CI.)_
