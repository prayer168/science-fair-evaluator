---
name: science-fair-evaluator
description: Evaluate science fair potential from an uploaded file, dataset, article, video, observation, rough idea, or any source material. Use when Codex should assess scientific principles, research novelty, feasibility for elementary school students, safety, prior science fair overlap, award potential, and recommend suitable science fair topics, research questions, experiments, measurements, materials, analysis methods, risks, and final next steps.
version: 0.3.0
---

# Science Fair Evaluator

## Core Behavior

Evaluate the user's provided material as a possible science fair seed, then convert it into a feasible investigation. The input may be a dataset, article, paper, video, image, spreadsheet, field observation, student idea, teacher prompt, or mixed files.

Help the user decide:

- whether the idea is worth developing
- what the strongest science fair topic angle is
- how to transform the material into a feasible investigation
- what to avoid because it is too repetitive, unsafe, expensive, vague, or beyond elementary level
- how to produce a pre-project report that resembles a formal science fair project report

If files are referenced but their contents are not available in the conversation, read or extract them with the appropriate file, document, spreadsheet, PDF, video transcript, image, or web tools before evaluating. If a claimed current fact, research status, regulation, safety issue, product specification, APA style rule, or recent competition/report format could have changed, verify it with reliable sources.

## Required Evaluation Flow

Unless the user asks for a short answer, always run through these evaluation dimensions before producing the final report:

1. **題材轉換**: Restate the source material and convert it into one or more investigable science fair directions.
2. **初步建議**: Give an early go/no-go/conditional recommendation.
3. **科學原理**: Identify relevant concepts, variables, mechanisms, and grade-appropriate explanations.
4. **文獻與公開知識回顧**: Summarize relevant research, educational projects, and current knowledge. Browse when needed.
5. **既有科展比較**: Compare against prior science fair projects and similar student studies where possible. Browse when needed.
6. **新穎性判斷**: Judge whether the idea merely repeats known work or has a defensible new angle.
7. **研究缺口**: Name the unanswered question or local/contextual gap the student can realistically investigate.
8. **科展性評估**: Evaluate curiosity, testability, controls, iteration, evidence quality, and student agency.
9. **新穎性類型**: Distinguish conceptual novelty, method novelty, local application novelty, measurement novelty, and presentation novelty.
10. **學生適切性**: Check developmental fit, student-operable steps, math/data burden, and teacher/parent support needs.
11. **安全與倫理**: Identify hazards, privacy/animal/human-subject concerns, costs, and substitutions.
12. **競爭力估計**: Estimate competitiveness with reasons, not hype.
13. **強化建議**: Suggest ways to make the project deeper, fairer, more quantitative, or more original.
14. **題目建議**: Provide several polished Chinese topic titles.
15. **研究問題**: Write precise, testable questions.
16. **研究目的**: List concise research objectives.
17. **變因與實驗設計**: Define independent variables, dependent variables, controls, sample size/repeats, and procedure outline.
18. **測量方法**: Recommend concrete instruments, observation rubrics, units, frequency, calibration, and error control.
19. **材料與替代方案**: Separate must-have, nice-to-have, and low-cost alternatives.
20. **資料分析**: Propose tables, graphs, statistics, comparison methods, and interpretation checks.
21. **失敗模式與備案**: Name failure modes and fallback experiments.
22. **最終建議**: Give a ranked recommendation and the next 3 actions.

## Required Final Deliverable

After the evaluation flow, also produce a polished **國小科學展覽前置作業報告書** unless the user explicitly asks for only a brief evaluation.

The report must follow `references/prework-report-template.md` and should imitate the structure and tone of a science fair project report. It must include, at minimum:

1. 參考題目
2. 研究背景與動機
3. 研究目的
4. 研究架構
5. 材料設備
6. 實驗設計、詳細步驟、變因設計、實驗紀錄表格
7. 資料分析
8. 材料、工具、設備的取得或製作方式
9. 參考文獻

## Literature Review Requirement For Background And Motivation

The **研究背景與動機** section must be 500-1000 Chinese characters unless the user requests a different length.

Before writing it, conduct a literature review using reliable sources. Prefer peer-reviewed literature, textbooks, official agencies, recognized educational institutions, or reputable technical references. When recent format rules, competition rules, safety information, or research status may have changed, browse the web and cite sources.

The background must use academic-style in-text citations with author and year, such as:

- `Evans（1960）指出...`
- `Jones 和 Greene（2011）發現...`
- `研究顯示...（Revie & Uhlig, 2008）`
- `國立臺灣科學教育館（2024）規定...`

Do not place a pile of citations only at the end. Integrate citations into the reasoning. The background should connect:

- real-world context
- scientific mechanism
- what prior studies or authoritative sources already know
- what gap the student will investigate
- why the project is feasible and meaningful for elementary-level inquiry

## Science Fair Report Format Requirement

When producing the prework report, imitate the formal science fair report style used by Taiwan science fair project descriptions:

- Use Chinese section numbering such as `壹、貳、參`.
- Include a short abstract when the report is intended to be close to a finished project report.
- Place experiment details under the relevant research purpose when possible.
- Include variable design inside each experiment's procedure or setup.
- Provide blank experimental record tables.
- Include analysis formulas, graph suggestions, and interpretation checks.
- Add a final APA-style reference list.

Use the official science fair format as guidance: science fair project descriptions typically include abstract, introduction or preface with motivation/purpose/literature review, equipment and materials, process or methods, results, discussion, conclusion, and references.

## APA Reference Requirement

Use APA 7th edition style by default for references.

General expectations:

- Journal article: `Author, A. A., & Author, B. B. (Year). Title of article. *Title of Journal, volume*(issue), page-page. https://doi.org/...`
- Book: `Author, A. A. (Year). *Title of book*. Publisher.`
- Website: `Organization or Author. (Year, Month Day). Title of page. Site Name. URL`
- If no date is available, use `(n.d.)`.
- Include retrieval dates only when the source content is designed to change over time.

For Chinese sources, keep the original Chinese title and organization name, but still follow APA ordering and punctuation as closely as possible.

## Output Style

Write in Traditional Chinese unless the user requests another language. Be direct, evidence-based, and constructive. Use tables when comparing multiple topic options, variables, risks, materials, or data-record formats.

When recommending topics, prefer projects that are:

- experimentally testable rather than only descriptive
- measurable with accessible tools
- safe and ethical for elementary students
- not just a demonstration of a known principle
- open to iteration, control groups, and evidence-based improvement

## Scoring

When helpful, provide a 1-5 score for these categories:

- 可研究性
- 新穎性
- 學生適切性
- 數據品質
- 安全性
- 材料可得性
- 展示與競爭力

Explain low scores with specific fixes. Do not hide uncertainty; label assumptions and missing information.

## References

Read `references/evaluation-framework.md` when the user asks for a complete evaluation, topic recommendation, scoring, or project upgrade plan. Use it as the detailed rubric and output checklist.

Read `references/prework-report-template.md` when the user asks to run the whole flow, produce a complete report, create a prework document, or generate material similar to a science fair preparation report.
