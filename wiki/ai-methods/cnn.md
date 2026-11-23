# CNN 入門

## Beginner Explanation

CNN（Convolutional Neural Network，卷積神經網路）會學習從影像找出可以用來分類的特徵。前面的層可以擷取邊緣或紋理，後面的層再把這些訊號組合成較複雜的圖樣。見 [SRC-003](../sources/SRC-003.md) §1、§2.4。

## Definition and Key Concepts

卷積層用可學習的濾波器在影像的各個區域提取特徵。分類模型再整理這些特徵，為輸入影像產生各類別的分數。Transfer Learning（遷移學習）則把預訓練模型學到的特徵用於新的任務。見 [SRC-003](../sources/SRC-003.md) §2.4。

## Connection to Mammography and AI

[SRC-003](../sources/SRC-003.md) §2.2、§2.4 以 ResNet50 進行 Transfer Learning。每次輸入一張 FFDM 影像（CC 或 MLO），模型輸出 normal 或 pathological 的分類結果。研究效能以單張影像計算，患者層級表現與臨床輔助成效需要另外驗證。

## Related Topics

- [分類效能指標](classification-metrics.md)
- [Mammography Positioning](../fundamentals/mammography-positioning.md)

## References

- [SRC-003](../sources/SRC-003.md)，§1、§2.2、§2.4、Table 1。

## Last Reviewed

2026-11-23
