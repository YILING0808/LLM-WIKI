# Mammography AI Wiki

本專案整理五份來源的乳房攝影與 AI 知識庫，包含原始 Wiki、15 頁繁體中文教學簡報及驗證紀錄。

- [Wiki 索引](wiki/index.md) · [變更紀錄](wiki/log.md) · [AGENTS.md](AGENTS.md)
- [GitHub Pages 簡報入口](docs/index.html)
- [Lint 紀錄](output/reports/lint-report.md) · [簡報驗證紀錄](output/reports/presentation-report.md) · [發布檢查](output/reports/github-pages-release-report.md)

## 發布

1. 解壓縮後，將本資料夾內的檔案與子資料夾上傳至 GitHub 儲存庫的 `main` 分支根目錄。確認在儲存庫首頁可看見 `docs/`、`wiki/` 及 `AGENTS.md`。上傳時連同 `docs/.nojekyll` 一併保留。
2. 開啟 **Settings → Pages → Build and deployment**，選 **Deploy from a branch**，設定 **main** 與 **/docs**，再按 **Save**。
3. 部署完成後，從 Pages 設定開啟 **Visit site**。專案網站一般為 `https://帳號.github.io/儲存庫名稱/`。交作業時可同時附上該網址及儲存庫的 `wiki/index.md` 網址。

## 原文存取

公開包保留五份 Source Pages。三份期刊 PDF 保留於原始專案，公開包改由下列 DOI 提供查閱入口。為保留原版 Wiki，Source Pages 內的三個本機 PDF 連結仍指向原始專案路徑。

- SRC-003：[Ciurescu 等人](https://doi.org/10.3390/medicina61050809)
- SRC-004：[Jassim 等人](https://doi.org/10.1136/bmjopen-2025-111360)
- SRC-005：[Eisemann 等人](https://doi.org/10.1038/s41591-024-03408-6)
