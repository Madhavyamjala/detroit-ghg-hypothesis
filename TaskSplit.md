# IT 50700 Term Project: Task Split

Detroit Refinery GHG emissions, 2010–2019. Team: Yamjala Madhav, Shraddha Upadhyay, Robin Sajedul Alam.

Each person has one coding section, one Methodology subsection, their own part of the Discussion, and their own slides. Everyone presents.

Already done: Introduction and Literature Review (in `docs/group/IT507_Term_Paper_Draft.docx`), the data file (`code/data/Detroit_Refinery_GHG_2010_2019.csv`), the shared setup in `code/main.ipynb`, and the exploratory data analysis (Section A1–A8: data checks, descriptive statistics, year-over-year changes, Figure 1 and four EDA figures).

Folder layout and how to run the notebook are in `README.md`.

## Madhav: data, H1 linear trend, residual checks

**Code (`main.ipynb` Section A9–A10)**
- A9: H1 linear regression (slope t-test, F, R², ANOVA table), saved to `models/h1_linear_model.json`.
- A10: H4 part 1, Shapiro–Wilk on the H1 residuals, Durbin–Watson, and Figure 2 (residual plots).

**Paper**
- Methodology: Data (source, facility ID 1006388, why the supplier figure is excluded) and H1 with residual checks (about 1 page).
- Discussion: what H1 found, plus the limitations (only 10 values, whether the residuals are independent, the hydrogen plant reporting separately from 2012).
- Update the Introduction and Literature Review: move Table 2 to the Appendix and fix anything the results change.

**Slides:** title, problem and hypotheses, data, H1 results.

## Shraddha: H2 mean shift, sensitivity check

**Code (`main.ipynb` Section B)**
- B1: H4 part 2, Shapiro–Wilk on each period, Levene's test.
- B2: H2 one-way ANOVA, Kruskal–Wallis if assumptions fail, and Figure 3 (box plots).
- B3: sensitivity check, 2010–2012 against 2013–2019.

**Paper**
- Methodology: H2, the decision rule (ANOVA or Kruskal–Wallis), and the sensitivity check (about 0.75 page).
- Discussion: what H2 and the sensitivity check found.
- Conclusion, which ties all hypotheses together (about 0.5 page).
- Confirm the three corrected citations (Sanchez et al., An et al., Mu et al.) are the papers actually read.

**Slides:** H2 results, sensitivity check, conclusion.

## Robin: H3 monotonic trend, results table, final assembly

**Code (`main.ipynb` Sections C and D)**
- C1: H3 Mann–Kendall test, written by hand and checked against Kendall's tau.
- C2: Sen's slope and Figure 4 (regression line and Sen's slope line).
- D: summary table of all tests, saved to `results/summary_of_tests.csv`.
- Merge everyone's sections into `main.ipynb` and run Restart & Run All.

**Paper**
- Methodology: H3 and Sen's slope (about 0.5 page).
- Discussion: what H3 found and how it compares with H1.
- Appendix (Table 2, the data table) and final formatting: table of contents, figure and table numbers, IEEE references, page numbers, PDF export.

**Slides:** literature review highlights, H3 results, summary table of all tests. Also combine everyone's slides into one deck.

## Everyone
- Read the full paper once before submission. Each person checks the sections they didn't write.
- Rehearse the 10-minute talk together and attend both presentation days.
- Fill in and submit your own peer evaluation (`IT 507_Peer Evaluation_FA26.docx`).

## Order of work
1. **Code, in parallel:** each person copies `main.ipynb`, fills in only their own section, and sends that section to Robin.
2. **Merge:** Robin merges the sections, runs the notebook, and shares the figures and `summary_of_tests.csv`.
3. **Write, in parallel:** each person writes their Methodology and Discussion parts in `docs/group`.
4. **Assemble:** Robin builds the paper and the deck. Shraddha writes the Conclusion once all results are in.
5. **Review and rehearse:** everyone reviews and rehearses. Submit the PDF and PowerPoint (one per group) and peer evaluations (one each).

The main text must be 8–10 pages, excluding the cover, table of contents, references and appendix. Introduction and Literature Review take about 6 pages, leaving about 2–2.5 pages for Methodology and 1–1.5 for Discussion and Conclusion.
