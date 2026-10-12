# Checklist workflow

There are two modes. Work out which one the user wants from the request:

- **Blank checklist**: the user wants a list to work through themselves, e.g. before writing, during writing, or before submitting. No manuscript is supplied.
- **Audit**: the user supplies a draft, a section, a table, a figure description, or a reviewer's comment, and wants it checked.

If the user gives both a document and a request for "a checklist", they almost always mean an audit.

## Step 1: Determine the applicable study types

Use the tags in `stats-guideline.md`: RCT, EFFECT, ASSOC, PRED, DIAG, TTE, LONG, META. A study can have several, e.g. EFFECT + TTE.

- Infer the study type from the manuscript or the description wherever possible. The distinction that matters most is **EFFECT vs ASSOC vs PRED**, because items S5.2–S5.12 and S6.7–S6.8 depend on it.
- Ask only if the type really cannot be inferred, and then ask one short question. For a blank checklist with no context, ask:
  - What is the main question?
  - Is the outcome time-to-event?
- In audit mode, never ask if the document answers the question.

Then build the item list:
- All items tagged `ALL`, plus those matching the study types.
- All FP, FD and FT items, if the work has tables or figures. Drop KM-only items when there is no time-to-event outcome, and PRED-only figure items when there is no prediction or marker component.

## Step 2a: Blank checklist output

Group items by **manuscript section**, not by guideline chapter. Each group is a table whose columns are ID, item, and what to check. A Status column is optional. Use this order:

1. Methods: design and cohort
2. Methods: analysis plan (the PLAN-stage items, marked "decide before analysis")
3. Results: estimates and inference
4. Tables
5. Figures
6. Discussion and conclusions

Keep each "what to check" cell to one concrete, checkable sentence. "Exclusions listed one by one with n for each" is concrete; "Describe cohort well" is not.

If the user names a stage, include only the relevant items:
- **Pre-analysis**: PLAN items. Suggest the SAP workflow instead, which handles these better.
- **Pre-submission**: everything.

End the checklist with one line on S1.1: any item may be departed from with a stated justification.

## Step 2b: Audit

1. **Read the material.** For .docx, try `pandoc -t plain` or `python -m docx2txt` if available, or unzip and strip `word/document.xml`. For .pdf, use the Read tool or `pdftotext`. If the text cannot be extracted, say so and ask for a different format. Never audit content you have not read.

2. **Check each applicable item** against the text, and assign one status:
   - ✅ **Met**: you can point to the passage that satisfies it.
   - ❌ **Not met**: you can point to a violation, or the required element is clearly absent.
   - ⚠️ **Partly met**: some elements are present and others missing.
   - ➖ **Not applicable**: briefly say why, if it is not obvious.
   - ❔ **Cannot assess**: the relevant material was not supplied, e.g. figures are missing from a text-only file. Do not guess.
   - 🔷 **Justified deviation**: the authors depart from the item and give a reason (S1.1). Say whether the reason seems adequate.

   Only mark Met or Not met when you can cite evidence: a short quote, or a location such as "Methods ¶3" or "Table 2, row 'Age'". Unsupported verdicts make the audit untrustworthy, and a wrong ✅ is worse than a ❔.

3. **Rank the problems.**
   - **High**: problems that threaten the validity of the inferences. Typical examples are stepwise or univariable screening (S5.2), immortal time bias (S4.15), wrong censoring (S4.13), accepting the null (S3.1), causal claims from associations (S6.8), and the absence of a between-group estimate (S4.4).
   - **Medium**: reporting problems a statistical reviewer will reliably flag, such as S4.5, S4.7, S5.3, S5.5, FT3 and FD6.
   - **Low**: precision and formatting issues, such as S4.1, FT12 and FD2.

4. **Output** in this structure:
   - **Summary**: 2–4 sentences covering the study type(s) assumed, how many items were checked, and the counts by status.
   - **Priority fixes**: the High and Medium ❌/⚠️ items, most serious first. For each, give the ID, the problem with its evidence, and a concrete fix. Where wording is the issue, include suggested replacement text.
   - **Full checklist**: section-grouped tables with columns ID | Item | Status | Evidence / note. Collapse long runs of ✅ items into a single line per section if the table gets very long, e.g. "S2.2, S2.5, S4.3 met".
   - **Cannot assess**: what extra material would allow these items to be checked.

## Checking a single comment or practice

Sometimes the request is narrow, e.g. "a co-author says our forward selection violates the guidelines, are they right?" In that case, answer directly:
- the relevant item(s) and what they say;
- whether any exception applies;
- what to do instead;
- how to word a justification, if the user has a legitimate reason to deviate.

A full checklist is unnecessary here.
