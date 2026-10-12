# uro-stats-guide

A [Claude Code](https://claude.com/claude-code) skill that applies the joint statistical reporting guidelines of the major urology journals to your own research. It has two functions:

1. **Checklist**: generates a checklist tailored to your study type, or audits a manuscript, table, figure or reviewer comment item by item. Each finding comes with evidence and a suggested fix.
2. **Statistical analysis plan (SAP)**: an interactive workflow that builds an analysis plan in which every decision (covariates, coding, censoring, validation, tables, figures) is tied to a guideline item.

## Guidelines covered

- Assel M, Sjoberg D, Elders A, et al. **Guidelines for Reporting of Statistics for Clinical Research in Urology.** *Eur Urol* 2019;75(3):358–367. doi:[10.1016/j.eururo.2018.12.014](https://doi.org/10.1016/j.eururo.2018.12.014). Free full text: [PMC6391870](https://pmc.ncbi.nlm.nih.gov/articles/PMC6391870/). Also published in *J Urol*, *Urology* and *BJU Int*.
- Vickers AJ, Assel MJ, Sjoberg DD, et al. **Guidelines for Reporting of Figures and Tables for Clinical Research in Urology.** *Urology* 2020;142:1–13. doi:[10.1016/j.urology.2020.05.002](https://doi.org/10.1016/j.urology.2020.05.002). Free full text: [PMC7387170](https://pmc.ncbi.nlm.nih.gov/articles/PMC7387170/). Also published in *Eur Urol* 78:97–109, *J Urol* 204:121–133 and *BJU Int* 126:14–25.

The files in `references/` are **paraphrased summaries** of these papers, organised by item number and tagged by study type, stage and manuscript section. They do not reproduce the original text and do not replace it. Please read and cite the original papers.

## Install

```bash
git clone <this-repo-url> ~/.claude/skills/uro-stats-guide
```

Claude Code picks the skill up automatically. You can invoke it with `/uro-stats-guide`, or just ask, e.g. "check my draft against the urology statistics guidelines" or "help me write an SAP for my cohort study".

## Behaviour

- Output appears directly in the conversation by default. Ask for a Markdown file or a web page if you want one.
- Replies follow the language of your request (default English). Guideline item IDs such as `S5.2` and `FT3` stay the same in every language.

## Disclaimer

This is an independent tool. It is not affiliated with or endorsed by the guideline authors or the journals. It supports, but does not replace, review by a qualified statistician.
