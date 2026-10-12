# Figures and tables guideline: item reference

Source: Vickers AJ, Assel MJ, Sjoberg DD, et al. *Guidelines for Reporting of Figures and Tables for Clinical Research in Urology.* Published 2020 in four journals:
- Urology 142:1–13 (doi:10.1016/j.urology.2020.05.002)
- Eur Urol 78(1):97–109 (doi:10.1016/j.eururo.2020.04.048)
- J Urol 204(1):121–133 (doi:10.1097/JU.0000000000001096)
- BJU Int 126(1):14–25 (doi:10.1111/bju.15102)

Statistical reviewers at these journals use it as a reference and ask authors to follow it, or to justify not doing so. Like the statistics guideline, it allows any item to be broken when the result is a clearer table or a better figure.

Everything below paraphrases the paper. Cite items by their ID:
- `FG`: general remarks
- `FP3.x`: the six figure principles
- `FD1–FD30`: figure dos and don'ts
- `FT1–FT15`: table rules

Items that repeat a statistics item give its cross-reference (S-numbers, see `stats-guideline.md`).

**Applies to** is `ALL` unless a figure type is named: KM (Kaplan-Meier/survival), PRED (prediction/marker), RCT.

## Contents
1. General remarks (FG)
2. Figure principles (FP3.1–FP3.6)
3. Figure dos and don'ts (FD1–FD30)
4. Table rules (FT1–FT15)
5. Suggested tools

---

## 1. General remarks

### FG Tables and figures complement the text; they do not duplicate it
- Mention the key points in the text and also show them in a table or figure. Order tables and figures so the reader can move easily between them and the text.
- Tables hold detailed numbers. Figures give an immediate impression that words or numbers cannot.

## 2. Figure principles

### FP3.1 Include a figure only if it clearly helps the reader understand the findings
- Ask whether the paper would be weaker without it. A plain bar chart of stage counts adds nothing over a table.
- Kaplan-Meier plots are not automatically required, e.g. when events are rare and follow-up is long. Have a reason for each one.

### FP3.2 Design the graph around the message; don't just pick a software default
- Sketch possible designs independently of the software (e.g. on a whiteboard), then program the chosen one.
- Software presets are rarely good enough except for standard plots: calibration, decision curve, forest and survival plots.
- Showing individual patient data is often more informative than summary bars.

### FP3.3 Figures do not replace key numbers in the text
- Key estimates must also appear as numbers, in the text or a table, e.g. the between-group difference with its 95% CI (see S4.4, S4.5). "Results are shown in Figure 2" is not enough.

### FP3.4 A graph should give an immediate visual impression
- If reading the figure takes as long as reading one sentence of numbers (e.g. a box plot of age), the figure is not earning its place.

### FP3.5 Make the figure attractive
- Clean lines, little clutter, white space. Avoid censoring hash marks that hide curves, dense gridlines, odd plot markers and harsh colour schemes.

### FP3.6 Labels and legends must be clear and complete
- The legend should make sense without the main text, even if that makes it long.
- Avoid unexplained acronyms. Use real group names ("drug"/"placebo", not "A"/"B"). Define terms such as "clinically significant cancer". Give the time axis units.
- Labels placed directly beside the curves are often better than a separate legend box.

## 3. Figure dos and don'ts

