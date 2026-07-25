# 论文主张与基线公平性核查清单
# Paper Claim and Baseline Fairness Audit Checklist

本清单用于核查论文中的性能提升、最佳模型、泛化能力和优于基线等主张。它不判断作者是否诚信，而是检查结论与证据是否严格对应。

This checklist audits claims about performance gains, best models, generalization, and superiority over baselines. It does not judge author integrity; it checks whether conclusions correspond precisely to evidence.

## 1. 先固定主张原文与含义
## 1. Fix the Exact Claim and Its Meaning

记录作者的精确主张，并用自己的话改写一次。区分“在一个任务上更好”“平均更好”“统计显著更好”和“在所有条件下更好”。

Record the exact claim and rewrite it once in your own words. Distinguish “better on one task,” “better on average,” “significantly better,” and “better under all conditions.”

如果主张包含百分比，确认它是绝对百分点、相对提升、误差下降比例，还是多个数据集的平均值。

When a claim includes a percentage, determine whether it is an absolute percentage-point gain, a relative improvement, an error reduction, or an average across datasets.

## 2. 明确比较对象
## 2. Identify the Comparison Target

记录被比较的基线名称、版本、输入特征、预训练权重、训练数据、超参数和代码来源。

Record the baseline name, version, input features, pretrained weights, training data, hyperparameters, and code source.

确认论文比较的是最强公开基线、作者自行复现的基线、删减版本，还是从旧论文表格中引用的历史数字。

Determine whether the comparison uses the strongest public baseline, an author reimplementation, a reduced version, or a historical number copied from an older paper.

不同基线如果使用不同数据量、不同标签、不同外部知识或不同调参预算，就不能只比较最终分数而不说明资源差异。

If baselines use different data volumes, labels, external knowledge, or tuning budgets, final scores cannot be compared without reporting those resource differences.

## 3. 核对任务与测试集
## 3. Verify the Task and Test Set

确认所有模型是否解决同一个任务、使用同一个标签定义、同一个候选空间和同一个评估单位。

Confirm that all models solve the same task and use the same label definition, candidate space, and evaluation unit.

检查测试集是否完全一致，是否存在按样本、个体、患者、序列家族、批次或时间划分的差异。

Check whether the test set is identical and whether splits differ by sample, individual, patient, sequence family, batch, or time.

如果模型选择、阈值选择或早停使用了测试集信息，应把结果标为存在测试集污染风险。

If model selection, threshold selection, or early stopping used test-set information, mark the result as at risk of test-set contamination.

## 4. 核对训练与调参预算
## 4. Verify Training and Tuning Budgets

记录每个模型的随机种子数、训练轮次、搜索空间、试验次数、硬件和模型选择规则。

Record the number of random seeds, training epochs, search space, number of trials, hardware, and model-selection rule for each model.

如果新模型进行了大量超参数搜索，而基线只运行默认设置，比较可能反映调参预算而不是方法本身。

If the new model received extensive hyperparameter search while baselines used defaults, the comparison may reflect tuning budget rather than the method itself.

检查作者是否报告所有运行结果，还是只选择最佳种子、最佳数据集或最佳指标。

Check whether all runs are reported or only the best seed, dataset, or metric is selected.

## 5. 核对预训练数据与潜在重叠
## 5. Verify Pretraining Data and Potential Overlap

记录预训练语料、时间范围、数据库版本和去重方法。

Record the pretraining corpus, time range, database version, and deduplication method.

检查测试序列、患者、蛋白、文献或数据库条目是否可能出现在预训练或外部检索数据中。

Check whether test sequences, patients, proteins, publications, or database entries may appear in pretraining or external retrieval data.

无法排除重叠时，不应把结果直接解释为严格的分布外泛化。

When overlap cannot be excluded, do not interpret the result directly as strict out-of-distribution generalization.

## 6. 核对指标与不确定性
## 6. Verify Metrics and Uncertainty

确认指标是否适合类别不平衡、排序、校准或临床决策场景，并记录宏平均、微平均或加权平均方式。

Confirm that the metric is appropriate for class imbalance, ranking, calibration, or clinical decision settings, and record whether macro, micro, or weighted averaging is used.

要求同时查看均值、标准差、置信区间、随机种子和统计检验，而不是只看单个最高分。

Inspect means, standard deviations, confidence intervals, random seeds, and statistical tests rather than a single best score.

如果性能差异小于随机波动或误差范围，结论应写成“未显示稳定优势”，而不是“显著优于”。

If the performance difference is smaller than random variation or the uncertainty range, write “no stable advantage was demonstrated” rather than “significantly outperformed.”

## 7. 拆解提升百分比
## 7. Decompose Improvement Percentages

对“提升 16.3%”一类表述，必须回答：相对哪一个基线、哪个指标、哪个数据集、绝对值从多少到多少、是否平均、是否只选最佳结果。

For statements such as “improved by 16.3%,” answer: relative to which baseline, on which metric and dataset, from what absolute value to what value, whether averaged, and whether only the best result was selected.

相对提升可能在基线很低时显得很大，因此报告中应同时给出原始分数与绝对差值。

A relative improvement may appear large when the baseline is low, so reports should include the original scores and absolute difference.

## 8. 区分证据、作者解释与自己的推断
## 8. Separate Evidence, Author Interpretation, and Your Inference

把每个关键结论拆成三栏：观察到的结果、作者给出的解释、你的独立判断。

Split each key conclusion into three columns: observed result, author interpretation, and your independent judgment.

作者提出的机制解释如果没有消融、干预实验或替代假设对照，应标为解释性假说，而不是已证明机制。

If an author’s mechanistic explanation lacks ablation, intervention, or alternative-hypothesis controls, label it as an interpretive hypothesis rather than a proven mechanism.

## 9. 建立待核验事项表
## 9. Build an Unresolved-Item Register

对补充表、代码划分、预训练语料、基线参数和无法定位的百分比，记录具体问题、需要查看的来源和当前状态。

For supplementary tables, code splits, pretraining corpora, baseline parameters, and percentages that cannot be located, record the exact question, required source, and current status.

推荐状态为：`已核验 / Verified`、`部分核验 / Partially verified`、`未找到 / Not found`、`存在冲突 / Conflicting` 和 `无法判断 / Indeterminate`。

Recommended statuses are `Verified`, `Partially verified`, `Not found`, `Conflicting`, and `Indeterminate`.

## 10. 最终写作规则
## 10. Final Writing Rules

只有在任务、数据、预算、指标和统计不确定性均可比时，才使用“公平比较”或“明确优于”。

Use “fair comparison” or “clearly outperformed” only when task, data, budget, metrics, and statistical uncertainty are comparable.

证据不完整时，使用“论文报告”“结果提示”“尚不能排除”或“需要代码与补充材料确认”等限定表达。

When evidence is incomplete, use qualified wording such as “the paper reports,” “the result suggests,” “cannot yet exclude,” or “requires confirmation from code and supplementary materials.”
