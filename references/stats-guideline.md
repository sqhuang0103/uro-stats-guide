# Statistics guideline: item reference

Source: Assel M, Sjoberg D, Elders A, et al. *Guidelines for Reporting of Statistics for Clinical Research in Urology.* Eur Urol 2019;75(3):358–367. doi:10.1016/j.eururo.2018.12.014. Co-published in *The Journal of Urology*, *Urology* and *BJU International*, and adopted by *European Urology Focus* and *European Urology Oncology*. Statistical reviewers at these journals assess submissions against it.

Everything below paraphrases the paper. Cite items by their ID (e.g. "S5.2"). When a user needs the exact wording, send them to the paper rather than reconstructing a quotation.

## Tags

**Applies to** (study types):
- `ALL`: any quantitative clinical study
- `RCT`: randomized trial
- `EFFECT`: observational comparison of treatments or exposures, where the aim is to estimate an effect
- `ASSOC`: prognostic factor or marker association study ("is X associated with outcome?")
- `PRED`: prediction model development or validation
- `DIAG`: evaluation of a test, marker or model for clinical use (cut-points, sensitivity/specificity, decision curves)
- `TTE`: any analysis with a time-to-event outcome (combine with the above)
- `LONG`: change over time, or repeated measures
- `META`: meta-analysis

**Stage**:
- `PLAN`: must be decided before analysis, so it belongs in the SAP
- `REPORT`: concerns how results are written up
- `PLAN+REPORT`: both

**Section**: the manuscript section where compliance is visible (Methods / Results / Tables / Figures / Discussion / Conclusions).

## Contents
1. Golden rule (S1.1)
2. Reporting of design and analysis (S2.1–S2.5)
3. Inference and p values (S3.1–S3.10)
4. Reporting of study estimates (S4.1–S4.16)
5. Multivariable models and diagnostic tests (S5.1–S5.12)
6. Conclusions and interpretation (S6.1–S6.8)
7. Sections 7–8 (general remarks on p values; concluding remarks)

---

## 1. Golden rule

### S1.1 Any guideline may be broken when that makes scientific sense
- Applies: ALL · Stage: PLAN+REPORT · Section: any
- Gist: Science is too varied for universal rules. Authors may depart from any item, but they need to give a clear justification.
- Use: Never call a deviation an "error" outright. If the user has a reason, record it as a justified deviation and help them word the justification.

## 2. Reporting of design and statistical analysis

### S2.1 Follow the reporting guideline for your study type
- Applies: ALL · Stage: PLAN+REPORT · Section: Methods
- Gist: Use the design-specific reporting guideline, e.g. CONSORT (trials), REMARK (marker studies), TRIPOD (prediction models), STROBE (observational studies), AMSTAR (systematic reviews). These are available from the EQUATOR Network.
- Note: This skill covers only the two urology guidelines. Name the relevant design guideline, but do not audit against it.

### S2.2 Describe how the cohort was selected
- Applies: ALL · Stage: PLAN+REPORT · Section: Methods / Results
- Gist: Give the dates of the cohort, the inclusion criteria, and whether it is a consecutive series or a selected sample. List exclusions one at a time, each with its n, ending at the final analytic n. Obvious inclusion criteria can be omitted. Explain dates whose choice a reader might question.
- Check: Are the date range, the consecutive/selected status and a stepwise exclusion count with n per step all present?

### S2.3 Describe the practical steps of randomization (allocation concealment)
- Applies: RCT · Stage: PLAN+REPORT · Section: Methods
- Gist: Saying "a statistician made a list" or "envelopes were used" does not show concealment. State the exact logistics that prevented anyone from foreseeing or changing allocation, ideally a password-protected computer system.

### S2.4 Set out each study question and the analysis that addresses it
- Applies: ALL · Stage: PLAN+REPORT · Section: Methods
- Gist: A list of tests ("Mann-Whitney for continuous, Fisher for binary") is not enough. Take each primary question in turn, describe its analysis, and justify the approach where it is not obvious or alternatives exist. Explain uncommon methods.

### S2.5 Describe methods in enough detail for an independent statistician to replicate them
- Applies: ALL · Stage: PLAN+REPORT · Section: Methods
- Gist: "Adjusted for confounders" or "nonlinear approaches" is too vague. Name every covariate in each model and define any ambiguous variable precisely, including its coding (e.g. grade group entered as 1, 2, 3, 4–5 rather than "Gleason was included").

