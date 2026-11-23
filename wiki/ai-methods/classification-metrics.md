# 分類效能指標

## Beginner Explanation

讀分類結果時，先問分母是什麼。Accuracy 看所有輸入影像。Sensitivity 看實際標為陽性的影像。Specificity 看實際標為陰性的影像。見 [SRC-003](../sources/SRC-003.md) §2 評估方法、Table 1。

## Definition and Key Concepts

在 Confusion Matrix（混淆矩陣）中，TP 和 TN 分別表示正確辨識的陽性和陰性，FN 是判成陰性的陽性，FP 是判成陽性的陰性。

| 指標 | 如何解讀 |
|---|---|
| Accuracy（準確率） | 全部樣本中分類正確的比例，(TP + TN) / (TP + TN + FP + FN)。 |
| Sensitivity（敏感度） | 陽性樣本中被正確辨識的比例，TP / (TP + FN)。 |
| Specificity（特異度） | 陰性樣本中被正確辨識的比例，TN / (TN + FP)。 |
| AUC-ROC | ROC 曲線下面積，概括模型在不同分類閾值下區分陽性與陰性的能力。 |

## Evidence and Applicability

[SRC-003](../sources/SRC-003.md) Table 1 報告 Accuracy 88.5%、Sensitivity 81%、Specificity 92.7%、AUC-ROC 0.93。Figure 6 旁正文列出 TP 26、TN 51、FN 6、FP 4，可重算 Accuracy（77/87 ≈ 88.5%）、Sensitivity（26/32 ≈ 81.3%）與 Specificity（51/55 ≈ 92.7%）。AUC-ROC 需不同閾值的資料，不能由這四格重算。

### 從單張影像分類到篩檢流程

[SRC-003](../sources/SRC-003.md) Table 1、Figure 6 的 Accuracy 以影像為分母，Sensitivity 和 Specificity 則分別以標為陽性和陰性的影像為分母。[SRC-004](../sources/SRC-004.md) Results 的 Cancer Detection Rate（CDR）以篩檢次數為分母，通常呈現每千次偵測到的癌症數。Recall Rate 同樣以篩檢次數為分母，分子為被召回進一步評估的篩檢。讀片工作量計算人工判讀次數，減幅以對照或原流程的讀片量為基準。比較結果前先確認分析單位與臨床角色。

### PRAIM 讀表例子

[SRC-005](../sources/SRC-005.md) Table 3 的模型估計乳癌偵測率為每千名受篩檢女性 6.7 對 5.7。絕對差異是每千名約多偵測 1.0 例（95% CI +0.3 至 +1.7）。相對差異以對照組為基準，原文估計為 +17.6%（95% CI +5.7% 至 +30.8%）。

召回率為每千名 37.4 對 38.3，相對差異為 −2.5%（95% CI −6.5% 至 +1.7%）。區間上限 +1.7% 低於研究預設的 +10% 非劣性界線，因此符合非劣性標準。區間包含 0，仍容許召回率略升或略降（Methods、Table 3）。

## Limitations and Open Questions

四格合計 87，方法（§2.2）列出 88 張測試影像，差異原因未核實。解讀時應一併確認分析單位、陽性標籤定義和資料來源。這組影像層級的效能數字無法直接估計患者層級的篩檢成效。

## Related Topics

- [CNN](cnn.md)
- [AI 篩檢判讀流程](../clinical-applications/ai-screening-workflows.md)

## References

- [SRC-003](../sources/SRC-003.md)，§2.2、§2 評估方法、Table 1、Figure 6。
- [SRC-004](../sources/SRC-004.md)，Results、Discussion。

- [SRC-005](../sources/SRC-005.md)，Results、Methods、Table 3。

## Last Reviewed

2026-11-23
