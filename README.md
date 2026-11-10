# Longitudinal Trend and Shift Analysis of GHG Emissions at the Detroit Refinery (2010–2019)

IT 50700 Measurement and Evaluation in Industry and Technology, Fall 2026.
Team: Yamjala Madhav, Shraddha Upadhyay, Robin Sajedul Alam.

The project tests whether the Marathon Detroit Refinery's annual greenhouse gas emissions, as reported to the U.S. EPA Greenhouse Gas Reporting Program, changed significantly between 2010 and 2019.

| Hypothesis | Question | Test |
|---|---|---|
| H1 | Is there a linear trend? | Linear regression (slope t-test, F, R²) |
| H2 | Did the mean differ between 2010–2014 and 2015–2019? | One-way ANOVA, or Kruskal–Wallis if assumptions fail |
| H3 | Is there a monotonic trend without normality assumptions? | Mann–Kendall |
| H4 | Do the data meet the normality and equal-variance assumptions? | Shapiro–Wilk, Levene |

Who does what is in [TaskSplit.md](TaskSplit.md).

## Folders

```
README.md                this file
TaskSplit.md             who does what and the order of work
code/
  main.ipynb             setup and EDA, plus TODO sections for each person's tests
  data/                  Detroit_Refinery_GHG_2010_2019.csv
  models/                saved model parameters (h1_linear_model.json)
  figures/               PNG figures for the paper and slides
  results/               CSV tables (descriptive statistics, test results)
docs/
  group/                 the group's term paper (IT507_Term_Paper_Draft.docx, final PDF)
  presentation/          the group's PowerPoint
  documentation/         course guidelines, templates, sample project, article split
  me/                    personal files, not tracked by git
```

## Data

Source: EPA GHGRP through the Envirofacts API (`PUB_FACTS_SECTOR_GHG_EMISSION` and `PUB_FACTS_SUBP_GHG_EMISSION`, facility ID 1006388). The data are listed on Data.gov as the Greenhouse Gas Data Publication Tool.

`total_direct_tCO2e` is the refinery's own on-site emissions: Subpart C (stationary combustion) plus Subpart Y (petroleum refining), in metric tons CO2e. The "Petroleum Product Suppliers" figure under the same facility ID is excluded, because it covers the emissions from burning the fuel the refinery sells.

To download the data again, set `REFRESH_FROM_EPA = True` in Section 0 of the notebook.

## How to run

Requires Python 3 with `numpy`, `pandas`, `scipy`, `matplotlib` and Jupyter:

```bash
pip install numpy pandas scipy matplotlib jupyter
```

Open `code/main.ipynb` and run **Kernel → Restart & Run All**. Figures are written to `code/figures/`, tables to `code/results/`, and the H1 model to `code/models/`.

## Status

| Part | Owner | Status |
|---|---|---|
| Introduction and Literature Review | Group | Drafted (status report) |
| Section A1–A8: exploratory data analysis | Shared | Done |
| Section A9–A10: H1, residual checks | Madhav | To do |
| Section B: H2, sensitivity check | Shraddha | To do |
| Section C–D: H3, summary table | Robin | To do |
| Methodology, Discussion and Conclusion | All | To do |
| Presentation | All | To do |
