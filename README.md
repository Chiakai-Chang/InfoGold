# InfoGold - 會議逐字稿系統化整理與行動分析工具
#### [繁體中文 | [English](#english-version)]

本專案提供一套結構化的提示詞規範，協助使用者利用 AI 助理（如 Claude Code, Gemini, Pi 或網頁版 ChatGPT/Claude）將雜亂的會議或談話錄音逐字稿，**系統化地一氣呵成產出一整套結構化決策套件**。不僅能還原乾淨的發言紀錄，更能進行深度策略分析，並提供具備可行動價值（Actionable Value）的下一步執行建議。

---

## 🎯 專案目標
原始錄音轉文字（ASR）常伴隨口語重複、錯別字與發言混亂，且通常缺乏脈絡整理與具體行動方針。本專案旨在提供系統化的精煉流程，將 raw 檔逐字稿一併轉化為以下三份具備實行價值的結構化產出：
1. **乾淨的發言紀錄**：自動清理語氣贅字、修正專有名詞與台英語錯字，產出排版清晰的對齊逐字稿。
2. **結構化會議重點摘要**：條列會議核心結論、會議議題與結論矩陣、爭議與妥協歷程，以及具體的待辦行動事項表。
3. **行動價值的戰略分析與執行路徑**：自適應套用商務/公務分析框架（如 SWOT、5 Whys、JTBD 等），並規劃出具體的 **30-60-90 天落地執行路徑（Roadmap）**，指出下一步該怎麼做。

---

## 🧠 整理原理與分析框架
AI 會在讀取逐字稿後，智慧評估會議的複雜度與主題，**自動拼裝並複合使用**以下最適合的分析框架，以產出具備行動價值的決策建議，並於報告開頭說明框架選用理由：
* **SWOT 分析 + TOWS 矩陣**：適用於涉及政策發展規劃、資源盤點或重大發展策略會議。
* **JTBD (Jobs-to-be-Done) + 價值主張**：適用於探討公共服務設計、便民措施改進與民眾期待分析。
* **5 Whys 根因分析 + RACI 責任分配**：適用於專案延宕、流程缺失檢討、跨部門協調障礙與權責釐清。
* **Pain & Gain 痛點分析**：適用於民意反饋彙整、公聽會意見整理與陳情案件剖析。
* **OKR 目標對齊 + 艾森豪優先權矩陣**：適用於定期工作會報同步、施政計畫進度追蹤與科室分工。

*特別要求：報告中的每一項戰略分析結論，皆會自動標註逐字稿的**行號引用**（例如 `[Ref: Line 42]`），確保字字有據，便於呈報與查證。*

---

## 💡 InfoGold 的核心哲學：將經歷轉化為智慧與能力
本專案的底層設計不僅是文字排版，更是一套「榨取談話經驗價值」的閉環系統，實踐以下核心原則：
1. **輸入-轉化-輸出閉環**：將每一篇雜亂的逐字稿看作生產素材，系統性地轉化為理性邏輯決策文件。
2. **費曼解構 (補齊思維斷層)**：將會議中複雜的爭執以最簡單的邏輯釐清，找出被忽略的思維斷層與潛在共識。
3. **偶然成功 SOP 化**：捕捉對話中的偶發靈感，在 Roadmap 中拆解為可重複執行的步驟，將一次性的價值轉化為長期能力資產。
4. **第一性原理與反向思考**：剝離表面詞藻直指本質問題，並透過預測失敗（WT 戰略與權責劃分）來強化當前行動方案。
5. **極致利他與共享**：提供高易讀性的共享決策套件，協助團隊迅速掌握下一步，固化為團隊複利能力。

---

## 🚀 使用方法

根據您的辦公環境，選擇以下任一方式使用：

### 方式一：網頁複製貼上（最簡單）
適用於使用 ChatGPT、Claude.ai、Gemini 等網頁版對話介面的使用者。
1. 開啟本專案的 [`RefineryPrompt.md`](file:///D:/MyProject/InfoGold/RefineryPrompt.md)。
2. 複製該檔案內的所有 Prompt 內容，貼入 AI 網頁對話框。
3. 在最下方附上您的原始逐字稿文字，送出即可。

### 方式二：本地文件調用
適用於使用可在本機讀寫檔案的 AI 助理（如 Claude Code, Gemini CLI, Pi 等）。
1. 將本專案的 [`InfoGold.md`](file:///D:/MyProject/InfoGold/InfoGold.md) 規則檔與您的逐字稿文字檔放入同一個資料夾。
2. 對您的 AI 助理輸入指令：
   > `"請閱讀 @InfoGold.md，然後協助整理 @您的逐字稿檔案.txt"`
3. AI 將自動在資料夾中生成 `output/` 資料夾與三份整理後的報告。

### 方式三：安裝為全域指令
如果您經常需要使用此功能，可以將 [`InfoGold.md`](file:///D:/MyProject/InfoGold/InfoGold.md) 中的規則內容複製，貼入您的 AI 助理全域自訂指令中，即可隨時在命令列直接呼叫：
> `infogold @您的逐字稿檔案.txt`

---

## 📁 檔案結構

```text
InfoGold/
├── InfoGold.md             # 本地端引導 AI 助理的規則檔
├── RefineryPrompt.md       # 網頁版 AI 複製貼上的 Prompt 範本
├── Draft.md                # 原始專案實作規格書 (藍圖)
├── asr_input_example.txt   # 跨部門協調會議的原始譯文範例
├── README.md               # 本說明文件
└── output/                 # 執行後自動產出的決策套件
    ├── 01_raw_aligned.md   # [產出一] 清理且標記發言人的乾淨逐字稿
    ├── 02_structured.md    # [產出二] 結構化重點摘要、妥協歷程與待辦事項表格
    └── 03_strategy.md      # [產出三] 自適應戰略分析報告與 30-60-90 天落地路徑
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
1. **Web UI (Copy-Paste)**: Copy [`RefineryPrompt.md`](file:///D:/MyProject/InfoGold/RefineryPrompt.md) and paste it into ChatGPT/Claude Web, followed by your transcript text.
2. **Local AI CLI**: Put [`InfoGold.md`](file:///D:/MyProject/InfoGold/InfoGold.md) in your workspace folder and run:
   `"Please read @InfoGold.md, then help organize @my_transcript.txt"`
3. **Global Custom Command**: Store `InfoGold.md` contents globally in your assistant's settings and call:
   `infogold @my_transcript.txt`
