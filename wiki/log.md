# Wiki Change Log

## [2026-11-23] ingest | Proposal 001: UCLA Positioning and Technique

- **Approval basis:** 使用者本回合明確批准「Proposal 001：UCLA Positioning and Technique」及建立獨立可交付副本；授權範圍為列出的 1 份來源註冊、1 份 source summary、4 份 concept pages、index/log 及 Lint。
- **Source ID:** SRC-001 — UCLA Health educational webpage; full body examined 2026-11-23, page publication/update date unverified.
- **Created:** `raw/guidelines/ucla-positioning-and-technique.md`（registration only, not original full-text copy）；`wiki/sources/SRC-001.md`；`wiki/fundamentals/mammography-positioning.md`；`wiki/fundamentals/cc-view.md`；`wiki/fundamentals/mlo-view.md`；`wiki/fundamentals/breast-compression.md`；`wiki/index.md`。
- **Log:** 本檔作為初始專案的第一筆附加紀錄；既有使用者專案未被覆寫。
- **Lint outcome:** 見 `output/reports/proposal-001-lint.md`（生成後檢查）。
- **Unresolved:** 未取得／保存 UCLA 網頁不可變原始全文；圖像重用權利未核實；發布日期未核實；非正式 Guideline；PNL 定量要求與 implants 規範未由正式來源交叉確認；仍需要至少 4 份不同來源。


## [2026-11-23] ingest | Proposal 002: ACR BI-RADS® 入門

- **Approval basis:** 使用者明確回覆「我批准 Proposal 002」。
- **Source ID:** SRC-002 — ACR 官方公開介紹網頁，已查閱 Current Release 與 Citation and Usage Guidelines。
- **Created:** `wiki/sources/SRC-002.md`、`wiki/imaging-findings/bi-rads.md`。
- **Updated:** `wiki/index.md`，新增概念與來源連結並細化待補範圍。此筆紀錄附加於 `wiki/log.md`。
- **Lint outcome:** PASS（相對連結、來源 ID、索引及核准變更範圍）。WARNING（原頁未保存固定版本，手冊全文未查閱）。
- **Unresolved:** Assessment Categories 詳細判準、惡性機率、追蹤建議及 Breast Density 分類待查驗。公開頁發布／更新日期未核實。

## [2026-11-23] ingest | Proposal 003: 2D Mammography 的 AI 影像分類

- **Approval basis:** 使用者明確回覆「我批准 Proposal 003」。
- **Source ID:** SRC-003 — Ciurescu 等人，2025，Medicina 61(5), 809。
- **Created:** `raw/papers/ciurescu-2025-ai-in-2d-mammography.pdf`、`wiki/sources/SRC-003.md`、`wiki/ai-methods/cnn.md`、`wiki/ai-methods/classification-metrics.md`。
- **Updated:** `wiki/index.md` 增列來源與概念頁連結，此紀錄附加於 `wiki/log.md`。
- **Lint outcome:** PASS（原始 PDF 雜湊、來源 ID、索引、相對連結與核准範圍）。WARNING（§2.2 的測試集為 88 張，Figure 6 正文四格合計 87；三項比例已核算）。
- **Unresolved:** 分母差異原因、患者層級切分與完整標籤驗證方式未核實。跨中心與臨床篩檢成效仍待相應驗證。

## [2026-11-23] ingest | Proposal 004: AI 如何融入乳癌篩檢判讀

- **Approval basis:** 使用者明確回覆「我批准 Proposal 004」。
- **Source ID:** SRC-004 — Jassim 等人（2025），BMJ Open 15(12), e111360。
- **Created:** `raw/papers/jassim-2025-ai-in-breast-cancer-screening.pdf`、`wiki/sources/SRC-004.md`、`wiki/clinical-applications/ai-screening-workflows.md`。
- **Updated:** `wiki/ai-methods/classification-metrics.md` 增加跨來源分母比較，`wiki/index.md` 新增連結，`wiki/log.md` 追加本筆。
- **Lint outcome:** PASS（PDF 雜湊、來源 ID、索引、連結、核准範圍及數值定位）。WARNING（研究異質性、部分 Interval Cancer 追蹤未完成，MASAI 數據取自回顧轉述）。
- **Unresolved:** MASAI 原始試驗與後續追蹤需獨立查驗。SRC-003 的 87／88 張分母差異仍待釐清。

## [2026-11-23] ingest | Proposal 005: PRAIM 真實世界導入研究

- **Approval basis:** 使用者明確回覆「我批准 Proposal 005」。
- **Source ID:** SRC-005 — Eisemann 等人（2025），Nature Medicine 31, 917–924。
- **Created:** `raw/papers/eisemann-2025-praim.pdf`、`wiki/sources/SRC-005.md`。
- **Updated:** `wiki/clinical-applications/ai-screening-workflows.md`、`wiki/ai-methods/classification-metrics.md`、`wiki/index.md`；本筆追加於 `wiki/log.md`。
- **Lint outcome:** PASS（PDF 雜湊、五個來源 ID、索引、連結、核准範圍及 Figure 1、Table 3 的樣本與指標核對）。WARNING（觀察性分組可能有殘餘混雜）。
- **Unresolved:** PRAIM 的 Interval Cancer 與長期結果待查；MASAI 原始試驗仍待獨立核對。
