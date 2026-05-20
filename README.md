# InfoGold - 會議逐字稿整理與分析工具
#### [繁體中文 | [English](#english-version)]

本專案提供一套結構化的提示詞規範，協助使用者利用 AI 助理（如 Claude Code, Gemini, Pi 或網頁版 ChatGPT/Claude）將雜亂的會議錄音逐字稿整理為排版乾淨、具參考價值的會議紀錄與分析報告。

---

## 🎯 專案目標
原始錄音轉文字（ASR）常伴隨口語重複、錯別字、發言人混亂等問題。本專案旨在：
1. 自動清理語氣贅字、校正專有名詞，還原乾淨的發言紀錄。
2. 根據談話主題，套用常見的分析框架進行重點摘要與後續行動跟進。
3. 確保所有分析結論皆附帶原始逐字稿行號，便於後續查證，避免 AI 幻覺。

---

## 🧠 整理原理與分析框架
AI 會在讀取逐字稿後，自動判斷會議本質並套用以下適合的分析框架（可單獨套用或複合使用）：
* **SWOT 分析 + TOWS 矩陣**：適用於政策規劃、市場評估與發展策略會議。
* **JTBD (Jobs-to-be-Done) + 價值主張**：適用於服務設計、民眾需求與體驗分析。
* **5 Whys 根因分析 + RACI 矩陣**：適用於流程失誤、專案延宕或跨部門權責釐清。
* **Pain & Gain 痛點分析**：適用於民意陳情、客戶反饋與公聽會意見整理。
* **OKR 目標對齊 + 艾森豪矩陣**：適用於定期工作會報、時程進度同步與任務分配。

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
└── output/                 # 執行後自動產出的整理結果
    ├── 01_raw_aligned.md   # 清理且標記發言人的乾淨逐字稿
    ├── 02_structured.md    # 結構化會議重點摘要與待辦事項表格
    └── 03_strategy.md      # 自適應分析報告與 90 天執行路徑
```

---

<a name="english-version"></a>

# English Version

This project provides a structured prompt framework to help users organize raw, noisy ASR transcripts into clean records and strategic summaries using AI assistants.

## 🎯 Goal
1. Clean up filler words, correct technical terms, and align speaker roles.
2. Synthesize structured takeaways and action items using standard analytical frameworks.
3. Ensure traceabilty by adding line-number references back to the source text.

## 🚀 How to Use
1. **Web UI (Copy-Paste)**: Copy [`RefineryPrompt.md`](file:///D:/MyProject/InfoGold/RefineryPrompt.md) and paste it into ChatGPT/Claude Web, followed by your transcript text.
2. **Local AI CLI**: Put [`InfoGold.md`](file:///D:/MyProject/InfoGold/InfoGold.md) in your workspace folder and run:
   `"Please read @InfoGold.md, then help organize @my_transcript.txt"`
3. **Global Custom Command**: Store `InfoGold.md` contents globally in your assistant's settings and call:
   `infogold @my_transcript.txt`
