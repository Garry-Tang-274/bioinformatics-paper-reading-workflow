# 深度精读提示词
# Deep-Reading Prompt

## 使用说明
## Instructions

将论文文本、关键章节或经过授权的摘录提供给分析工具，并要求输出以下结构。不要让工具补写未提供的实验细节。

Provide the paper text, key sections, or authorized excerpts to the analysis tool and request the following structure. Do not allow the tool to invent experimental details that were not provided.

## 提示词正文
## Prompt Body

请先用三至五句话解释论文试图解决的生物学或计算问题，并说明这个问题为什么重要。

First explain in three to five sentences the biological or computational problem the paper addresses and why it matters.

请列出研究对象、数据来源、样本量、纳入排除标准、标签定义、训练验证测试划分，以及是否存在重复个体、重复序列或批次重叠。

List the study subjects, data sources, sample sizes, inclusion and exclusion criteria, label definitions, train-validation-test splits, and whether individuals, sequences, or batches overlap.

请用“输入—处理—输出”的顺序解释方法，并对每个关键模块说明它解决的问题，而不是只复述模型名称。

Explain the method in input-process-output order, and state the problem solved by each key module rather than merely repeating model names.

请逐项总结主要结果，并为每项结果记录对应图表、指标、对照、统计检验和作者结论。

Summarize each major result and record the corresponding figure or table, metric, control, statistical test, and author conclusion.

请将“论文直接证明”“论文提供支持但未完全证明”“基于证据的合理推断”分成三个区域。

Separate “directly demonstrated by the paper,” “supported but not fully demonstrated,” and “reasonable inference from the evidence” into three sections.

请最后给出局限、复现所需条件、对当前项目的可迁移启发，以及三个仍未解决的问题。

Finally provide limitations, requirements for reproduction, transferable implications for the current project, and three unresolved questions.
