# Science Fair Evaluator

`science-fair-evaluator` 是一套專為臺灣國小科展設計的 AI Skill，協助教師與學生從題目萌芽、相似研究搜尋、科展可行性評估、研究演化、實驗設計、資料分析，到完整前置作業報告書的產出。

目前版本：`1.1.0`

> 核心研究鏈：**真實問題 → 科學機制 → 可量測方法 → 實驗或原型 → 數據分析 → 真實情境驗證**

這個 Skill 不只回答「這個題目能不能做」，更重要的是辨識普通、重複、過度廣泛、難以量測、科技裝飾化或不適合國小學生操作的方向，並將它們轉化為具有探究性、學生主體性、可重複量測與可辯護創新的科展研究。

---

## 適用對象

- 臺灣國小自然科教師
- 國小中、高年級科展學生
- 科展社團、營隊或研究指導教師
- 想把生活觀察轉換成研究題目的使用者
- 需要檢查題目重複性、研究深度與競爭力的指導者
- 希望結合 Arduino、ESP32、感測器、Python、AI、電腦視覺或 IoT 的研究團隊

---

## 可以輸入什麼

Skill 可以從下列素材開始工作：

- 一句模糊的題目或學生想法
- 生活中的觀察或問題
- 新聞、文章、網站、論文或 PDF
- YouTube 影片、影片逐字稿或課堂示範
- 照片、圖表、實驗記錄或觀察日誌
- CSV、試算表或既有實驗數據
- 歷屆科展作品
- 感測器紀錄、Arduino 或 ESP32 資料
- 教師提供的材料、設備或限制條件

若素材涉及最新研究、歷屆科展、產品規格、安全規範、競賽格式或近期技術，Skill 應先使用可靠來源查證，不可只依賴模型記憶。

---

## 主要功能

### 1. 題材轉換

從輸入素材辨識：

- 可觀察現象
- 真實問題
- 可能科學機制
- 可操縱變因
- 可量測結果
- 對照條件
- 學生可執行部分
- 可能的研究價值

### 2. 相似研究與重複性搜尋

正式決定題目前，優先搜尋：

- 臺灣全國與地方歷屆科展作品
- 國外學生科展與教學實驗
- 學術論文與技術文獻
- 大學、研究機構與官方科學資源
- 安全資料與產品規格

並比較：

- 前人已做過哪些變因
- 使用哪些量測方法
- 與候選題目重疊程度
- 還有哪些研究缺口
- 能否形成國小可操作的新角度

### 3. Stage Gates 硬性關卡

候選題目必須依序通過：

1. 安全與倫理
2. 可檢驗性
3. 學生主體性
4. 資源與時程
5. 資料品質
6. 新穎性
7. 可完成性

高分不能抵銷硬性關卡失敗。例如：不安全、無法量測或主要工作都由成人完成的題目，即使名稱新潮也不能被推薦。

### 4. 多面向評分

完整評估可涵蓋：

- 真實問題價值
- 科學機制清楚度
- 可研究性
- 新穎性
- 國小適切性
- 學生主體性
- 資料可量測性
- 控制與重複性
- 安全與倫理
- 成本及設備可及性
- 原型與迭代潛力
- 真實情境驗證
- 科展展示與競爭力

分數只作為比較工具，必須搭配具體理由、限制與改進方法。

### 5. Research Evolution Engine

將普通題目逐步演化：

- 現象描述 → 科學機制
- 主觀感覺 → 定量測量
- 單次展示 → 控制與重複試驗
- 「哪一個最好」→「在什麼條件下、為什麼」
- 既有題型 → 在地情境與新研究缺口
- 單一比較 → 多階段研究架構
- 完成實驗 → 依據數據改良原型
- 室內結果 → 真實情境驗證
- 科技裝飾 → 提升證據品質的技術工具

### 6. 完整研究設計

可產出：

- 正式研究題名
- 核心研究問題
- 研究假設
- 研究目的
- 研究架構
- 實驗分組
- 操縱、應變與控制變因
- 對照組與實驗組
- 樣本數與重複次數
- 校正與試做
- 詳細操作步驟
- 空白實驗紀錄表
- 建議圖表
- 誤差控制
- 資料排除規則
- 安全注意事項

實驗數量以科學必要性為原則，通常每個研究目的安排 1～3 個實驗，不為了格式硬湊重複或無意義的子實驗。

