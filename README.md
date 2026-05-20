# InfoGold - 知識資產生成與提取框架 (Knowledge Asset Generation & Extraction Framework)
#### [繁體中文 | [English](#english-version)]

本專案定義了一套系統化的 **知識資產生成與提取框架 (KAGEF)**。透過結構化的提示詞規範與自動化隔離目錄，協助使用者利用 AI 助理（如 Claude Code, Gemini, Pi 或網頁版 ChatGPT/Claude）將雜亂的會議逐字稿、閱讀筆記、工作手稿、企劃草案或文章，**一氣跨越轉化為具備「可複利價值」與「行動策略」的知識資產套件**。

---

## 🎯 框架三支柱 (Framework Pillars)
本專案的底層設計不僅是文字整理，更是將暫時性的談話與碎片化經歷，固化為團隊長期能力的閉環系統：

1. **第一支柱：經歷固化 (Ephemeral-to-Durable)** ➔ 生成 `01_cleaned_text.md`
   * **目標**：完整精煉原始語料。
   * **實踐**：自動清理贅字、語氣詞與排版錯亂。若是會議對話則還原流暢對齊的逐字稿；若是隨筆手稿則梳理邏輯語序。在此階段**忠實保留原始術語**，保留話語權與原意。

2. **第二支柱：結構對齊 (Structural Logic Alignment)** ➔ 生成 `02_structured_summary.md`
   * **目標**：萃取核心結論與待辦清單，套用臺灣在地化專業語彙。
   * **實踐**：提煉核心結論、議題邏輯矩陣，並透過**費曼技巧**解構對話/草稿中的「思維斷層」與潛在共識，並將隨機好點子轉化為具備負責人與期限的標準待辦事項。

3. **第三支柱：決策增值 (Adaptive Strategic Compound)** ➔ 生成 `03_strategy_roadmap.md`
   * **目標**：進行深度策略分析，並給予 90 天的可行動步驟。
   * **實踐**：AI 自適應評估文本主題，複合使用分析框架（SWOT/TOWS、JTBD、5 Whys 根因分析、OKR、痛點分析等）。報告中的每點結論**強迫引用原始文本引註標記**（例如 `[Ref: Line X]`）確保字字有據，並產出清晰的 30-60-90 天 SOP 落地路徑。

---

## 🧠 自適應複合分析模組
AI 讀取文本後，會根據主題智慧拼裝並複合使用以下分析工具，以提煉出具備行動價值的建議，並於報告開頭說明框架選用理由：
* **SWOT 分析 + TOWS 矩陣**：適用於政策發展規劃、資源盤點或重大發展策略。
* **JTBD (Jobs-to-be-Done) + 價值主張**：適用於公共服務設計、宣導方案、便民措施改進與使用者期待分析。
* **5 Whys 根因分析 + RACI 責任分配**：適用於流程失誤、專案延宕檢討、跨部門協調障礙與權責釐清。
* **Pain & Gain 痛點分析**：適用於民意反饋彙整、意見公聽會整理與陳情需求分析。
* **OKR 目標對齊 + 艾森豪優先權矩陣**：適用於定期工作會報同步、進度追蹤與團隊排程分工。

*特別要求：報告中的每一項戰略分析結論，皆會自動標註原始文本的**行號或段落引用**（例如 `[Ref: Line 42]` 或 `[Ref: 段落 2]`），確保字字有據，便於呈報與查證。*

---

## 💡 核心價值提煉與「資產化」哲學
為了讓使用者能從任何文本與經歷中徹底「榨取」價值，本框架實踐以下核心法則：
* **輸入-轉化-輸出閉環**：不作被動的接收者，把每一件事當作生產素材，積極轉為系統化、可複利的決策文獻。
* **偶然成功 SOP 化**：捕捉靈感，拆解為可重複執行的標準步驟，將一次性幸運固化為組織長期能力資產。
* **第一性原理與反向思考**：直指核心問題本質，並預測「若該規畫徹底失敗會是什麼原因」，透過防禦策略強化執行價值。
* **極致利他與共享**：提供高易讀性的共享決策套件（自動在子目錄下生成導覽門戶 `README.md`），提供各檔案的精華亮點摘要與索引連結，方便直接呈報分享。

---

## 🚀 使用方法

根據您的辦公環境，選擇以下任一方式使用：

