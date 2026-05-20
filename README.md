# InfoGold - 智慧型會議錄音與逐字稿戰略精煉引擎 🌟
### *Transform Raw ASR Noise into Actionable Executive Intelligence*
#### [繁體中文 (Taiwan Localized) 🇹🇼 | [English Version 🇺🇸](#english-documentation)]

---

**InfoGold** 是一個智慧化的單檔驅動專案基礎架構，旨在解決企業在「語音轉文字（ASR）整理」上的核心痛點。不論是口語雜亂、錯別字、音訊模糊還是多人對話混亂，InfoGold 能將原始譯文自動提煉為**高品質會議紀錄**，並動態適應會議本質，產出具備**行動價值與決策深度的戰略報告**。

此專案已針對 **本地開源模型 (Local LLMs)** 進行深度最佳化，同時完美支援雲端 Coding Agents，為您提供安全、零幻覺、符合臺灣商務語境的精煉解決方案。

---

## 🎯 核心價值與優勢 (Key Value Proposition)

* **🇹🇼 臺灣在地化對齊**：全自動修正簡體字、簡體術語及大陸用詞（自動過濾「項目、優化、數據」等，對齊為「專案、最佳化、資料」）。
* **🧠 智能適應分析 (Dynamic Routing)**：AI 會在讀取內容時，自動判斷會議性質，並動態載入最適合的分析框架（如戰略規劃套用 SWOT/TOWS，技術故障套用 5 Whys/RACI），拒絕死板分析。
* **🛡️ 安全指令隔離 (Sandboxing)**：採用 `<ASR_LITERAL_DATA>` 沙箱機制，確保譯文內包含的任何語音命令或惡意注入代碼皆不會被執行。
* **🔍 零幻覺實證原則**：所有戰略報告與行動方針的論點，皆強制附帶乾淨逐字稿的**行號引用**（例如 `[Ref: Line 42]`），保證字字有依據。

---

## 🛣️ 三軌執行路徑 (Three Execution Paths)

InfoGold 提供以下三種靈活的調用方式，您可以根據您的工作流程自由選擇：

### 🔹 路徑 A：安裝為系統級自訂指令 (Installed Agent Skill)
如果您使用的是支援「自訂指令（Custom Instructions）」或「全域配置」的 Coding Agent（例如 Claude Code 的全域設定，或是自訂的本地 CLI Alias），您可以直接將 [`InfoGold.md`](file:///D:/MyProject/InfoGold/InfoGold.md) 的內容貼入您的 Agent 全域系統提示詞中，將其安裝為全域 Skill。
* **呼叫方式**：直接用自訂指令呼叫，無需在專案中附帶 any md 規則檔。例如：
  > `infogold @my_transcript.txt`

### 🔹 路徑 B：專案級文件調用 (Workspace Document-Based Constitution)
如果您不想安裝全域設定，只希望在特定專案資料夾內以文件引導 Agent 執行。
* **使用方式**：將 [`InfoGold.md`](file:///D:/MyProject/InfoGold/InfoGold.md) 放入您的專案資料夾，並在 CLI 終端機或 AI 編輯器（如 Cursor、Windsurf）對話框中輸入：
  > `"請閱讀 @InfoGold.md，然後協助整理 @my_transcript.txt"`

### 🔹 路徑 C：網頁版免安裝貼入 (Web Copy-Paste Prompt Template)
如果您使用的是沒有讀寫檔案功能、純網頁版的 Chat UI（如 Claude.ai、ChatGPT、Gemini 網頁版）。
* **使用方式**：打開 [`RefineryPrompt.md`](file:///D:/MyProject/InfoGold/RefineryPrompt.md)，複製其內部的全部 Prompt，貼入對話框並於下方附上您的 ASR 譯文。AI 將直接在對話框中印出所有清理好的內容與戰略報告。

---

## 📁 專案檔案架構 (Repository Structure)

```text
InfoGold/
├── InfoGold.md             # 路徑 B：專案級文件調用的執行憲法
├── RefineryPrompt.md       # 路徑 C：網頁版 LLM 複製貼上的免安裝 Prompt 範本
├── Draft.md                # 原始專案實作規格書 (藍圖)
├── asr_input_example.txt   # 內建的「資料庫事故檢討會」原始譯文範例
├── README.md               # 本說明文件 (中文為主，英文為輔)
└── output/                 # 執行後自動生成的精煉產出
    ├── 01_raw_aligned.md   # 階段 1：乾淨對齊的逐字稿 (臺灣繁中)
    ├── 02_structured.md    # 階段 2：結構化會議重點摘要與議題行動表格 (雙語對照)
    └── 03_strategy.md      # 階段 3：自適應選擇的戰略分析報告與 90 天落地路徑 (雙語對照)
```

---

## ⚡ 智慧分類路由表 (Intelligent Dynamic Selector)

AI 將在讀取譯文後自動路由至最適合的框架：

| 會議分類 | 本質特徵 | 選用戰略分析框架 |
| :--- | :--- | :--- |
| **戰略規劃 / 商業決策** | 高階發展規劃、市場定位、合作談判 | **SWOT 分析 + TOWS 戰略交叉矩陣** |
| **產品設計 / 用戶調研** | 功能需求、體驗反饋、腦力激盪 | **JTBD (Jobs-to-be-Done) + 價值主張畫布** |
| **技術架構 / 故障檢討** | 系統當機、程式缺陷、架構擴充 | **5 Whys 根因分析 + RACI 責任分配矩陣** |
| **銷售對話 / 客戶反饋** | 價格協商、客戶訴求、商務提案 | **Pain & Gain 痛點與期望效益分析** |
| **日常營運 / 專案同步** | 團隊週會、進度對齊、任務跟進 | **OKR 目標對齊 + 艾森豪優先權矩陣** |

---

<a name="english-documentation"></a>

# English Documentation 🇺🇸

**InfoGold** is a lightweight, single-file driven infrastructure designed to transform raw, noisy, and unstructured ASR (Audio-to-Text) transcripts into high-readability executive records and strategic roadmaps.

## 🌟 Key Benefits
* **Taiwanese Business Localization**: Automatically translates and maps terminology to standard Taiwan tech and business terms.
* **Dynamic Strategic Selector**: Auto-classifies the meeting type and routes to the most effective analysis framework (SWOT/TOWS, JTBD, 5 Whys, etc.).
* **Security & Sandboxing**: Isolates transcript strings in `<ASR_LITERAL_DATA>` blocks to prevent prompt injections.
* **Zero-Hallucination References**: Enforces strict line number citations (`[Ref: Line X]`) back to the clean transcript for all strategic points.

## 🚀 Execution Paths

### Path A: Installed Agent Skill
* *Target*: Register the rules globally in your Coding Agent's system configurations.
* *Command*: Call by your configured alias name directly: `infogold @my_transcript.txt`

### Path B: Workspace Document-Based Constitution (`InfoGold.md`)
* *Target*: Keep the constitution file locally in the workspace folder.
* *Command*: `"Please read @InfoGold.md, then help organize @my_transcript.txt"`

### Path C: Copy-Paste Prompt Template (`RefineryPrompt.md`)
* *Target*: Copy prompt text into standard Web UIs (Claude Web, ChatGPT Web) along with your transcript.