- **FD1** Label every axis. All text must be easy to read, in an appropriate font size and not squashed by software defaults. Explain unavoidable abbreviations in the caption.
- **FD2** Include the leading zero ("0.5", not ".5").
- **FD3** Consider giving rates and probabilities as percentages (50%) rather than proportions (0.5).
- **FD4** Keep fonts, colours, labels and the placement of on-plot text consistent across all figures.
- **FD5** Consider adding the predictor's distribution (e.g. a shaded density) beneath line plots, so readers can see where the data actually are. · PRED
- **FD6** Put a number-at-risk table per arm under Kaplan-Meier plots, and consider showing CIs. If there is a risk table, leave out censoring marks. · KM (see S4.16)
- **FD7** Use numbers and text on a figure sparingly. They should explain the figure (axis and line labels), not add results such as p values or HRs. Put those in the legend, where you can also explain, for example, that they come from an adjusted model while the curve itself is unadjusted.
- **FD8** Say what error bars represent (95% CI, SD, reference range).
- **FD9** Use subfigures only for closely related graphs, not to reduce the figure count.
- **FD10** Do not present ROC curves. They rarely show more than the AUC does (the paper cites statistics item "5.7"). · PRED
- **FD11** Do not plot values that are impossible for the outcome. Predicted risks and their CIs must stay within (0, 1); if they do not, use a different estimation method. · PRED
- **FD12** No pie charts. They use a lot of ink for little data, are hard to read when categories are small, and a table does the job better.
- **FD13** No bar charts. A dot plot is usually clearer and makes comparisons easier.
- **FD14** Balance white space against data. Truncating an axis to focus on the informative range can help.
- **FD15** Be careful with sparse tails and outliers. They can mislead or squash the rest of the plot.
- **FD16** Truncate Kaplan-Meier follow-up once fewer than about 5 (or 10) patients remain at risk in any group. · KM (see S4.16)
- **FD17** No 3D plots for 2D data.
- **FD18** No coloured or dark backgrounds; use white or light grey.
- **FD19** No hatching or patterned fills.
- **FD20** Draw to scale. Time points at 1, 3, 6 and 12 months must be spaced in proportion to time, not evenly.
- **FD21** Avoid box-and-whisker plots unless there is a good reason. Violin plots, spike histograms or ridgeline plots show where the data cluster.
- **FD22** Tell multiple lines apart by dash style, clearly different shades of grey, or distinct colours.
- **FD23** Refer to every figure in the text.
- **FD24** Give each figure an informative title. Its interpretation goes in the text, which also cites the figure.
- **FD25** Use a figure to show how a continuous predictor relates to the outcome. The paper cites statistics item "4.8", but the intended item is S4.9.
- **FD26** Turn off automatic software legends and labels (e.g. "x = 1"/"x = 0"). Label the curves directly or use the caption.
- **FD27** Label the Kaplan-Meier x-axis with units and time zero ("Years from surgery", not "Time" or "analysis time"). Prefer years or months to days unless events happen over a short period. · KM
- **FD28** Label the Kaplan-Meier y-axis with the correctly defined endpoint, e.g. disease-free vs disease-specific survival. · KM (see S4.13)
- **FD29** When survival stays high, plot cumulative incidence (y-axis 0 to 0.1) rather than truncating the KM y-axis at 0.9–1. · KM
- **FD30** If the study is about group differences, do not show a separate CI for each group. Show the difference and its CI (see S4.5). · RCT/EFFECT

## 4. Table rules

- **FT1** Do not repeat the table's numbers in the text. Refer to every table and give an overall interpretation (e.g. "the cohort is typical apart from a high rate of prior negative biopsy").
- **FT2** Leave out rows or columns that can be derived from other data (see S4.2). Typical cases are a whole-cohort column next to the group columns, both percentages of a binary variable, and the same variable categorized two ways.
- **FT3** Give p values in tables only after thinking about the hypothesis (see S3.10). Baseline p values in an RCT test a null known to be true. Groups receiving different procedures are often known to differ already. In huge data sets (e.g. SEER) almost every difference is "significant".
- **FT4** Make the null hypothesis of each p value clear: global vs pairwise when there are 3+ groups. Never mix p values for different hypotheses in one column without labelling them.
- **FT5** Keep tables simple, avoiding multiple sub-columns and sub-rows.
- **FT6** For a categorical variable, use one overall test of association rather than a test at each level.
- **FT7** Avoid repetition and empty cells. Instead of repeating "p < 0.0001" down a column, say it once in a footnote. Put the statistic in the column header, e.g. "Mean (SD)". Mark the reference category with an asterisk rather than giving it an empty row.
- **FT8** Show the number of patients and the missing data, in headers ("PSA, ng/ml; N = 992"), as a "Missing" row, or in a footnote. State which statistics are shown, e.g. "median (IQR) or n (%)". Keep statistics and tests consistent within a table, and footnote any justified exception.
- **FT9** Apply the statistics guideline inside tables: median and quartiles rather than ranges (S4.3), appropriate precision (S4.1), and rescaled predictors such as OR per 10 years (S5.4).
- **FT10** Use clear labels and units, and make the reference group clear for every OR/HR. Spell out abbreviations in footnotes.
- **FT11** Do not split categorical variables into too many categories. Collapse clinical T stage into about 5 groups, for example, rather than 9.
- **FT12** Format for readability. Left-justify the row-label column and centre the data columns, indent subcategories, and consider bold headers.
- **FT13** Avoid the "±" notation; say whether you mean SD or 95% CI.
- **FT14** Do not overload a table. Split a long or wide one, e.g. demographic and disease variables in separate tables.
- **FT15** Tables are where detailed reference information belongs. Balance completeness against how easily readers can find the key numbers.

## 5. Suggested tools (from the paper, "Taking it further")
- Frank Harrell's graphics ideas: datamethods.org/t/journal-graphics
- R package `gtsummary` (by co-author Daniel Sjoberg) produces tables that follow these guidelines
- Tufte, *The Visual Display of Quantitative Information*; Cleveland, *The Elements of Graphing Data*
