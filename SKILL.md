---
name: science-fair-evaluator
description: Evaluate science fair potential from an uploaded file, dataset, article, video, observation, rough idea, or any source material. Use when Codex should assess scientific principles, research novelty, feasibility for elementary school students, safety, prior science fair overlap, award potential, and recommend suitable science fair topics, research questions, experiments, measurements, materials, analysis methods, risks, and final next steps.
version: 0.2.0
---

# Science Fair Evaluator

## Core Behavior

Evaluate the user's provided material as a potential science fair seed. The input may be a dataset, article, paper, video, image, spreadsheet, field observation, student idea, teacher prompt, or mixed files. Produce a practical evaluation that helps the user decide:

- whether the idea is worth developing
- what the strongest science fair topic angle is
- how to transform the material into a feasible investigation
- what to avoid because it is too repetitive, unsafe, expensive, vague, or beyond elementary level

If files are referenced but their contents are not available in the conversation, read or extract them with the appropriate file, document, spreadsheet, PDF, video transcript, image, or web tools before evaluating. If a claimed current fact, research status, regulation, safety issue, product specification, or recent competition record could have changed, verify it with reliable sources.

## Required Final Deliverable

After completing the evaluation flow, also produce a polished **國小科學展覽前置作業報告書** unless the user explicitly asks for only a brief evaluation. This report is not a loose summary; it should be a practical pre-project document that a teacher, parent, or student can use to start the science fair project.

Use the report format in `references/prework-report-template.md`. Adapt headings to the actual project, but keep the same functional coverage:

- research title options
- research background and motivation
- importance of the study
- key terms
- scientific principles
- research questions
- research objectives
- hypotheses
- variables and controls
- materials and instruments
- experimental design and procedures
- measurement and record methods
- suggested data tables
- data analysis formulas and graph plans
- expected results
- safety, ethics, and risk controls
- feasibility and schedule
- fallback plans
- final recommended next actions

When the input is still vague, make reasonable assumptions and label them. When the report needs values such as concentrations, sample sizes, time span, or measurement units, provide conservative starting values that can be adjusted after a pilot test.

## Required Evaluation Flow

Always include these sections unless the user asks for a shorter format:

1. **題目理解與重新定義**: Restate the source material and convert it into one or more investigable science fair directions.
2. **初步結論**: Give an early go/no-go/conditional recommendation.
3. **科學原理**: Identify the relevant concepts, variables, mechanisms, and grade-appropriate explanations.
4. **國內外研究現況**: Summarize relevant public research, educational projects, and current knowledge. Browse when needed.
5. **歷屆科展與相近研究**: Compare against prior science fair projects and similar student studies where possible. Browse when needed.
6. **重複性與創新性判斷**: Judge whether the idea merely repeats known work or has a defensible new angle.
7. **研究缺口**: Name the unanswered question or local/contextual gap the student can realistically investigate.
8. **科展精神與探究成熟度**: Evaluate curiosity, testability, controls, iteration, evidence quality, and student agency.
9. **創新性**: Distinguish conceptual novelty, method novelty, local application novelty, measurement novelty, and presentation novelty.
10. **國小適切性**: Check developmental fit, student-operable steps, math/data burden, and teacher/parent support needs.
11. **安全、倫理與設備限制**: Identify hazards, privacy/animal/human-subject concerns, costs, and substitutions.
12. **獲獎潛力分析**: Estimate competitiveness with reasons, not hype.
13. **題目升級方向**: Suggest ways to make the project deeper, fairer, more quantitative, or more original.
14. **建議題目名稱**: Provide several polished Chinese topic titles.
15. **建議研究問題**: Write precise, testable questions.
16. **建議研究目的**: List concise research objectives.
17. **建議實驗架構**: Define independent variables, dependent variables, controls, sample size/repeats, and procedure outline.
18. **建議量測方法**: Recommend concrete instruments, observation rubrics, units, frequency, calibration, and error control.
19. **所需要的材料與工具**: Separate must-have, nice-to-have, and low-cost alternatives.
20. **建議資料分析**: Propose tables, graphs, statistics, comparison methods, and interpretation checks.
21. **風險與備案**: Name failure modes and fallback experiments.
22. **最終建議**: Give a ranked recommendation and the next 3 actions.

## Added Evaluation Dimensions

Also consider these dimensions when relevant:

- **資料品質**: source reliability, missing data, measurement precision, reproducibility, sample bias, and whether the data can support the claim.
- **變因可操作性**: whether the student can intentionally vary one factor while holding others stable.
- **時間與成本**: whether the project can fit the available weeks, budget, equipment, and classroom/home constraints.
- **評審溝通力**: whether the project can be explained clearly through a story, model, graph, prototype, or visual evidence.
- **地方性與生活連結**: whether the topic connects to local environment, school life, community needs, or student experience.
- **失敗後可學習性**: whether imperfect results still produce interpretable evidence and a meaningful discussion.

## Output Style

Write in Traditional Chinese unless the user requests another language. Be direct, evidence-based, and constructive. Avoid promising awards. Use tables when comparing multiple topic options, variables, risks, or materials.

When recommending topics, prefer projects that are:

- experimentally testable rather than only descriptive
- measurable with accessible tools
- safe and ethical for elementary students
- not just a demonstration of a known principle
- open to iteration, control groups, and evidence-based improvement

## Scoring

When helpful, provide a 1-5 score for these categories:

- 可研究性
- 創新性
- 國小可行性
- 資料可量測性
- 安全與倫理
- 成本與設備可及性
- 科展競爭力

Explain low scores with specific fixes. Do not hide uncertainty; label assumptions and missing information.

## References

Read `references/evaluation-framework.md` when the user asks for a complete evaluation, topic recommendation, scoring, or project upgrade plan. Use it as the detailed rubric and output checklist.

Read `references/prework-report-template.md` when the user asks to run the whole flow, produce a complete report, create a prework document, or generate material similar to a science fair preparation report.
