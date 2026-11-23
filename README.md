# 第十週作業｜溫室白漆節能效果 LLM Wiki + 教學 HTML 簡報

## 專案說明
本專案以溫室白漆節能實驗為主題，先將實驗背景、分組與資料處理、耗電量數據、計算方式、研究限制及後續改善方向拆成六篇可獨立 ingest 的 Markdown Wiki 條目，再依 Wiki 條目製作教學 HTML 簡報。

## 檔案結構

```text
Week10_Greenhouse_Wiki_Slides/
├── index.html                  # GitHub Pages 首頁：教學簡報
├── README.md
├── wiki/
│   ├── 00_Wiki_索引.md
│   ├── 01_實驗背景與研究問題.md
│   ├── 02_實驗分組與資料處理.md
│   ├── 03_耗電量資料表.md
│   ├── 04_計算方法與結果.md
│   ├── 05_結果解讀與研究限制.md
│   └── 06_後續實驗改善方向.md
├── prompts/                    # 先討論後生成、Wiki 與簡報生成 Prompt
├── workflow/
│   ├── graph.mmd                # Mermaid workflow graph
│   ├── validation_checklist.md  # 檢查清單
│   └── run_log_template.md      # 實際執行紀錄表（待平台實測填寫）
└── slides/
    └── index.html              # 教學簡報原始檔
```

## 如何使用
1. 將 `wiki/01` 至 `wiki/06` 六篇 Markdown 文件分別匯入 LLM Wiki（至少 ingest 五篇）。
2. 可先匯入 `00_Wiki_索引.md`，讓 Wiki 有整體導覽與檢索關鍵詞。
3. 使用 `prompts/01_先討論後生成_需求釐清.md` 的問題先和 LLM 討論，不要一開始就直接要求生成整份簡報。
4. 使用 `prompts/02_Wiki_生成提示詞.md` 整理或更新 Wiki；使用 `prompts/03_簡報生成提示詞.md` 讓模型以 Wiki 為依據產生簡報內容。
5. `index.html` 為可離線瀏覽的教學簡報，也可放在 GitHub Repository 根目錄後以 GitHub Pages 發布。

## 簡報操作
- 按「上一頁／下一頁」按鈕。
- 使用鍵盤 `←`、`→` 或 `PageUp`、`PageDown` 切換頁面。
- `Home` 回第一頁，`End` 到最後一頁。
- 手機可直接點擊按鈕操作。

## 核心數據（每分地）

| 期間 | 塗白漆組 | 對照組 |
|---|---:|---:|
| 6/18–7/18 | 130.65 | 219.60 |
| 7/18–8/18 | 77.10 | 143.80 |
| 8/18–9/16 | 195.55 | 397.90 |
| 累計 | 403.30 | 761.30 |

## 重要誠實性說明
這個資料包包含可供 LLM Wiki ingest 的知識條目與已製作的 HTML 簡報。外部 LLM Wiki 平台的實際 ingest、檢索與生成紀錄，需在使用者自己的平台執行後再填入 `workflow/run_log_template.md`，並截取真實畫面作為作業證據。本機數據預檢不等同於外部 Wiki 平台的執行紀錄。
