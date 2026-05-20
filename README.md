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

## 🛣️ 雙軌執行路徑：免安裝 vs. 整合型 Skill

為滿足不同使用者的習慣，InfoGold 提供兩種最輕量化的使用方式：

### 🔹 模式 A：給 Coding Agent 的安裝型憲法 (`skill.md`)
* **適用對象**：習慣使用終端機 CLI 工具（如 Claude Code, Gemini CLI）或 AI 編輯器（如 Cursor, Windsurf）的技術人員。
* **運作方式**：Agent 讀取 `skill.md` 後，會在背景全自動跑完四階段，並直接在您的目錄中生成結構化的報告檔案。
* **如何執行**：
  在對話框中提及 `skill.md` 與您的譯文檔案：
  > `"請閱讀 @skill.md，並協助整理 @my_transcript.txt"`

### 🔹 模式 B：給網頁版 LLM 的免安裝複製範本 (`RefineryPrompt.md`)
* **適用對象**：偏好使用網頁版對話介面（如 Claude.ai、ChatGPT Web、Gemini 網頁版）、不想安裝任何環境的商務使用者。
* **運作方式**：打開 [`RefineryPrompt.md`](file:///D:/MyProject/InfoGold/RefineryPrompt.md)，複製其內部的全部 Prompt，貼入對話框並於下方貼上您的逐字稿譯文。
* **如何執行**：
  直接在對話視窗貼上並送出，AI 將一氣呵成在對話框中印出所有清理好的內容與戰略報告。

---

## 📁 專案檔案架構 (Repository Structure)

```text
InfoGold/
├── skill.md               # 模式 A：專門給 Coding Agent 讀取的安裝型憲法
├── RefineryPrompt.md      # 模式 B：專門給網頁版 LLM 複製貼上的免安裝 Prompt 範本
├── Draft.md               # 原始專案實作規格書 (藍圖)
├── asr_input_example.txt  # 內建的「資料庫事故檢討會」原始譯文範例
├── README.md              # 本說明文件 (中文為主，英文為輔)
└── output/                # 執行後自動生成的精煉產出
    ├── 01_raw_aligned.md  # 階段 1：經清理、修正錯字並標記講者職稱的乾淨逐字稿 (臺灣繁中)
    ├── 02_structured.md   # 階段 2：高易讀性的摘要、會議議題矩陣與妥協歷程 (雙語對照)
    └── 03_strategy.md     # 階段 3：智慧自適應的戰略分析報告與 30-60-90 天落地路徑 (雙語對照)
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

## 🚀 Usage Modes

### Path A: Operational Constitution (`skill.md`)
* *Target Users*: Developers using CLI Agents (Claude Code, Gemini CLI) or Editor Chats (Cursor, Windsurf).
* *Command*: `@skill.md Please process @my_transcript.txt`
* *Result*: Automatically creates and saves output files in `output/` directory.

### Path B: Copy-Paste Prompt (`RefineryPrompt.md`)
* *Target Users*: Business users utilizing Web UIs (Claude Web, ChatGPT).
* *Usage*: Copy all content inside `RefineryPrompt.md`, paste into chat window, append your ASR transcript, and send.
* *Result*: Formatted reports are printed directly inside the chat panel for easy copying.

---

## 📄 License & Contribution
Feel free to fork this repository, submit issues, or pull requests. InfoGold is open-source and licensed under the MIT License.
