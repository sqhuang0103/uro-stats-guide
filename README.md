# uro-stats-guide

A [Claude Code](https://claude.com/claude-code) skill that applies the joint statistical reporting guidelines of the major urology journals (*European Urology*, *The Journal of Urology*, *Urology*, *BJU International*) to your own research. It has two functions:

| Function | What it does |
|---|---|
| **Checklist** | Generates a checklist filtered to your study type, or audits a manuscript, table, figure or reviewer comment item by item. Every verdict comes with evidence and a concrete fix. |
| **Statistical analysis plan (SAP)** | Interactively builds an analysis plan in which every decision (covariates, variable coding, censoring, validation, tables, figures) is tied to a guideline item, so it can be defended to co-authors and reviewers. |

[中文说明见下方](#中文说明)

## Guidelines covered

| ID prefix | Guideline |
|---|---|
| `S1.1`–`S6.8` | Assel M, Sjoberg D, Elders A, et al. **Guidelines for Reporting of Statistics for Clinical Research in Urology.** *Eur Urol* 2019;75(3):358–367. doi:[10.1016/j.eururo.2018.12.014](https://doi.org/10.1016/j.eururo.2018.12.014). Free full text: [PMC6391870](https://pmc.ncbi.nlm.nih.gov/articles/PMC6391870/). Co-published in *J Urol*, *Urology* and *BJU Int*. |
| `FP`, `FD`, `FT` | Vickers AJ, Assel MJ, Sjoberg DD, et al. **Guidelines for Reporting of Figures and Tables for Clinical Research in Urology.** *Urology* 2020;142:1–13. doi:[10.1016/j.urology.2020.05.002](https://doi.org/10.1016/j.urology.2020.05.002). Free full text: [PMC7387170](https://pmc.ncbi.nlm.nih.gov/articles/PMC7387170/). Also in *Eur Urol* 2020;78:97–109, *J Urol* 2020;204:121–133 and *BJU Int* 2020;126:14–25. |

Figures/tables IDs: `FP3.x` are the six figure principles, `FD1`–`FD30` the figure dos and don'ts, and `FT1`–`FT15` the table rules.

Each item is tagged with:
- **Study type**: `RCT`, `EFFECT` (treatment/exposure effect), `ASSOC` (prognostic factor or marker association), `PRED` (prediction model), `DIAG` (test/marker for clinical use), `TTE` (time-to-event), `LONG`, `META`
- **Stage**: decide before analysis, or a reporting issue
- **Manuscript section** where compliance is visible

These tags let the skill show only the items relevant to your study.

## Install

```bash
git clone git@github.com:sqhuang0103/uro-stats-guide.git ~/.claude/skills/uro-stats-guide
```

Restart Claude Code (or start a new session) and the skill is available in every project. To update later:

```bash
cd ~/.claude/skills/uro-stats-guide && git pull
```

## Usage

Invoke it explicitly with `/uro-stats-guide`, or just describe what you need. The skill triggers on urology-journal statistics questions. Examples:

```text
Check the Methods and Results of draft_v3.docx against the urology statistics guidelines.

My co-author says adding variables one at a time violates the European Urology guidelines. Is that right?

Help me write a statistical analysis plan for a retrospective cohort comparing robotic vs open
radical cystectomy, outcome recurrence-free survival.

Give me a pre-submission checklist for a prediction model paper going to BJUI.

Review Table 1 and Figure 2 (attached) against the figures and tables guideline.
```

### Behaviour

- **Output** goes directly into the conversation by default. Ask for a Markdown file or a web page if you want one.
- **Language** follows your request (English by default). Item IDs such as `S5.2` stay unchanged in every language, and text meant for the manuscript is written in English.
- **Scope** is limited to these two guidelines. Points they do not cover (e.g. events-per-variable rules, STROBE/TRIPOD items) are explicitly labelled as such rather than attributed to the journals.
- **Golden rule (S1.1)**: the guidelines allow any item to be broken with a scientific justification. The skill treats a departure as a decision to justify, not an automatic error, and helps you write that justification.

## Repository structure

```text
uro-stats-guide/
├── SKILL.md                              # entry point: routing, ground rules, output and language
└── references/
    ├── stats-guideline.md                # S1.1–S6.8, paraphrased and tagged
    ├── figures-tables-guideline.md       # FP / FD / FT items, paraphrased and tagged
    ├── checklist-workflow.md             # blank checklist and audit workflow
    └── sap-workflow.md                   # SAP interview, covariate table, SAP template
```

## Disclaimer

The files in `references/` are **paraphrased summaries** written for this tool. They do not reproduce the original papers. Read and cite the originals.

This project is independent and is not affiliated with or endorsed by the guideline authors or the journals. It supports, but does not replace, review by a qualified statistician.

---

## 中文说明

`uro-stats-guide` 是一个 Claude Code skill。它依据四大泌尿外科期刊（*European Urology*、*J Urol*、*Urology*、*BJUI*）共同发布的统计报告指南和图表报告指南，帮你做两件事：

- **Checklist（检查清单）**：按你的研究类型筛选出适用的条目，生成清单；或者逐条审查稿件、表格、图、审稿或合作者意见。每条结论都附上稿件中的证据和具体的修改建议。
- **SAP（统计分析计划）**：通过问答一步步写出统计分析计划。协变量选择、变量编码、删失规则、模型验证、图表安排等每个决定都标注对应的指南条目，方便向合作者和审稿人说明依据。

**安装：**

```bash
git clone git@github.com:sqhuang0103/uro-stats-guide.git ~/.claude/skills/uro-stats-guide
```

**使用：** 输入 `/uro-stats-guide`，或者直接用中文提问，例如"帮我们的回顾性队列研究写一份统计分析计划"，或者"合作者说逐个加变量不符合 European Urology 的指南，对吗？"。

- 默认直接在对话中输出；如果需要，可以要求另存为 Markdown 文件或网页。
- 用中文提问就用中文回答。条目编号（如 S5.2）保持不变，第一次出现时会附上英文名称，方便直接引用给英文合作者。
- 只依据这两份指南。指南没有涉及的内容会明确标注出来。

**声明：** `references/` 中的内容是对原文的转述摘要，不是原文。使用时请阅读并引用原始论文。本项目与指南作者和期刊没有任何关联。
