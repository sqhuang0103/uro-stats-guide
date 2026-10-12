# Statistical analysis plan (SAP) workflow

The aim is a written plan, agreed before the analysis, in which every decision is made deliberately and tied to the guidelines. This is exactly what S3.9 asks for. The plan also settles in advance the arguments that would otherwise come up in co-author reviews, such as which covariates to include and why.

## Step 1: Gather information, conversationally

First pull everything you can from what the user has already said: the conversation, any protocol, data dictionary or draft. Then ask only for what is missing, a few questions at a time and most important first. Do not send a 20-question form.

If an answer is unknown, write it as an open question in the SAP rather than blocking on it.

Information needed, in priority order:

1. **Primary question and study type.** This is the most important answer, because it determines most of the plan. Classify the study:
   - **EFFECT**: does treatment or exposure X change the outcome? → adjust for confounders, and report the X estimate only (S5.3).
   - **ASSOC**: is factor or marker X associated with the outcome, independently of known factors? → report the X estimate, rescaled (S5.4).
   - **PRED**: build or validate a model that predicts the outcome → overfit correction, calibration and clinical consequences (S5.8–S5.12).
   - **DIAG**: should test or marker X be used to make a clinical decision? → clinical consequences and decision curves rather than sensitivity/specificity (S4.8, S5.10–S5.12).
   - Also: RCT, LONG, META.
   If the user's description is ambiguous between these types, ask directly, giving examples of each, because mixing the aims is a common root cause of guideline violations.
2. **Design and cohort**: data source, dates, inclusion criteria, consecutive or selected series, and the expected exclusions (S2.2).
3. **Outcome(s)**: definition and type. For time-to-event outcomes also collect:
   - time zero;
   - the event definition;
   - the censoring date for each endpoint;
   - how other-cause death is handled, and the correct endpoint name (S4.13).
4. **Main exposure or predictor(s)**: definition, timing (known at time zero? S4.15) and coding:
   - categorical variables entered as categories (S4.6);
   - continuous variables kept continuous (S4.7), with nonlinearity considered (S4.9);
   - a rescaling unit chosen (S5.4).
5. **Covariates**: for each candidate, the clinical or causal reason it belongs. This is the heart of the plan for EFFECT and ASSOC studies; see Step 2.
6. **Secondary questions**: subgroups and effect modifiers (S3.7), sensitivity analyses, and which results are exploratory (S3.5).
7. **Missing data and selection**: expected missingness, and how excluded or incomplete patients will be described (S6.5).
8. **Sample size and events**: the expected n, and the number of events for binary or time-to-event outcomes.

## Step 2: Covariate selection (the most common point of dispute)

The guidelines rule out choosing covariates by data-driven significance (S5.2, S3.9). That includes:
- univariable screening at p < 0.05;
- forward, backward or stepwise selection;
- adding a variable "because groups differed at baseline".

Help the user instead build a **pre-specified covariate table** with these columns:

| Variable | Definition / coding | Form in model | Reason for inclusion | Source of rationale |

- **Reason for inclusion**:
  - for EFFECT: a plausible confounder, i.e. it affects both exposure and outcome;
  - for ASSOC: an established prognostic factor that X must add to;
  - for PRED: an available and plausible predictor.
- **Source of rationale**: clinical knowledge, prior literature, an existing nomogram, and so on.
- **When candidates must be cut**, e.g. because the user's team wants to "rationalise" the list, use non-data-driven reasoning:
  - drop variables that are redundant with another, measured after the exposure or time zero, or with too much missing data;
  - merge collinear measures;
  - prefer the variable that is better measured.
  Record the reason for each variable dropped as well as for each one kept.
- **If the number of covariates looks large relative to the number of events**, say so. Label this as a general statistical concern that the two guidelines do not cover; S5.1 touches on it only for propensity methods. Do not invent a guideline rule such as a fixed events-per-variable threshold.
- **If the user still wants stepwise selection**, check whether the S5.2 exception applies: early model development with poor prior knowledge. If it does, log it under "Deviations" with a justification, and require that internal validation repeat the selection step (S5.8). If it does not, explain plainly what the reviewers at these journals will say.

## Step 3: Write the SAP

Use the headings below. Annotate each decision with the guideline item ID(s) in square brackets, e.g. "[S4.13]", so that co-authors and reviewers can trace it. Include a section only if it applies, and mark any unknown as "TBD: <what needs deciding, by whom>".

```
# Statistical Analysis Plan: <short title>
Version <n>, <date>. Prepared with reference to the urology statistics [Assel 2019] and figures/tables [Vickers 2020] guidelines.
Design reporting guideline to follow: <STROBE / CONSORT / TRIPOD / REMARK …> [S2.1]

## 1. Study design and population
Data source, dates (with rationale if not obvious), inclusion criteria, consecutive vs selected, planned exclusion steps (n to be reported at each) [S2.2]

## 2. Research questions
Primary: <question> — study type <EFFECT/ASSOC/PRED/DIAG> — target estimate (e.g. adjusted HR for X vs Y) [S2.4, S4.4]
Secondary / exploratory: … (interpreted in light of multiplicity) [S3.5]

## 3. Variables
3.1 Outcome(s): definition; for time-to-event: time zero, event, censoring rule, competing risks, endpoint name [S4.13]
3.2 Exposure / predictor(s): definition, timing relative to time zero [S4.15], coding [S4.6, S4.7], scaling unit [S5.4]
3.3 Covariates: the pre-specified covariate table [S5.2, S3.9, S2.5]

## 4. Primary analysis
Model, covariates, nonlinear terms (e.g. restricted cubic splines) [S4.7, S4.9], how the estimate and 95% CI will be reported [S4.4, S4.5]

## 5. Secondary and sensitivity analyses
Interaction terms for effect modification [S3.7], sensitivity analyses, landmark / time-dependent analyses if needed [S4.15]

## 6. Prediction model development and validation   (PRED/DIAG only)
Internal validation with overfit correction repeating all steps [S5.8]; calibration (external data only) [S5.9]; clinical consequences at illustrative thresholds [S5.11]; decision curve with a pre-specified sensible threshold range [S5.12]; no sens/spec for continuous models [S5.10]

## 7. Missing data and selection
Expected missingness; descriptive comparison of excluded / incomplete patients [S6.5]; ascertainment-bias considerations [S6.6]

## 8. Reporting plan
8.1 Table 1: variables, median (quartiles) / n (%), no whole-cohort column, p values only if a sensible hypothesis exists [S4.2, S4.3, FT2, FT3, FT8]
8.2 Main results table: which estimates are shown (for EFFECT studies, the exposure only, not covariate ORs/HRs) [S5.3, S5.5], precision rules [S4.1]
8.3 Figures: list each planned figure and what it must show (e.g. KM with numbers at risk, truncated at <5 at risk, x-axis "years from surgery") [FP3.1, FD6, FD16, FD27]
8.4 Language rules for write-up: no accepting the null, no "trend", no "may" in conclusions [S3.1, S3.2, S6.2]

## 9. Deviations from the guidelines
Each deliberate deviation, the item it departs from, and the justification [S1.1]

## 10. Open questions for the team
```

## Step 4: Review the plan with the user

After the draft, flag in two or three lines:
- any decision that still conflicts with a guideline item;
- the TBDs that block the analysis from starting.

Offer to turn the SAP into a pre-analysis checklist, or to draft the Methods statistics paragraph from it. A good SAP converts almost directly into that paragraph, which helps with S2.4 and S2.5.