### 方式一：網頁複製貼上（免安裝，最簡單）
適用於使用 ChatGPT、Claude.ai、Gemini 等網頁版對話介面的使用者。
1. 開啟本專案的 [`InfoGold.md`](file:///D:/MyProject/InfoGold/InfoGold.md)。
2. 複製該檔案內的**所有內容**，直接貼入 AI 網頁對話框中。
3. 在最下方附上您的原始文本，送出即可。

### 方式二：本地文件調用
適用於使用可在本機讀寫檔案的 AI 助理（如 Claude Code, Gemini CLI, Pi 等）。
1. 將本專案複製/下載至您的電腦。
2. 將您的原始文本檔（如 `.txt` 檔）放入 `test/` 資料夾中。
3. 對您的 AI 助理輸入最簡指令：
```text
請閱讀 @InfoGold.md
```
*(AI 將會自動偵測並讀取 `test/` 資料夾下的文字檔，無需每次手動輸入長檔名)*
4. AI 將自動在 `output/` 目錄下建立以「執行日期_文本主題」命名的專屬資料夾（例如 `output/20260520_施主任討論意見/`），並產出三份精煉報告，確保多次使用時不會互相覆蓋。

### 方式三：安裝為全域指令
如果您經常需要使用此功能，可以將 [`InfoGold.md`](file:///D:/MyProject/InfoGold/InfoGold.md) 中的規則內容複製，貼入您的 AI 助理全域自訂指令中，即可隨時在命令列直接呼叫：
```bash
infogold
```
*(預設會直接讀取當前工作目錄下 `test/` 資料夾中的原始文本，不需傳入檔案參數)*

---

## 📁 檔案結構

```text
InfoGold/
├── InfoGold.md             # 核心規則檔 (同時支援本地端讀寫與網頁端複製貼上)
├── Draft.md                # 原始專案實作規格書 (藍圖)
├── test/                   # 多元原始文本存放資料夾 (內含範例檔，已設定隱私安全 gitignore)
│   ├── .gitkeep            # 資料夾說明檔
│   └── 5月18日與施主任討論意見.txt  # 內建的跨部門研究會議原始對話範例
├── README.md               # 本說明文件
└── output/                 # 執行後自動產出的決策套件 (已設定隱私安全 gitignore)
    ├── .gitkeep            # 資料夾說明檔
    └── YYYYMMDD_[主題]/    # 每次執行產生的獨立決策支援套件資料夾
        ├── README.md       # [導覽門戶] 各份報告的核心亮點摘要與連結
        ├── metadata.json   # 本次執行日誌與狀態中繼資料
        ├── 01_cleaned_text.md  # [產出一] 精煉清理且保留原文語彙的完整文本
        ├── 02_structured_summary.md # [產出二] 結構化重點與行動矩陣 (臺灣在地化)
        └── 03_strategy_roadmap.md # [產出三] 自適應分析與 30-60-90 天落地路徑 (臺灣在地化)
```

---

<a name="english-version"></a>

# English Version

This project provides a structured prompt framework to help users organize raw ASR transcripts into a systematic decision-support package using AI assistants.

## 🎯 Goal
Transform raw transcript text into three structured deliverables in one shot:
1. **Clean Verbatim Transcript**: Corrects terms, cleans filler words, and aligns speakers.
2. **Structured Summary & Takeaways**: Captures agendas, debates, compromise points, and action tables.
3. **Actionable Strategic Analysis**: Evaluates raw inputs via standard business/public-sector frameworks (SWOT, 5 Whys, etc.) and provides a concrete **30-60-90 day roadmap** outlining the next steps.

## 🚀 How to Use

### Mode 1: Web UI (Copy-Paste)
1. Open [`InfoGold.md`](file:///D:/MyProject/InfoGold/InfoGold.md), copy all of its content, and paste it into ChatGPT/Claude Web.
2. Paste your raw transcript at the bottom and submit.

### Mode 2: Local AI CLI
1. Put your raw text/transcript file inside the `test/` folder.
2. Run the following command in your terminal:
```text
Please read @InfoGold.md
```
*(The AI will automatically locate the input text in the `test/` folder and generate output files inside a unique `output/YYYYMMDD_[Topic]/` folder to prevent overwriting previous runs)*

### Mode 3: Global Custom Command
Save the rules from `InfoGold.md` globally in your assistant's settings and run:
```bash
infogold
```
