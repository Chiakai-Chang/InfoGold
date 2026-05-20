# InfoGold - 經歷提煉與知識資產增值框架 (Experience Refining & Knowledge Asset Value-Adding Framework)
#### [繁體中文 | [English](#english-version)]

本專案的核心哲學是：**使用者提供的原始文本（如會議逐字稿、閱讀筆記、工作手稿或文章等）本身就是蘊含智慧的「知識金礦」**。

InfoGold 扮演著「煉金助理」的角色，透過結構化的提示詞規範與自動化隔離目錄，協助使用者利用 AI 助理（如 Claude Code, Gemini, Pi 或網頁版 ChatGPT/Claude）對原始文字資產進行**三部曲提煉與策略增值**，一氣呵成轉化為可複利、可行動的「黃金知識資產套件」。

---

## 🎯 煉金三部曲：知識資產價值加值階梯

1. **第一階段：洗礦與原意固化 (Washing & Preservation)** ➔ 生成 `01_cleaned_text.md`
   * **核心哲學**：原始資料本身即是核心資產，必須妥善保存作為未來溯源與參考依據。
   * **實踐**：在保留原始語彙與語意的前提下，自動清理口語贅字與排版雜訊，還原成高可讀性、條理分明的精煉文本。在此階段**堅決不替換發言者原有的專業術語或習慣用法**，維護最真實的現場情境與發言話語權。

2. **第二階段：精煉金磚 (Structuring & Readability)** ➔ 生成 `02_structured_summary.md`
   * **核心哲學**：將長篇或散落的原始資產，組織成高清晰度、便於跨部門呈報與分享的結構化加值文獻。
   * **實踐**：提煉核心結論與議題邏輯矩陣（套用臺灣商務/公務在地化專業語彙），使用**費曼技巧**解構討論中的「思維斷層（想法衝突點與共識）」，並將隨機好點子轉化為具備負責人與期限的標準待辦事項。

3. **第三階段：鑄造策略貨幣 (Strategic Compounding & Action)** ➔ 生成 `03_strategy_roadmap.md`
   * **核心哲學**：不只停留在整理，更進一步從精煉資產中**「延伸、萃取、分析出更多可複利、可行動的戰略價值」**，將歷史經歷與點子鑄造為引導未來的執行決策。
   * **實踐**：AI 智慧評估主題，自適應複合使用分析框架（SWOT/TOWS、JTBD、5 Whys 根因分析、OKR、痛點分析等）。報告中的每點結論**強迫標註行號或段落引註**確保字字有據，並規劃出 30-60-90 天的可行動 SOP 執行路徑（Roadmap）。

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
4. AI 將自動在 `output/` 目錄下建立以「執行日期_文本主題」命名的專屬資料夾（例如 `output/20260520_跨部門協調會議/`），並產出三份精煉報告，確保多次使用時不會互相覆蓋。


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
├── test/                   # 多元原始文本存放資料夾 (已設定隱私安全 gitignore)
│   ├── .gitkeep            # 資料夾說明檔
│   └── 原始文字檔範例.txt  # 放入您的文字檔 (例如會議對話、隨筆或筆記)
├── README.md               # 本說明文件
└── output/                 # 執行後自動產出的決策套件 (已設定隱私安全 gitignore)
    ├── .gitkeep            # 資料夾說明檔
    └── YYYYMMDD_[主題]/    # 每次執行產生的獨立決策支援套件資料夾
        ├── README.md       # [導覽門戶] 各份報告的核心亮點摘要與連結
        ├── metadata.json   # 本次執行日誌與狀態中繼資料
        ├── 00_source_[原始檔名].txt  # [封存原始檔] 從 test/ 自動移動至此備份，保持 test/ 乾淨
        ├── 01_cleaned_text.md  # [產出一] 精煉清理且保留原文語彙的完整文本
        ├── 02_structured_summary.md # [產出二] 結構化重點與行動矩陣 (臺灣在地化)
        └── 03_strategy_roadmap.md # [產出三] 自適應分析與 30-60-90 天落地路徑 (臺灣在地化)
```

---

<a name="english-version"></a>

# English Version

# InfoGold - Experience Refining & Knowledge Asset Value-Adding Framework

InfoGold is built on a core philosophy: **the user's raw input (ASR transcripts, meeting notes, personal drafts, or articles) is already a valuable "Knowledge Gold Ore"**. 

Instead of generating content from scratch, InfoGold serves as your "Refining Assistant" to preserve, structure, and compound this asset in a 3-step value-adding process:

## 🎯 Value-Adding Trilogy
1. **Preservation & Washing (`01_cleaned_text.md`)**: Cleans filler words and organizes syntax while strictly **preserving raw domain-specific terminology** to safeguard verbatim authenticity.
2. **Structuring & Readability (`02_structured_summary.md`)**: Structures disorganized content into clear key findings, logic matrices, and action lists, localized to regional context.
3. **Strategic Compounding (`03_strategy_roadmap.md`)**: Applies business/public sector frameworks (SWOT, OKR, 5 Whys) and maps out a concrete **30-60-90 day roadmap** to translate historical experience into forward-looking strategic value.

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
*(The AI will automatically locate the input text in the `test/` folder, generate output files inside a unique `output/YYYYMMDD_[Topic]/` folder, and move the original file to that folder to keep `test/` clean for future runs)*

### Mode 3: Global Custom Command
Save the rules from `InfoGold.md` globally in your assistant's settings and run:
```bash
infogold
```