### 7. 資料分析規劃

可建議：

- 平均值、中位數、全距與標準差
- 百分比、恢復率、效率與標準化公式
- 長條圖、折線圖、散布圖、箱形圖與熱區圖
- 變因間相關分析
- 原始資料保存規則
- 異常值與資料排除規則
- 不確定性與限制
- 支持或削弱假設的判讀條件

### 8. 前置作業報告書

完整模式可產出接近臺灣科展作品書風格的前置作業，包含：

1. 封面資訊
2. 摘要
3. 參考題目與相似研究比較
4. 研究背景與動機
5. 研究目的
6. 研究架構
7. 材料設備
8. 研究過程與方法
9. 實驗紀錄表
10. 資料分析計畫
11. 材料與設備取得方式
12. 安全、倫理與風險控管
13. 預期結果與討論方向
14. 可行性與時程
15. 失敗模式與備案
16. 科展亮點與加強方向
17. APA 7 參考文獻
18. 下一步行動

### 9. 品質驗證

完成後檢查完整對應鏈：

```text
題目
→ 研究問題
→ 研究目的
→ 實驗
→ 應變變因
→ 測量方法
→ 紀錄表
→ 圖表
→ 判讀
```

任何一環缺漏，都必須補強或清楚標示限制。

---

## 四種工作模式

### Rapid Triage｜快速初評

適合只想先知道題目是否值得發展。

輸出通常包括：

- 適合／條件式適合／不適合
- 主要理由
- 最大風險
- 最有潛力的改造方向
- 建議下一步

範例：

```text
請用 science-fair-evaluator 快速評估「不同濾材的過濾效果」。
```

### Full Evaluation｜完整評估

適合題目決定前的完整檢查。

輸出包括：

- 相似研究搜尋
- 重複性判斷
- 候選題目
- Stage Gates
- 多面向評分
- 最佳題目推薦
- 研究缺口
- 強化方向

範例：

```text
請完整評估「咖啡渣混凝土」，先查找國內外研究與歷屆科展，再推薦一個最值得發展的國小題目。
```

### Complete Prework Report｜完整前置作業

適合題目已確定，希望建立可直接執行的研究計畫。

範例：

```text
請使用 science-fair-evaluator，針對「局部陰影的形狀與位置對太陽能板陣列輸出的影響」產出完整科展前置作業報告書。
```

### Research Evolution｜研究演化

適合普通、重複、描述性或只有科技名詞的題目。

範例：

```text
請使用 Research Evolution Engine，把「不同水質對植物生長的影響」升級為具有機制、量測、資料分析、原型或情境驗證的國小科展題目。
```

---

## AI、Arduino 與 IoT 的使用原則

本 Skill 不把「加入 AI、Arduino 或 ESP32」直接視為創新。這些技術只有在下列情況才建議加入：

- 提升測量精度
- 降低人為判讀偏差
- 自動記錄長期資料
- 同步量測多項環境變因
- 進行影像分析或物件追蹤
- 產生熱區圖與趨勢模型
- 支援真實情境監測

不建議只為了題目看起來新潮而加入感測器、App、AI 模型或物聯網平台。

---

## 安裝方式

### Codex：使用 Git 安裝

Windows PowerShell：

```powershell
New-Item -ItemType Directory -Force "$HOME\.codex\skills" | Out-Null
git clone https://github.com/prayer168/science-fair-evaluator.git "$HOME\.codex\skills\science-fair-evaluator"
```

macOS / Linux：

```bash
mkdir -p ~/.codex/skills
git clone https://github.com/prayer168/science-fair-evaluator.git ~/.codex/skills/science-fair-evaluator
```

重新啟動 Codex 後即可使用。

### 已安裝版本更新

Windows PowerShell：

```powershell
Set-Location "$HOME\.codex\skills\science-fair-evaluator"
git pull origin main
```

macOS / Linux：

```bash
cd ~/.codex/skills/science-fair-evaluator
git pull origin main
```

### 手動安裝

1. 下載 GitHub Repository ZIP。
2. 解壓縮。
3. 將整個資料夾命名為 `science-fair-evaluator`。
4. 放入：

```text
C:\Users\<使用者名稱>\.codex\skills\science-fair-evaluator
```

