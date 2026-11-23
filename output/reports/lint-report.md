# Mammography AI Wiki — Lint Report

- 檢查日期：2026-11-23（台北時間）
- 基準：`mammography-ai-wiki-proposal-005.zip`，含 SRC-001–005。
- 總評：**WARNING**。本次未觀察到達到 FAIL 門檻的 Wiki 問題。SRC-003 的分母差異出自原文，Wiki 已標明，仍列為 WARNING。
- 範圍：依封裝內 AGENTS.md §8，檢查 15 份 Wiki Markdown（索引、變更紀錄、5 個來源摘要、8 個概念頁）。程式核對結構、相對連結、來源 ID 與 PDF 雜湊。人工核對關鍵主張與指定原文位置，並抽查 UCLA 與 ACR 公開頁。未全面測試外部連結或獨立驗證台灣現行規範與各試驗長期結果。

## Structure — WARNING

| 結果 | 檔案／位置 | 實際發現 | 建議 |
|---|---|---|---|
| PASS | `wiki/`、`wiki/sources/` | 15 份 Markdown 各有一個 H1。8 個概念頁採 kebab-case。5 個來源檔名與頁首 ID 一致，書目可識別，1–5 無重複。封裝無重複路徑且 CRC 檢查通過。 | 延用命名與 ID 慣例。 |
| PASS | `wiki/log.md` | 依序記錄 Proposal 001–005，各有批准依據、變更、Lint 與待查事項。Proposal 001 的「仍需至少 4 份」是當時的紀錄。 | 保留歷史條目。 |
| WARNING | `wiki/index.md` → Pending Areas | 把 FFDM、DBT 與其他待補主題一起寫為缺乏已批准來源。FFDM 已見於 SRC-003 §2.2，DBT 已見於 SRC-004 納入範圍。 | 標記「已有研究情境引用，尚缺入門概念頁」。 |
| WARNING | `wiki/index.md` → Pending Areas | Breast Density、Mass、Calcification、Architectural Distortion、FFDM／DBT、CADe／CADx 尚無專門概念頁。BI-RADS 已有入門頁，Assessment Categories 詳細判準仍待補。 | 根據教學範圍與可查驗來源提案，再建立概念頁。 |
| WARNING | `raw/guidelines/ucla-positioning-and-technique.md` | 教學網頁的登錄紀錄存於 guidelines，內容已清楚標註來源類型。 | 後續提案可調整分類或在索引明示來源類型。 |

## Links — PASS（機械檢查）

| 結果 | 檔案／位置 | 實際發現 | 建議 |
|---|---|---|---|
| PASS | `wiki/**/*.md`、`wiki/index.md` | 96 個相對 Markdown 連結均可解析到封裝內檔案。索引有 13 個唯一目標，涵蓋全部來源與概念頁。零未知 Source ID、零索引重複項、零孤立來源或概念頁。 | 變更路徑後重跑檢查。 |
| PASS | `wiki/sources/SRC-001.md`–`SRC-005.md` | 兩份官網資料與三篇期刊文章的標題、網址或 DOI 可區分。 | 保留各自 ID。SRC-004 與 SRC-005 的研究證據重疊見 Evidence。 |

## Evidence — WARNING