## 3. Inference and p values

### S3.1 Do not accept the null hypothesis
- Applies: ALL · Stage: REPORT · Section: Results / Discussion / Conclusions
- Gist: A p ≥ 0.05 means the null was not rejected. It does not show "no difference", "ineffective" or "unaffected". Write "no evidence of…" or "no statistically significant difference…" instead.
- Check: Search for "no difference", "did not affect", "was not associated", "equivalent", "similar" when these are backed only by a non-significant p.

### S3.2 A p value just above 0.05 is neither a trend nor "approaching significance"
- Applies: ALL · Stage: REPORT · Section: Results / Discussion
- Gist: The p value is not moving anywhere. Describe the evidence honestly, e.g. "some evidence of …, but differences did not meet conventional significance".
- Check: Search for "trend", "borderline", "marginally", "approaching", "tended to".

### S3.3 p values and CIs are not probabilities of a hypothesis
- Applies: ALL · Stage: REPORT · Section: Results / Discussion
- Gist: p = 0.03 does not mean a 3% chance the result is due to chance. A 95% CI is not a 95% probability that the true value lies inside it. A p value is the probability of data at least this extreme if the null were true.

### S3.4 Do not use confidence intervals to test hypotheses
- Applies: ALL · Stage: REPORT · Section: Results
- Gist: CIs are for estimation. Methods for CIs and for p values can disagree, so a CI excluding 1 and a p < 0.05 do not always coincide. Base claims of significance on the p value, and use the CI to describe precision.

### S3.5 Interpret multiple p values with multiplicity in mind
- Applies: ALL · Stage: PLAN+REPORT · Section: Methods / Results / Discussion
- Gist: The more tests you run, the more false positives you get. Formal adjustment suits only some settings (e.g. genomics). More often, interpret each p value in light of how many hypotheses were tested.
- Plan: Say which question is primary and which are secondary or exploratory.

### S3.6 Do not use separate within-group p values to answer a between-group question
- Applies: RCT, EFFECT, LONG · Stage: PLAN+REPORT · Section: Results
- Gist: One question gets one hypothesis and one p value. A significant change in arm A and a non-significant change in arm B does not show that A beats B. Test the difference between groups directly.

### S3.7 Use interaction terms rather than separate subgroup analyses
- Applies: RCT, EFFECT, ASSOC · Stage: PLAN+REPORT · Section: Methods / Results
- Gist: To ask whether an effect differs by subgroup, fit a treatment × subgroup interaction term. Within-subgroup estimates with CIs can be shown, but without per-subgroup p values.
- Plan: Pre-specify any effect modifiers to be tested this way.

### S3.8 Tests of change over time are usually uninteresting
- Applies: LONG · Stage: PLAN+REPORT · Section: Results
- Gist: A null of "no change over time" is often known to be false (e.g. function declines with age). Report the estimated change with a 95% CI rather than a paired-test p value.

### S3.9 Do not use statistical tests to choose the analysis
- Applies: ALL · Stage: PLAN · Section: Methods
- Gist: Examples include a normality test to choose between t-test and Mann-Whitney, a heterogeneity test to choose fixed or random effects, and a baseline-difference test to decide whether to adjust for a covariate. These tests often check nulls already known to be false, and switching methods on their result is of doubtful value. Follow a pre-specified plan, and change it only if the data clearly point to a better alternative.
- Plan: This is the main justification for a written SAP. Covariates must not be chosen by testing whether groups differ on them.

### S3.10 State the hypothesis each p value tests, and make sure it is a sensible one
- Applies: ALL · Stage: REPORT · Section: Results / Tables
- Gist: With three groups, say whether the p value is global or pairwise. Some hypotheses are not worth testing. For example, baseline p values in an RCT test a null that is known to be true.

## 4. Reporting of study estimates

### S4.1 Report numbers to an appropriate precision
- Applies: ALL · Stage: REPORT · Section: Results / Tables
- Rules:
  1. Give p values to 1 significant figure, or 2 when close to 0.05. Small values can be written "<0.001". Do not write "NS". Examples of correct reporting: <0.001, 0.004, 0.045, 0.13, 0.3, 1.
  2. Give percentages, rates and probabilities to 2 significant figures (75%, 3.4%, 0.13%).
  3. Never report p = 0.
  4. Give no decimals when a value is exactly 1 or 100% (not "1.00" or "100.00%"). Do not add decimals to integer-only data reported per person.
  5. Rarely give more than 3 significant figures.
  6. Give HR and OR to 2 decimals, except for large ratios (18.2, not 18.17).

