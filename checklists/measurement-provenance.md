# 先确认测量，再比较模型
# Check the Measurement Before Comparing Models

准备证据表时，以一个实验结果为一行，不以数据库中的一条序列或一篇论文为一行。记录原论文、图/表/补充材料位置、实验构建、测量方法、单位、细胞或样本背景、对照及重复。

Use one experimental result per evidence row, rather than one sequence or one paper. Record the original paper, figure/table/supplement location, construct, assay, units, cellular or sample context, controls and replicates.

## 最小核对项
## Minimum Checks

- 数据库的标签来自实测、作者分类、人工整理，还是模型预测？“未标注”不能自动变成阴性。
- Does the database label come from a measurement, an author category, curation, or a prediction? Unlabelled does not automatically mean negative.
- 两组结果是否使用同一构建、实验条件、单位和归一化？差值能否解释为同一种变化？
- Do both results share the construct, experimental conditions, units and normalization? Does their difference represent the same change?
- 比较中的身份是记录、克隆、样本、供者还是研究？划分必须与目标泛化单位对应。
- Is the identity a record, clone, sample, donor or study? Splits must match the intended unit of generalization.
- 输入转换是否改变了坐标、长度、链映射或标签？保留原版本与转换说明。
- Did preprocessing change coordinates, length, chain mapping or labels? Retain the original version and transformation description.
- 哪些比较直接观测到，哪些由匹配、重采样或模型推断？把适用条件放在对应结论旁。
- Which comparisons are observed directly, and which rely on matching, resampling or model inference? Put the relevant conditions beside the conclusion.

## 一个可执行的停止条件
## A Practical Stop Condition

如果无法确认两个分数指向可比测量，先停止计算其生物效应差值，继续核对原方法与补充资料；仍可把模型预测表现作为独立问题评价。

If two scores cannot be tied to comparable measurements, stop interpreting their difference as a biological effect and check the original methods and supplement. Predictive performance can still be evaluated as a separate question.

填写 [证据台账模板](../templates/measurement-evidence.csv)，再结合[主张与基线检查](claim-and-baseline-audit.md)和[复现前检查](reproduction-readiness.md)决定下一步。

Fill in the [evidence-ledger template](../templates/measurement-evidence.csv), then use the [claim/baseline audit](claim-and-baseline-audit.md) and [reproduction-readiness checklist](reproduction-readiness.md) to choose the next step.
