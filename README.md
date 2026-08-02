# Science Fair Evaluator

`science-fair-evaluator` 是一套給 Codex 使用的國小科展評估、研究演化與前置作業報告 Skill。

目前版本：`1.0.0`

## 核心研究鏈

> 真實問題 → 科學機制 → 可量測方法 → 實驗或原型 → 數據分析 → 真實情境驗證

它不只判斷題目「能不能做」，還會把普通、重複、太廣或難以量測的想法，重新設計成適合國小學生操作、具有學生主體性、可以取得可信數據的研究。

## 主要功能

- 從題目、文章、影片、圖片、表格、資料集與生活觀察中找出研究種子
- 搜尋並比較國內外相似研究與歷屆科展作品
- 評估安全性、科學性、新穎性、可量測性、成本與科展競爭力
- 使用硬性關卡排除不安全、不可測量或缺乏學生主體性的方向
- 執行 Research Evolution Engine，將普通題目升級
- 建立題目、研究問題、目的、實驗、測量、紀錄表與分析的完整對應鏈
- 規劃材料、預算、時程、風險、備案與真實情境驗證
- 產出國小科學展覽前置作業報告書
- 使用 APA 7 整理參考文獻
- 完稿後執行一致性與品質檢核

## 四種模式

1. **Rapid Triage**：快速判斷適合、條件式適合或不適合。
2. **Full Evaluation**：完整科展評估、搜尋、比較、評分與題目推薦。
3. **Complete Prework Report**：產出文獻、動機、目的、實驗、紀錄表、材料、預算、時程與參考文獻。
4. **Research Evolution**：將重複、描述性或科技裝飾型題目演化為真正可研究的方向。

## Stage Gates

候選題目必須依序通過：

- 安全與倫理
- 可檢驗性
- 學生主體性
- 資源與時程
- 資料品質
- 新穎性
- 可完成性

高總分不能抵銷安全、可檢驗性或學生主體性的失敗。

## Research Evolution Engine

研究演化可從以下方向進行：

- 現象轉向機制
- 主觀觀察轉向量化測量
- 單次比較轉向控制與重複試驗
- 「哪個最好」轉向「在什麼條件下、為什麼」
- 已知實驗轉向在地情境驗證
- 實驗轉向證據驅動的原型迭代
- 單一結果轉向模型預測與外部驗證
- 合理導入 Arduino、ESP32、感測器、Python、電腦視覺、AI 或 IoT

科技必須提升測量、降低偏差或支援長期監測，不能只是裝飾。

## 檔案結構

```text
science-fair-evaluator/
├── CHANGELOG.md
├── README.md
├── SKILL.md
├── VERSION
├── agents/
│   └── openai.yaml
└── references/
    ├── evaluation-framework.md
    ├── prework-report-template.md
    ├── quality-validation-checklist.md
    └── research-evolution-engine.md
```

## 安裝

將整個資料夾放入 Codex skills 目錄：

```text
C:\Users\<your-name>\.codex\skills\science-fair-evaluator
```

或使用 Git：

```bash
git clone https://github.com/prayer168/science-fair-evaluator.git ~/.codex/skills/science-fair-evaluator
```

重新啟動 Codex 後即可使用。

## 呼叫範例

```text
請用 science-fair-evaluator 評估「局部陰影對太陽能板陣列輸出的影響」，先查找相似研究，再推薦最佳題目並產出完整前置作業。
```

```text
請使用 Research Evolution Engine，把「不同濾材的過濾效果」升級成具機制、量測、原型與情境驗證的國小科展題目。
```

## 設計原則

- 小而嚴謹，比大而模糊更適合國小科展。
- 不把科學示範誤當成科學探究。
- 不捏造文獻、結果、精確度或得獎保證。
- 一個好題目必須能回答：改變了什麼、量到了什麼、如何公平比較、結果如何解釋，以及真實情境是否成立。