### S4.2 Avoid redundant descriptive statistics
- Applies: ALL · Stage: REPORT · Section: Results / Tables
- Gist: Leave out anything derivable from numbers already given: both sexes' percentages, a whole-cohort column next to the group columns, or the same variable categorized two ways.

### S4.3 Describe data with median and quartiles rather than mean and SD/SE; avoid ranges
- Applies: ALL · Stage: REPORT · Section: Results / Tables
- Gist: The range reflects just two patients.

### S4.4 Report an estimate for each main study question
- Applies: ALL · Stage: PLAN+REPORT · Section: Results
- Gist: When comparing groups, report the difference between them, not only each group's value and whether p < 0.05. For a prognostic factor, report its strength (OR/HR) as well as the p value.
- Plan: Name the estimand (target estimate) for each primary question.

### S4.5 Give 95% CIs for the main estimates only
- Applies: ALL · Stage: REPORT · Section: Results / Tables / Figures
- Gist: Give a CI for the key estimate, such as the between-group difference. Do not give CIs for each group's own rate, or for descriptive statistics such as mean age.

### S4.6 Do not treat categorical variables as continuous
- Applies: ALL · Stage: PLAN+REPORT · Section: Methods / Results
- Gist: Ordinal categories such as ISUP grade group are not equally spaced. Describe them as categories, and enter them into models as category indicators rather than as one "per 1-point" term.

### S4.7 Do not categorize continuous variables without a convincing reason
- Applies: ALL · Stage: PLAN · Section: Methods
- Gist: Dichotomizing (age ≥60) or splitting into quantiles assumes everyone in a category shares the same risk. Keep variables continuous, rescale them for interpretation (see S5.4), and consider nonlinear terms such as splines.

### S4.8 Do not use statistical methods to find cut-points for clinical practice
- Applies: ASSOC, DIAG, PRED · Stage: PLAN · Section: Methods
- Gist: Choosing the cut-point with the smallest p value, or the one maximizing sensitivity + specificity (Youden, the corner of the ROC curve), ignores clinical consequences. Missing disease is usually worse than unnecessary treatment.

### S4.9 Show continuous associations graphically, preferably with nonlinear modelling
- Applies: ASSOC, EFFECT, PRED · Stage: PLAN+REPORT · Section: Figures
- Gist: Plot the predictor against predicted risk, with a CI, using nonlinear terms so that thresholds or changes in slope can be seen.
- Note: The figures/tables guideline (FD25) cites this item as "4.8", which is a numbering slip in that paper. This is the item it means.

### S4.10 Do not ignore significant heterogeneity in meta-analyses
- Applies: META · Stage: PLAN+REPORT · Section: Results / Discussion
- Gist: Do more than report a random-effects estimate. Look into the sources of heterogeneity (shared features of concordant studies, peculiarities of outlying ones).

### S4.11 Time-to-event: report the number of events, not a crude proportion
- Applies: TTE · Stage: REPORT · Section: Results
- Gist: "10 of 60 (17%) died" means little when follow-up varies. Report events plus Kaplan-Meier style probabilities (e.g. 5-year risk) or the median survival.

### S4.12 Time-to-event: describe follow-up using patients without the event
- Applies: TTE · Stage: REPORT · Section: Results
- Gist: Give median follow-up among event-free patients, or the number followed event-free for at least X years. Median follow-up across all patients is misleading.

### S4.13 Time-to-event: state when follow-up starts and how and when patients are censored
- Applies: TTE · Stage: PLAN+REPORT · Section: Methods
- Gist: Censor at the last date the patient was known to be event-free for *that* endpoint. For metastasis-free survival this is the last negative scan or undetectable PSA, not the last contact. Last contact is fine for overall survival.
  - For disease-specific endpoints, think about deaths from other causes. Censoring them can introduce bias when other-cause death is common or related to the predictor, and a competing-risks analysis is then appropriate.
  - In "disease-free survival", death from any cause counts as an event. If other-cause deaths are censored, call the endpoint "freedom from progression".
