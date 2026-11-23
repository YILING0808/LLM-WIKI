# AI 篩檢判讀流程

## Beginner Explanation

同一個 AI 分數可以在流程中做不同的事。它可以在醫師讀片時提供輔助，也可以用來決定哪些檢查要進入額外讀片。評估效果前，先確認每一類檢查由誰判讀，以及什麼條件會觸發人工處理。見 [SRC-004](../sources/SRC-004.md) Results、Discussion。

## Definition and Key Concepts

| AI 角色 | 在篩檢流程中的用途 |
|---|---|
| Second Reader | AI 在判讀流程中提供第二判讀意見或同步輔助，醫師仍參與判讀。 |
| Triage | 依 AI 分數或風險分層，決定優先順序或分配不同讀片路徑。 |
| Decision Referral | 依預設閾值將指定範圍的檢查轉交人工判讀。 |
| Standalone Reader | 在被評估的流程中，由 AI 獨立產生判讀結果。 |

依 [SRC-004](../sources/SRC-004.md) Results 的角色分組整理，實際安排依各研究而異。

## Evidence and Applicability

[SRC-004](../sources/SRC-004.md) Results 轉述 MASAI 試驗階段性結果，AI 組每千次篩檢偵測 6.4 例癌症，對照組為 5.0 例。此指標以篩檢次數為分母。回顧在 Abstract、Discussion 報告部分流程的讀片量減幅約 40–90%，範圍涵蓋不同流程及研究設計。

### PRAIM 的雙人判讀實例

[SRC-005](../sources/SRC-005.md) Results、Table 2 與 Extended Data Figure 1 顯示，Normal Triaging 在工作清單標記 AI 判為低疑慮的檢查，Safety Net 則在醫師先判為無疑慮而 AI 判為高度可疑時提示複看。兩組皆保留雙人判讀。對照 [SRC-004](../sources/SRC-004.md) 的角色分類，PRAIM 示範 Triage 與 Decision Support 如何同時融入一個流程。

PRAIM 是觀察性導入研究。其較高的模型估計乳癌偵測率與使用 AI 有關，醫師自行選擇使用 AI 仍可能造成殘餘混雜。這與上文 [SRC-004](../sources/SRC-004.md) 轉述的 MASAI 隨機試驗各有自己的研究設計及結果。PRAIM 的 Interval Cancer 和長期結果仍待查驗（[SRC-005](../sources/SRC-005.md) Discussion）。

## Limitations and Open Questions

讀片減幅受閾值、基準流程及研究設計影響。部分研究的 Interval Cancer（篩檢間隔期癌症）追蹤在此回顧中仍不完整。需同時檢視偵測、召回、讀片量與後續追蹤結果，才能評估特定流程（[SRC-004](../sources/SRC-004.md) Discussion）。

## Related Topics

- [分類效能指標](../ai-methods/classification-metrics.md)

## References

- [SRC-004](../sources/SRC-004.md)，Abstract、Results、Discussion。

- [SRC-005](../sources/SRC-005.md)，Results、Methods、Table 3。

## Last Reviewed

2026-11-23
