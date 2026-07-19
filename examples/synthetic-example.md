# 合成示例：基因表达分类器
# Synthetic Example: Gene-Expression Classifier

本示例使用虚构数据演示工作流，不对应任何真实患者、论文或实验。

This example uses fictional data to demonstrate the workflow and does not correspond to any real patient, paper, or experiment.

研究问题是：使用一百个基因的表达量能否区分两种合成细胞状态，并在未见批次上保持性能？

The research question is whether expression values from one hundred genes can distinguish two synthetic cell states and retain performance on an unseen batch.

数据包含三个批次，每批次二百个细胞。训练使用前两个批次，测试只使用第三个批次，以避免随机划分掩盖批次依赖。

The data contain three batches with two hundred cells each. The first two batches are used for training and the third batch alone is used for testing so that a random split cannot hide batch dependence.

基线模型是逻辑回归，比较模型是随机森林。主要指标为宏平均 F1，同时报告每类召回率和校准曲线。

The baseline model is logistic regression and the comparison model is a random forest. The primary metric is macro F1, with per-class recall and calibration curves also reported.

若随机划分性能显著高于按批次划分性能，合理结论是模型利用了批次相关信号；不能直接声称模型学习了稳定的细胞状态生物学。

If random-split performance substantially exceeds batch-held-out performance, the reasonable conclusion is that the model used batch-associated signals; one cannot directly claim that it learned stable cell-state biology.

最小复现需要生成固定随机种子的合成矩阵、保存划分索引、训练两个模型，并核对测试集宏平均 F1 是否落在预设区间。

The minimal reproduction requires generating a synthetic matrix with a fixed random seed, saving split indices, training both models, and checking whether test macro F1 falls within a predefined interval.