5. 確認資料夾根目錄包含 `SKILL.md`。
6. 重新啟動 Codex。

---

## 呼叫方式

Codex 通常可依 description 自動觸發，也可明確指定：

```text
請使用 science-fair-evaluator 評估這個題目。
```

或使用本地 Skill 路徑：

```text
[$science-fair-evaluator](C:\Users\<使用者名稱>\.codex\skills\science-fair-evaluator\SKILL.md) 鎂棒保護鐵釘
```

---

## 推薦提示詞

### 題目初評

```text
請使用 science-fair-evaluator 評估以下題目是否適合臺灣國小中高年級科展。請檢查安全性、可量測性、重複性、學生主體性、成本與競爭力，並提出一個最佳改造方向：

題目：＿＿＿＿＿＿
```

### 完整研究搜尋

```text
請使用 science-fair-evaluator 對以下題材進行完整評估。先搜尋臺灣歷屆科展、國外學生研究、學術文獻與官方資料，再比較前人做過的變因、方法與研究缺口。最後只推薦一個最佳題目：

題材：＿＿＿＿＿＿
```

### 完整前置作業

```text
請使用 science-fair-evaluator 的 Complete Prework Report 模式，針對以下題目產出完整前置作業。內容包含文獻回顧、研究動機、研究目的、研究架構、每個實驗的詳細步驟、空白紀錄表、材料設備、預算、時程、安全風險、資料分析、失敗備案與 APA 7 參考文獻：

題目：＿＿＿＿＿＿
```

### 研究演化

```text
請使用 Research Evolution Engine，把以下普通題目依序升級：真實問題、科學機制、可量測方法、控制實驗、資料分析、原型迭代與真實情境驗證。不要只加入 AI 或 Arduino 作為裝飾：

原始題目：＿＿＿＿＿＿
```

---

## 檔案結構

```text
science-fair-evaluator/
├── README.md
├── SKILL.md
├── VERSION
├── version.md
├── CHANGELOG.md
├── agents/
│   └── openai.yaml
└── references/
    ├── evaluation-framework.md
    ├── prework-report-template.md
    ├── quality-validation-checklist.md
    └── research-evolution-engine.md
```

### 檔案用途

- `SKILL.md`：主要觸發條件、行為規則與完整執行流程。
- `README.md`：技能包功能、安裝、使用方式與範例。
- `VERSION`：供程式或腳本讀取的單行版本號。
- `version.md`：人類可閱讀的完整版本演進紀錄。
- `CHANGELOG.md`：精簡發布紀錄。
- `references/evaluation-framework.md`：評分、Stage Gates 與題目選擇規準。
- `references/research-evolution-engine.md`：研究演化與題目升級方法。
- `references/prework-report-template.md`：完整前置作業報告模板。
- `references/quality-validation-checklist.md`：完稿前一致性與品質檢查。
- `agents/openai.yaml`：Skill 顯示與代理設定。

---

## 版本管理

版本遵循語意化版本概念：

- `MAJOR`：核心架構或使用方式重大改變
- `MINOR`：新增功能且維持相容
- `PATCH`：修正錯誤、文字或小幅改善

目前版本以 `VERSION`、`SKILL.md` metadata、`README.md`、`CHANGELOG.md` 與 `version.md` 為一致性來源。每次發布時應同步更新。

---

## 設計原則

- 小而嚴謹，比大而模糊更適合國小科展。
- 真實探究比華麗科技名詞重要。
- 不把已知現象展示誤當成研究。
- 不把不同品牌或材料排名直接視為高品質科展。
- 不捏造文獻、研究結果、測量精度或獲獎保證。
- 明確區分已查證事實、合理推論、研究假設與預期結果。
- 每個研究目的都必須有對應實驗與量測方法。
- 每個應變變因都必須能在紀錄表中被收集。
- 每項安全風險都必須有控制、替代或停止條件。
- 學生必須能親自提出問題、操作、記錄、分析及解釋。

---

## 授權與貢獻

此 Repository 可持續擴充新的評估規準、研究模板與範例。提交修改前，請確認：

- 版本號已同步
- `SKILL.md` 與 references 沒有互相矛盾
- 沒有強制產生不必要的實驗
- 沒有弱化安全與倫理關卡
- 沒有把科技工具誤當成研究創新
- 完成題目到判讀的一致性檢核
