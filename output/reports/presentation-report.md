# 教學簡報驗證紀錄

主題：乳房攝影與人工智慧：從影像基礎到 AI 輔助乳癌偵測  
基準：Proposal 005 Lint 版。依使用者續指示產出現有證據版，保留大綱中的缺口。

| 狀態 | 檢查 | 實際結果 |
|---|---|---|
| 通過 | HTML 結構 | 15 頁、15 個跳頁選項、zh-TW、內部錨點存在且 ID 唯一。 |
| 通過 | 引用對照 | 逐頁核對 Wiki 路徑存在於基準專案，來源區列 Source ID、原文位置與原文連結。未重新測試所有外部網址。 |
| 通過 | 測驗靜態結構 | 3 題各含正解及解析，JavaScript 通過語法檢查。 |
| 未通過 | 教學範圍完整性 | 第 5 頁保留影像徵象缺口。第 2、6、8、10 頁標出成像、BI-RADS 詳細判準、FFDM／DBT 及 CADe／CADx 的證據邊界。 |
| 未驗證 | 瀏覽器操作與版面 | Chromium 嘗試啟動兩次，皆在建立本機 socket 時遭環境拒絕。沒有實際瀏覽器畫面可確認。鍵盤操作、導覽、進度、測驗互動與桌面／手機版面均未判為通過。 |

## 逐頁來源對照

| 頁次 | Wiki 路徑 | 來源／位置 |
|---|---|---|
| 1 | wiki/index.md | 課程導覽 |
| 2 | wiki/fundamentals/mammography-positioning.md | SRC-001 Introduction |
| 3 | wiki/fundamentals/cc-view.md, wiki/fundamentals/mlo-view.md | SRC-001 Introduction、CC View、MLO View |
| 4 | wiki/fundamentals/breast-compression.md | SRC-001 Introduction |
| 5 | wiki/index.md, wiki/imaging-findings/bi-rads.md | SRC-002 Current Release，支持報告結構背景 |
| 6 | wiki/imaging-findings/bi-rads.md | SRC-002 Current Release |
| 7 | wiki/ai-methods/cnn.md | SRC-003 §1、§2.4 |
| 8 | wiki/ai-methods/cnn.md, wiki/sources/SRC-003.md | SRC-003 §2.2、§2.4–2.6 |
| 9 | wiki/ai-methods/classification-metrics.md | SRC-003 §2.2、§2.6、Table 1、Figures 6–7 |
| 10 | wiki/clinical-applications/ai-screening-workflows.md | SRC-004 Results，AI 角色分組；Discussion |
| 11 | wiki/clinical-applications/ai-screening-workflows.md, wiki/sources/SRC-005.md | SRC-005 Results、Table 2、Extended Data Figure 1 |
| 12 | wiki/ai-methods/classification-metrics.md | SRC-004 Results；SRC-005 Methods、Table 3 |
| 13 | wiki/ai-methods/classification-metrics.md, wiki/clinical-applications/ai-screening-workflows.md | SRC-003 §4；SRC-004 Discussion；SRC-005 Discussion |
| 14 | wiki/fundamentals/cc-view.md, wiki/fundamentals/mlo-view.md, wiki/ai-methods/classification-metrics.md | SRC-001 CC View、MLO View；SRC-003 Figure 6；SRC-005 Table 3 |
| 15 | wiki/index.md | SRC-001 來源摘要與原文；SRC-002 來源摘要與原文；SRC-003 來源摘要與原文；SRC-004 來源摘要與原文；SRC-005 來源摘要與原文 |

HTML 與報告加入封裝副本。原始 Wiki 與既有封裝內容逐檔比對一致。
