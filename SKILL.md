---
name: uro-stats-guide
description: Applies the joint urology-journal statistical reporting guidelines (Assel et al., Eur Urol 2019, co-published in J Urol, Urology and BJUI) and the companion figures and tables guidelines (Vickers et al., 2020). It has two functions. (1) CHECKLIST: generate a guideline checklist, or audit a manuscript, section, table, figure or co-author/reviewer comment against the guidelines. (2) SAP: interactively build a statistical analysis plan whose every decision is tied to guideline items. Use this skill whenever the user is planning, analysing, writing, revising or reviewing clinical research aimed at a urology journal (European Urology, Eur Urol Focus/Oncology, Journal of Urology, Urology, BJU International), or asks about the statistics or table/figure guidelines of those journals. Also use it whenever they debate variable selection, stepwise/univariable screening, covariate choice, p-value wording, Kaplan-Meier or survival reporting, Table 1 or regression-table formatting for a urology paper, or ask in Chinese for 统计分析计划, 投稿前检查, checklist, 泌尿 期刊 统计 指南, even if the guidelines are not named.
---

# uro-stats-guide

This skill applies two guidelines that statistical reviewers at the major urology journals use when assessing submissions:

- **Statistics**: Assel M, Sjoberg D, Elders A, et al. *Guidelines for Reporting of Statistics for Clinical Research in Urology.* Eur Urol 2019;75(3):358–367. Item IDs are `S1.1`–`S6.8`. See `references/stats-guideline.md`.
- **Figures and tables**: Vickers AJ, Assel MJ, Sjoberg DD, et al. *Guidelines for Reporting of Figures and Tables for Clinical Research in Urology.* 2020, published in Urology, Eur Urol, J Urol and BJUI. Item IDs are `FG`, `FP3.1`–`FP3.6`, `FD1`–`FD30` and `FT1`–`FT15`. See `references/figures-tables-guideline.md`.

The reference files paraphrase each item and tag it with the study types it applies to, the stage (plan or report), and the manuscript section where it shows. Those tags are what let either function pick out the items relevant to a particular study.

## Choose the function

| The user wants… | Function | Read |
|---|---|---|
| A checklist to work through; to have a draft, table, figure or abstract checked; to know whether a practice or comment is consistent with the guidelines | **Checklist** | `references/checklist-workflow.md` plus the guideline reference(s) it needs |
| To plan an analysis, decide on covariates or a model before analysing, or write or revise an analysis plan or the statistical methods | **SAP** | `references/sap-workflow.md` plus `references/stats-guideline.md` (and the figures/tables file for the reporting plan) |

If the request fits neither function exactly (e.g. "what does the guideline say about X?"), answer it directly from the reference files, citing item IDs. Neither workflow is needed.

If it is unclear which function the user wants, ask once. Otherwise go ahead.

## Ground rules (both functions)

**Stay within these two guidelines.** Cite items by ID so users can look them up. Some necessary points are not covered by either guideline, e.g. events-per-variable rules, specific missing-data methods, or design-specific guidelines such as STROBE or TRIPOD. Mention such a point only if it matters, and label it plainly as "not covered by these guidelines". This keeps users from attributing a rule to the journals that the journals never made.

**Paraphrase; do not fabricate quotations.** The reference files are paraphrases. If the user needs exact wording, for instance to quote it to a co-author, give the citation and suggest they check the original text.

**Respect the golden rule (S1.1).** The guidelines explicitly allow any item to be broken with a clear scientific justification. A departure is a decision to justify, not automatically an error. Help the user either change their approach or write the justification.

**Be concrete.** Name the item, show the evidence or the exact decision, and give the fix, with replacement wording where the problem is wording. Generic advice such as "consider improving reporting" does not help.

## Output

**Default: answer directly in the conversation**, using Markdown headings and tables. This suits most checklists, audits and SAPs.

Write a file only when the user asks for one:
- **Markdown file**: save a `.md` file to the current working directory, or to a path the user gives, with a descriptive name (e.g. `SAP_<study>_v1.md`, `checklist_<study>.md`). Tell them the path.
- **Web page**: if the environment provides an Artifact or page-publishing tool, follow that tool's own instructions to publish the page. Otherwise write a self-contained `.html` file. Checklists work well as pages with tick boxes, grouped by section.

If the answer would be very long (e.g. a full audit of a long manuscript), still answer in the conversation. Put the priority items first, compress the rows that are met, and offer the complete version as a `.md` file or web page in one line.

## Language

- **Reply in the language of the user's request.** A request written in Chinese gets a Chinese reply, and so on. If the language is unclear, use English.
- **Keep item IDs (S5.2, FT3…) unchanged in any language.** When replying in a language other than English, add the short English item name in parentheses the first time an item appears, e.g. "S5.2（避免逐步选择变量 / Avoid stepwise selection）", so the user can cite it to English-speaking co-authors and reviewers.
- **A document the user will submit or circulate** (e.g. the SAP, or replacement sentences for the manuscript) is usually in English even when the conversation is not. If the user is conversing in another language, write the explanation in their language and the drop-in manuscript text in English, unless they ask otherwise.
