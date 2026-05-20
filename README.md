# InfoGold - 智慧型會議錄音與逐字稿戰略精煉引擎 🌟
### *將雜亂的錄音逐字稿，轉化為高價值的施政與決策產出*
#### [繁體中文 (Taiwan Localized) 🇹🇼 | [English Version 🇺🇸](#english-documentation)]

---

**InfoGold** 是一個輕量化的單檔驅動智慧架構，專為政府機關、企劃部門、行政主管與決策人員設計。不論是口語雜亂、字詞錯漏、音訊模糊或多人發言混亂的原始逐字稿（ASR 譯文），InfoGold 都能協助 **智慧 AI 助理** 自動將其精煉為**高品質會議紀錄**，並自適應會議內容，產出具備**行動價值與決策深度的戰略報告**。

本專案無需任何程式開發背景，專為一般行政辦公與智慧助理協作進行最佳化，支援本地端安全運行（保障公務機密隱私）或雲端 AI 助理。

---

## 🎯 核心價值與優勢 (Core Benefits)

* **🇹🇼 臺灣在地化商務與公務用語**：全自動修正簡體字與簡體術語（自動過濾「項目、優化、數據」等，對齊為「專案、最佳化、資料」，完美符合公務文書規範）。
* **🧠 自適應複合分析 (Smart Adaptive Hybrid Analysis)**：AI 會智慧評估會議的複雜度，自動裝配最適合的決策框架（例如：政策規劃套用 SWOT/TOWS，業務流程檢討套用 5 Whys/RACI，日常會報套用 OKR），拒絕死板格式。
* **🛡️ 機密與安全防禦**：設有專用的 `<ASR_LITERAL_DATA>` 沙箱保護，避免譯文中的口語內容誤觸 AI 的指令執行，確保安全。
* **🔍 零幻想實證原則**：報告中的每一項結論與建議，皆會自動標註逐字稿的**行號引用**（例如 `[Ref: Line 42]`），公務呈報時字字有依據，禁得起檢驗。

---

## 🛣️ 三種調用路徑 (Three Easy Ways to Use)

InfoGold 不需要您安裝任何程式，請根據您的日常辦公環境選擇以下最簡單的方式：

### 🔹 路徑 A：安裝為 AI 助理的全域指令 (Installed Agent Skill)
如果您使用的是安裝在電腦本機上的智慧 AI 助理（如 **Claude Code**, **Gemini CLI/Antigravity**, **Pi** 等），您可以直接將 [`InfoGold.md`](file:///D:/MyProject/InfoGold/InfoGold.md) 的規則內容貼入您助理的全域系統提示詞設定中。
* **呼叫方式**：直接在電腦命令列輸入自訂指令呼叫，AI 會直接讀檔並產出報告。例如：
  > `infogold @my_transcript.txt`

### 🔹 路徑 B：專案資料夾文件調用 (Workspace Document-Based Usage)
如果您希望在特定資料夾中，透過規則檔引導 AI 助理進行整理。
* **使用方式**：將 [`InfoGold.md`](file:///D:/MyProject/InfoGold/InfoGold.md) 規則檔與您的會議逐字稿放在同一個資料夾，並直接對您的 AI 助理說：
  > `"請閱讀 @InfoGold.md，然後協助整理 @my_transcript.txt"`
* **結果**：AI 助理會全自動在背景跑完四個階段，並直接在資料夾中生成精美的 Markdown 報告。

### 🔹 路徑 C：網頁版免安裝貼入 (Web Copy-Paste Prompt Template)
如果您使用的是一般瀏覽器網頁版 AI（如 Claude.ai、ChatGPT、Gemini 網頁版）。
* **使用方式**：打開 [`RefineryPrompt.md`](file:///D:/MyProject/InfoGold/RefineryPrompt.md)，**複製該檔案內的全部 Prompt 內容**並貼入對話框，隨後在最下方附上您的逐字稿。AI 將直接在網頁對話框中一次性印出所有清理好的內容與戰略報告，方便您複製使用。

---

## 📁 檔案架構說明 (Folder Layout)

```text
InfoGold/
├── InfoGold.md             # 路徑 B：放於資料夾中引導 AI 助理的精煉憲法
├── RefineryPrompt.md       # 路徑 C：專供網頁版 AI 複製貼上的 Prompt 範本
├── Draft.md                # 原始專案實作規格書 (藍圖)
├── asr_input_example.txt   # 內建的「跨部門協調會議」原始譯文範例
├── README.md               # 本說明文件 (中文為主，英文為輔)
└── output/                 # 執行後自動生成的精煉產出
    ├── 01_raw_aligned.md   # 階段 1：乾淨對齊的會議逐字稿 (臺灣繁中)
    ├── 02_structured.md    # 階段 2：結構化會議重點摘要與議題行動表格 (雙語對照)
    └── 03_strategy.md      # 階段 3：自適應選擇的戰略分析報告與 90 天落地路徑 (雙語對照)
```

---

## ⚡ 自適應分析工具箱 (Smart Adaptive Hybrid Selector)

AI 會自動評估您的會議性質，**彈性挑選並組合**以下最適合的公務/商務分析工具：

1. **SWOT 分析 + TOWS 矩陣**：適用於政策發展規劃、施政決策、跨機關商務談判。
2. **JTBD (Jobs-to-be-Done) + 價值主張畫布**：適用於公共服務設計、政策宣導方案、民眾需求梳理。
3. **5 Whys 根因分析 + RACI 責任分配**：適用於業務流程檢討、專案延宕改進、跨部門權責劃分。
4. **Pain & Gain 痛點與期望效益分析**：適用於民意反饋、陳情案件梳理、政策公聽會意見彙整。
5. **OKR 目標對齊 + 艾森豪矩陣**：適用於處務會議同步、年度施政計畫跟進、科室任務分工。

---

<a name="english-documentation"></a>

# English Documentation 🇺🇸

**InfoGold** is a lightweight, single-file driven intelligence framework designed for government administrative staff, project planners, and policy decision-makers. It transforms noisy, unstructured ASR (Audio-to-Text) conference transcripts into clean, professional records and strategic analysis reports.

## 🌟 Key Benefits
* **Taiwanese Business & Government Localization**: Automatically aligns terminology to standard Taiwan business and administrative phrases.
* **Smart Adaptive Hybrid Selector**: Dynamically selects and combines strategic frameworks (SWOT, 5 Whys, JTBD, OKRs, etc.) based on meeting complexity.
* **Security & Confidentiality**: Employs sandboxing tags (`<ASR_LITERAL_DATA>`) to prevent direct execution of transcript text.
* **Zero-Hallucination References**: Enforces strict line number citations (`[Ref: Line X]`) back to the clean transcript for all key decisions.

## 🚀 Execution Paths

### Path A: Installed AI Agent Skill
* *Target*: Configure globally within your local AI Agent (Claude Code, Gemini CLI, Pi).
* *Command*: Call directly: `infogold @my_transcript.txt`

### Path B: Workspace Document-Based Usage (`InfoGold.md`)
* *Target*: Keep the config file in your workspace folder.
* *Command*: `"Please read @InfoGold.md, then help organize @my_transcript.txt"`

### Path C: Copy-Paste Prompt Template (`RefineryPrompt.md`)
* *Target*: Copy the template from `RefineryPrompt.md`, paste into standard Web UIs (Claude Web, ChatGPT Web), and append your transcript.
