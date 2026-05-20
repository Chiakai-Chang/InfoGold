# InfoGold - 多元文本與經驗價值提煉工具 (會議逐字稿/閱讀筆記/工作手稿/文章)
#### [繁體中文 | [English](#english-version)]

本專案提供一套結構化的提示詞規範，協助使用者利用 AI 助理（如 Claude Code, Gemini, Pi 或網頁版 ChatGPT/Claude）將雜亂的會議逐字稿、閱讀筆記、工作手稿、企劃草案或文章，**系統化地一氣呵成產出一整套結構化決策套件**。不僅能還原乾淨流暢的精煉文本，更能進行深度策略分析，並提供具備可行動價值（Actionable Value）的下一步執行建議。

---

## 🎯 專案目標
原始錄音轉文字（ASR）或隨筆手稿常伴隨重複、錯別字與邏輯混亂，且通常缺乏脈絡整理與具體行動方針。本專案旨在提供系統化的精煉流程，將各類原始文本轉化為以下三份具備實行價值的結構化產出：
1. **精煉且乾淨的文本/發言紀錄**：自動清理語氣贅字、修正專有名詞錯字，若是手稿筆記則重新梳理邏輯語序與排版。
2. **結構化重點與邏輯矩陣**：條列核心結論、議題與邏輯矩陣、思維斷層/爭議與解決路徑，以及具體的待辦行動事項表。
3. **行動價值的戰略分析與執行路徑**：自適應套用商務/公務分析框架（如 SWOT、5 Whys、JTBD 等），並規劃出具體的 **30-60-90 天落地執行路徑（Roadmap）**，指出下一步該怎麼做。

---

## 🧠 整理原理與分析框架
AI 會在讀取文本後，智慧評估內容的複雜度與主題，**自動拼裝並複合使用**以下最適合的分析框架，以產出具備行動價值的決策建議，並於報告開頭說明框架選用理由：
* **SWOT 分析 + TOWS 矩陣**：適用於涉及政策發展規劃、資源盤點或重大發展策略。
* **JTBD (Jobs-to-be-Done) + 價值主張**：適用於探討公共服務設計、便民措施改進與使用者期待分析。
* **5 Whys 根因分析 + RACI 責任分配**：適用於專案延宕、流程簡化與缺失檢討、跨部門協調障礙與權責釐清。
* **Pain & Gain 痛點分析**：適用於民意反饋彙整、公聽會意見整理與陳情案件剖析。
* **OKR 目標對齊 + 艾森豪優先權矩陣**：適用於定期工作會報同步、進度追蹤與團隊排程分工。

*特別要求：報告中的每一項戰略分析結論，皆會自動標註原始文本的**行號或段落引用**（例如 `[Ref: Line 42]`），確保字字有據，便於呈報與查證。*

---

## 💡 InfoGold 的核心哲學：將經歷轉化為智慧與能力
本專案的底層設計不僅是文字排版，更是一套「榨取談話經驗價值」的閉環系統，實踐以下核心原則：
1. **輸入-轉化-輸出閉環**：將每一篇雜亂的逐字稿或隨筆手稿看作生產素材，系統性地轉化為理性邏輯決策文件。
2. **費曼解構 (補齊思維斷層)**：將複雜的爭執或草稿中的矛盾以最簡單的邏輯釐清，找出被忽略的思維斷層與潛在共識。
3. **偶然成功 SOP 化**：捕捉對話或文本中提及的成功案例或靈感，在 Roadmap 中拆解為可重複執行的步驟，將一次性的價值轉化為長期能力資產。
4. **第一性原理與反向思考**：剝離表面詞藻直指本質問題，並透過預測失敗（WT 戰略與權責劃分）來強化當前行動方案。
5. **極致利他與共享**：提供高易讀性的共享決策套件，協助團隊迅速掌握下一步，固化為團隊複利能力。

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
