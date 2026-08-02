---
name: science-fair-evaluator
description: Evaluate science fair potential from an uploaded file, dataset, article, video, observation, rough idea, or any source material. Use when Codex should assess scientific principles, research novelty, feasibility for elementary school students, safety, prior science fair overlap, award potential, and recommend suitable science fair topics, research questions, experiments, measurements, materials, analysis methods, risks, and final next steps.
version: 0.6.0
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
2. **相似研究搜尋**: Search domestic and international websites, science fair databases, educational demonstrations, official/technical sources, and academic literature for similar experiments before finalizing the topic.
3. **相似研究比較表**: Summarize what has already been done, including source, investigated variables, methods, findings, overlap with the proposed idea, and what remains untested.
4. **創新性、可執行性與獲獎潛力評估**: Score and explain candidate topic directions for novelty, feasibility, safety, data quality, student agency, local relevance, and award potential.
5. **最佳題目推薦**: Recommend one best topic only, with a short reason. Do not produce the full report around multiple competing topics.
6. **初步建議**: Give an early go/no-go/conditional recommendation for the selected best topic.
7. **科學原理**: Identify relevant concepts, variables, mechanisms, and grade-appropriate explanations.
8. **文獻與公開知識回顧**: Summarize relevant research, educational projects, and current knowledge. Browse when needed.
9. **既有科展比較**: Compare against prior science fair projects and similar student studies where possible. Browse when needed.
10. **新穎性判斷**: Judge whether the idea merely repeats known work or has a defensible new angle.
11. **研究缺口**: Name the unanswered question or local/contextual gap the student can realistically investigate.
12. **科展性評估**: Evaluate curiosity, testability, controls, iteration, evidence quality, and student agency.
13. **新穎性類型**: Distinguish conceptual novelty, method novelty, local application novelty, measurement novelty, and presentation novelty.
14. **學生適切性**: Check developmental fit, student-operable steps, math/data burden, and teacher/parent support needs.
15. **安全與倫理**: Identify hazards, privacy/animal/human-subject concerns, costs, and substitutions.
16. **競爭力估計**: Estimate competitiveness with reasons, not hype.
17. **強化建議**: Suggest ways to make the project deeper, fairer, more quantitative, or more original.
18. **研究問題**: Write precise, testable questions.
19. **研究目的**: List concise research objectives.
20. **變因與實驗設計**: Define independent variables, dependent variables, controls, sample size/repeats, and procedure outline.
21. **測量方法**: Recommend concrete instruments, observation rubrics, units, frequency, calibration, and error control.
22. **材料與替代方案**: Separate must-have, nice-to-have, and low-cost alternatives.
23. **資料分析**: Propose tables, graphs, statistics, comparison methods, and interpretation checks.
24. **失敗模式與備案**: Name failure modes and fallback experiments.
25. **最終建議**: Give a ranked recommendation and the next 3 actions.

## Topic Formulation Requirement

Before writing `參考題目` or choosing the formal title, search for similar domestic and international work. Use a mix of:

- Taiwan science fair databases or local science fair PDFs
- international classroom demonstrations or university demo pages
- academic literature or technical articles
- official or reputable safety/engineering sources

Then provide a compact comparison showing:

- what similar work already tested
- how close it is to the user's idea
- whether the idea is repetitive
- what variable, method, context, measurement, or analysis can make it more original
- feasibility for elementary students
- safety constraints
- likely science fair competitiveness

Finally, recommend **one best topic** and use that topic consistently throughout the rest of the report.

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

## Research Purpose To Experiment Mapping Requirement

The **研究過程與方法** section must be generated from the items listed under **研究目的**. For every research purpose, create 2-3 child experiments whenever scientifically feasible.

Number experiments sequentially across the whole report:

- `研究目的一` -> `實驗 1`, `實驗 2`, `實驗 3`
- `研究目的二` -> `實驗 4`, `實驗 5`, `實驗 6`
- and so on

If a purpose only supports one valid experiment, explain why and add a small extension experiment such as a reliability check, calibration check, comparison condition, or pilot test. Do not invent unsafe, irrelevant, or redundant experiments just to fill the count.

Every child experiment must include:

- 實驗目的
- 操縱變因、應變變因、控制變因
- 對照組、實驗組
- 實驗時間
- 詳細實驗步驟
- 實驗紀錄表格
- 建議圖表
- 可能誤差與控制方法
- safety notes when applicable

The report should make it easy to see that all experiments are justified by the research purposes, not appended as unrelated activities.

Each child experiment must contain a full procedure, not only a summary table. A table may summarize variables and groups, but it must be followed by numbered operational steps, record-table fields, chart suggestions, and error-control notes.

## Detailed Acquisition And Safety Requirement

The **材料、工具、設備的取得或製作方式** section must be detailed. Include likely purchase locations, online search terms, school sources, household substitutions, adult-only preparation, approximate specifications, storage, labeling, calibration, disposal, and low-cost alternatives.

The **安全、倫理與風險控管** section must also be detailed. Include hazard source, possible accident, severity, prevention, required protective equipment, adult-only steps, emergency response, waste handling, and safer substitutions.

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

The final reference section title must be **參考文獻**. Do not use `參考來源`, `參考資料`, `來源`, or a plain link list as the final heading. If the report uses numbered Chinese sections, use a heading such as `拾肆、參考文獻`.

General expectations:

- Journal article: `Author, A. A., & Author, B. B. (Year). Title of article. *Title of Journal, volume*(issue), page-page. https://doi.org/...`
- Book: `Author, A. A. (Year). *Title of book*. Publisher.`
- Website: `Organization or Author. (Year, Month Day). Title of page. Site Name. URL`
- If no date is available, use `(n.d.)`.
- Include retrieval dates only when the source content is designed to change over time.

For Chinese sources, keep the original Chinese title and organization name, but still follow APA ordering and punctuation as closely as possible.

The reference list must include both domestic and international sources when possible. Provide accessible links whenever available. If a source has no public link, verify its bibliographic details from reliable catalog, publisher, DOI, official, or library records and state enough details for the user to find it.

Every item under **參考文獻** must be formatted as an APA-style bibliography entry, not as a bullet that only names the source or URL. Links may appear inside the APA entry.

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