| 結果 | 檔案／位置 | 實際發現 | 建議 |
|---|---|---|---|
| PASS | `raw/papers/`、`wiki/sources/SRC-003.md`–`SRC-005.md` | 三份 PDF 的 SHA-256 各自與來源摘要一致。 | 保留原始 PDF 與雜湊。 |
| PASS | `wiki/fundamentals/breast-compression.md` → Beginner Explanation | UCLA 原頁 Introduction 明確支持壓迫可能造成短暫不適。此項覆核釐清先前的引用疑慮。 | 保留現有引文。 |
| WARNING | `wiki/fundamentals/mammography-positioning.md` → Definition and Key Concepts | Screening Mammography 的無症狀對象說明缺少就近引用。UCLA 原頁 Introduction 首段已有直接依據。 | 在該條後補 SRC-001 與章節位置。 |
| WARNING | `wiki/sources/SRC-001.md`、`SRC-002.md` → Verification and Source Access | 有官方網址、查閱日及章節定位，專案內無當時公開頁的固定版本。ACR 摘要所查驗的範圍為公開介紹。 | 在可取得且符合授權時登錄固定版本或封存網址。若需引用手冊內容，另核對對應章節。 |
| WARNING | `wiki/sources/SRC-003.md`、`wiki/ai-methods/classification-metrics.md` → Evidence and Applicability | PDF §2.2 報告 88 張測試影像。第 13 頁 Figure 6 與正文均顯示 TP 26、TN 51、FN 6、FP 4，共 87 張。77/87 約 88.5%、26/32 約 81.3%（四捨五入）、51/55 約 92.7%。Wiki 已區分重算與 Table 1。 | 保留差異。若取得更正或作者說明，再更新定量結論。 |
| WARNING | `wiki/sources/SRC-004.md`、`wiki/clinical-applications/ai-screening-workflows.md` → Evidence and Applicability | 回顧的 40–90% 是跨情境讀片減幅範圍。MASAI 的 6.4 與 5.0／千次來自回顧轉述。現有部分定位僅寫 Results、Discussion。 | 補到 MASAI 結果段落及對應流程小節。需要直接引用試驗時另提原始論文 Ingest。 |
| WARNING | `wiki/sources/SRC-004.md`、`SRC-005.md` | SRC-004 參考文獻第 19 筆已引用 PRAIM。兩份是不同文件，整理 PRAIM 效果時涉及同一研究。 | 在回顧與原始研究之間補交叉註記，彙整時只計一次該研究。 |
| PASS | `wiki/sources/SRC-005.md`、`wiki/ai-methods/classification-metrics.md` → PRAIM 讀表例子 | Figure 1 的 461,818 人可由兩組 260,739 + 201,079 重算，並與 463,094 名受篩檢女性區分。Table 3 核對偵測率 6.7／5.7 與召回率 37.4／38.3，分母均為每千名受篩檢女性。召回率差異的 95% CI 上限 +1.7% 低於 Methods 的 +10% 非劣性界線。 | 保留模型估計、分母與非劣性定義。 |

## Clinical Consistency — WARNING

| 結果 | 檔案／位置 | 實際發現 | 建議 |
|---|---|---|---|
| PASS | `wiki/imaging-findings/bi-rads.md` | 報告術語、結構、Final Assessment 和 Management Recommendations 符合 ACR 公開介紹。頁面已限定適用範圍。 | 若補分類判準、惡性機率或處置，須引用可查驗的對應版本和章節。 |
| WARNING | `wiki/fundamentals/cc-view.md`、`wiki/sources/SRC-001.md` | PNL 的 1 cm 有 UCLA 教學來源，正式品質要求與地區適用性仍待核對。植入物投照涉及的 MQSA 說法也尚未獨立查驗。 | 維持教學歸因。要用作臨床規範前，另核對適用地區、版本與正式文件。 |
| PASS | `wiki/ai-methods/cnn.md`、`classification-metrics.md`、`wiki/clinical-applications/ai-screening-workflows.md` | 單張 FFDM 影像分類、Digital Mammography／DBT 的回顧納入範圍和 PRAIM 的雙人判讀流程可區分。PRAIM 以關聯表述，保留醫師自行選用 AI 的殘餘混雜。 | 保留各來源的影像模態、AI 角色、分析單位和設計限制。 |
| WARNING | `wiki/clinical-applications/ai-screening-workflows.md`、`wiki/sources/SRC-004.md`、`SRC-005.md` | 部分研究的 Interval Cancer 追蹤在回顧範圍內仍不完整。PRAIM 的主要結果是偵測率與召回率。 | 更新長期安全性或地區適用性時，另查試驗追蹤與在地資料。 |

## Language — PASS（抽查）

| 結果 | 檔案／位置 | 實際發現 | 建議 |
|---|---|---|---|
| PASS | `wiki/fundamentals/`、`wiki/imaging-findings/`、`wiki/ai-methods/`、`wiki/clinical-applications/` | 抽查教學段落使用繁體中文，保留英文專業術語。 | 後續新增內容延續此用語方式。 |

## 查驗依據與處理狀態

- [UCLA Health — Positioning and Technique，Introduction](https://www.uclahealth.org/departments/radiology/education/breast-imaging-teaching-resources/screening-mammogram/positioning-and-technique)
- [ACR — BI-RADS，Current Release](https://www.acr.org/Clinical-Resources/Clinical-Tools-and-Reference/Reporting-and-Data-Systems/BI-RADS)
- [Ciurescu 等人 — SRC-003](https://doi.org/10.3390/medicina61050809)
- [Jassim 等人 — SRC-004](https://doi.org/10.1136/bmjopen-2025-111360)
- [Eisemann 等人 — SRC-005](https://doi.org/10.1038/s41591-024-03408-6)

本次僅新增此報告。修正建議尚未核准或套用。封裝內其餘檔案的內容已與基準逐一比對。