- Plan: Write down time zero, the event definition, the censoring date per endpoint, and how competing risks are handled.

### S4.14 Time-to-event: do not report mean follow-up, mean survival, or survival among those who had the event
- Applies: TTE · Stage: REPORT · Section: Results
- Gist: None of these is valid with censored data.

### S4.15 Time-to-event: all predictors must be known at time zero; otherwise use a landmark analysis or time-dependent covariates
- Applies: TTE · Stage: PLAN · Section: Methods
- Gist: Using information that becomes available only after the clock starts is invalid. Examples: response to chemotherapy when time is counted from the first dose; PSA velocity calculated from later PSA values. This is commonly called immortal time bias.
  - Landmark analysis: start the clock at a fixed later time point, include only patients still at risk then, and fix the variable's status at that point.
  - Time-dependent covariate: update the variable as new information arrives.

### S4.16 Kaplan-Meier figures: show the number at risk and truncate when numbers are small
- Applies: TTE · Stage: REPORT · Section: Figures
- Gist: Include a number-at-risk table. Truncate the curve once fewer than about 5 (or 10) patients remain at risk in any group.

## 5. Multivariable models and diagnostic tests

### S5.1 Multivariable, propensity and instrumental-variable methods are not a cure for confounding
- Applies: EFFECT, ASSOC · Stage: PLAN+REPORT · Section: Methods / Discussion
- Gist: Adjustment only balances covariates as they were recorded. Coarse coding hides residual differences (two T2c tumours can be very different), and unmeasured confounders remain. Propensity methods generally give results very similar to regression, except when there are many covariates relative to events. Instrumental-variable analysis needs a strong, valid instrument, which is rarer than people assume.
- Check: Watch for claims that adjustment "removes confounding", "makes groups comparable" or "mimics an RCT".

### S5.2 Avoid stepwise selection
- Applies: EFFECT, ASSOC, PRED · Stage: PLAN · Section: Methods
- Gist: This covers two practices: putting variables into a multivariable model only if they were significant in univariable analysis, and fitting everything then dropping non-significant terms. Data-driven selection of this kind raises the risk of overfit and makes CIs and other statistics unreliable.
- Exception stated in the paper: stepwise selection can be acceptable in a few situations, e.g. early in model development when little is known about which variables are predictive.
- Plan: Choose covariates in advance from clinical knowledge, prior literature or causal reasoning, and record the reason for each. If the user really is in the early-development exception, record it as a justified deviation (S1.1), and remember that internal validation must then repeat the selection step (S5.8).

### S5.3 When the aim is the effect of an intervention, do not report OR/HR for the covariates
- Applies: EFFECT, RCT · Stage: PLAN+REPORT · Section: Results / Tables
- Gist: Adjustment variables (stage, grade, PSA) are there to control confounding. Their own ratios are already known and draw attention away from the main estimate. Report the effect estimate for the intervention or exposure.
- Plan: Decide early whether the study is EFFECT or ASSOC/PRED, because that determines whether a full coefficient table is appropriate.

### S5.4 Rescale predictors so estimates can be interpreted
- Applies: ASSOC, EFFECT, PRED · Stage: PLAN+REPORT · Section: Results / Tables
- Gist: An OR per year of age of 1.02 (1.01, 1.02) is uninformative. Rescale, e.g. per 10 years, to get 1.16 (1.10, 1.22).

### S5.5 Do not report both univariable and multivariable results without good reason
- Applies: ASSOC, EFFECT, PRED · Stage: PLAN+REPORT · Section: Results / Tables
- Gist: The comparison is worth showing only when it addresses a mechanism question, e.g. whether an effect of race is explained by income and access to care. Routinely showing both is discouraged.

### S5.6 Do not rank predictors by strength
- Applies: ASSOC, PRED · Stage: REPORT · Section: Results / Discussion
- Gist: Claims such as "the marker was the strongest predictor" are not meaningful. Ratios depend on the units used, continuous and categorical variables cannot be compared, and prevalence matters too.

### S5.7 Discrimination depends on the predictors and the data set, not on the model
- Applies: PRED, DIAG · Stage: REPORT · Section: Discussion
- Gist: AUC/C-index is driven by which predictors are available and by how much they vary in the sample. Comparing models' discrimination across different data sets needs care.

