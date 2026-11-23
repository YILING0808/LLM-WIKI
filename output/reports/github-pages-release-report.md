# GitHub Pages 發布檢查

| 項目 | 結果 |
|---|---|
| Wiki 保留 | 逐檔比對 wiki/ 與 AGENTS.md 和基準 ZIP 位元組一致。保留五份來源摘要、八個概念頁、索引、log 和既有 Lint／Presentation 報告。 |
| Pages 入口 | docs/index.html 與已完成教學簡報位元組一致。包含 docs/.nojekyll。CSS 與 JavaScript 均內嵌。簡報沒有圖片、外部腳本、外部樣式表或根目錄相依資源。所有內部錨點均存在，引用原文使用 HTTPS 絕對網址。 |
| PDF 與圖片 | 公開包無 PDF 或圖片。原版 SRC-003 與 SRC-005 標示 CC BY 4.0，SRC-004 標示 CC BY-NC 4.0。未逐一確認嵌入影像的再發布條件，故三份原文 PDF 均留在原始專案。各來源頁及 README 有 DOI。 |
| 個資 | 對公開 Markdown 與 HTML 檢查常見個資及敏感資料格式，包括電子郵件、台灣手機號碼、身分證號格式、病歷號字樣及本機路徑。未發現命中。文獻作者姓名保留作為書目。 |
| Wiki 本機連結 | 相對 Markdown 連結掃描發現三個目標為移出公開包的原始 PDF。已在 README 說明。保留原始 Wiki 位元組及現有 DOI 連結。 |
| 部署狀態 | 已核對公開資料夾與專案子路徑相容性。尚未上傳或部署到 GitHub，沒有線上部署結果。先前瀏覽器驗證的限制見 presentation-report.md。 |

[GitHub Pages 發布來源說明](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