### S5.8 Correct for overfit in internal validation
- Applies: PRED · Stage: PLAN+REPORT · Section: Methods
- Gist: Use cross-validation or the bootstrap, and *repeat every model-building step* inside each resample, including any variable selection. Then compute AUC and similar statistics from the out-of-sample predictions.

### S5.9 Report and interpret calibration correctly
- Applies: PRED · Stage: PLAN+REPORT · Section: Results / Figures
- Gist: Calibration on the development data, even cross-validated, is almost always good, so it is rarely worth reporting. On independent validation of a pre-specified model, show a calibration plot. Do not use the Hosmer-Lemeshow test. Calibration belongs to a model in a particular population; a model is not "well calibrated" in general.

### S5.10 Do not report sensitivity and specificity for continuous predictors or models
- Applies: DIAG, PRED · Stage: REPORT · Section: Results
- Gist: This includes sensitivity/specificity at an arbitrary cut-point and specificity at a fixed sensitivity. Without prevalence and the relative harms of errors, these figures cannot tell anyone whether to use the test.

### S5.11 Report the clinical consequences of using the test or model
- Applies: DIAG, PRED · Stage: PLAN+REPORT · Section: Results
- Gist: Pick illustrative thresholds and report what would happen at each, e.g. biopsies done or avoided, cancers found or missed per 1000 patients.

### S5.12 Interpret decision curves against sensible threshold probabilities
- Applies: DIAG, PRED · Stage: PLAN+REPORT · Section: Results / Discussion
- Gist: Benefit at thresholds no clinician would use (e.g. 35–65% for biopsy decisions about high-grade cancer) means no benefit in practice. Specify the clinically reasonable range of thresholds in advance.

## 6. Conclusions and interpretation

### S6.1 Draw a conclusion; do not restate the results
- Applies: ALL · Stage: REPORT · Section: Conclusions
- Gist: State what the findings mean for research or clinical practice.

### S6.2 Avoid "may" and "might" in conclusions
- Applies: ALL · Stage: REPORT · Section: Conclusions / Abstract
- Gist: "X may benefit" was already true before the study, so the sentence adds nothing. The paper says this alone can justify rejection.

### S6.3 Statistical significance does not mean clinical significance
- Applies: ALL · Stage: REPORT · Section: Discussion / Conclusions
- Gist: Clinical recommendations need an explicit analysis of clinical implications.

### S6.4 Avoid pseudo-limitations; discuss specific biases and how they would affect the findings
- Applies: ALL · Stage: REPORT · Section: Discussion
- Gist: "Small sample" or "retrospective" is not a limitation in itself. Discuss how likely each bias is, which direction it would push the results, and how large its effect might be.

### S6.5 Consider the impact of missing data and patient selection
- Applies: ALL · Stage: PLAN+REPORT · Section: Methods / Results / Discussion
- Gist: Compare patients who have missing data, or who were not selected, with those analysed. Formal missing-data adjustment is warranted only in some situations, but simple descriptive comparisons are easy and useful.
- Plan: Plan how excluded or incomplete patients will be described.

### S6.6 Consider ascertainment bias
- Applies: ALL (especially ASSOC, DIAG) · Stage: PLAN+REPORT · Section: Discussion
- Gist: This arises when the chance of being tested for the outcome depends on the predictor, e.g. biopsy triggered by PSA, or more frequent biopsies in active surveillance after worse results.

### S6.7 Do not confuse a poor outcome with a poor response to treatment
- Applies: ASSOC, EFFECT · Stage: REPORT · Section: Discussion / Conclusions
- Gist: When all patients received the same treatment, a subgroup with worse outcomes is not thereby a poor candidate for that treatment; such patients may need it most.

### S6.8 Be cautious about causal language
- Applies: ASSOC, EFFECT · Stage: REPORT · Section: Discussion / Conclusions
- Gist: If the stated aim is association, the conclusion must not imply that changing X would change the outcome.

## 7–8. General remarks (no numbered items)
- The paper follows the American Statistical Association's statement on p values. A p value is only one input. Conclusions also weigh methodology, other evidence, biological plausibility and effect size, and dividing studies into "positive" and "negative" by p < 0.05 is discouraged.
- The guidelines cover common practice and are not a complete account of medical statistics. A paper can meet every item and still be flawed, or break several and be sound.
