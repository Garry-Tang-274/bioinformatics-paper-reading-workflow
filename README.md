# 生物信息学论文精读与汇报工作流
# Bioinformatics Paper Reading and Presentation Workflow

这是一个面向生物信息学学习、科研讨论和组会汇报的可复用工作流。它将论文阅读拆分为背景、问题、数据、方法、结果、局限、复现性和项目启发，并提供严格对应的中英双语模板。

This is a reusable workflow for bioinformatics study, research discussion, and journal-club presentation. It separates paper reading into background, question, data, methods, results, limitations, reproducibility, and project implications, and provides strictly corresponding Chinese-English templates.

本仓库不收录受版权保护的论文全文或高清图表。示例只使用原创概括、合成数据和可公开引用的书目信息。

This repository does not include copyrighted full papers or high-resolution figures. Examples use only original summaries, synthetic data, and openly citable bibliographic information.

## 适用场景
## Intended Uses

工作流适合精读方法论文、数据库论文、基准测试、机器学习模型、单细胞研究和多组学研究，也可用于生成 Word 报告或简洁的组会幻灯片提纲。

The workflow is suitable for methods papers, database papers, benchmarks, machine-learning models, single-cell studies, and multi-omics research, and it can also generate outlines for Word reports or concise journal-club slides.

## 核心原则
## Core Principles

先解释作者解决的生物学问题，再解释模型；先核对数据来源和划分，再讨论指标；把作者结论、证据和自己的推断明确分开。

Explain the biological question before the model; verify data sources and splits before discussing metrics; clearly separate the authors’ conclusions, supporting evidence, and your own inference.

任何性能数字都应同时记录任务定义、比较基线、测试集组成、统计不确定性和潜在泄漏路径。

Every performance number should be recorded together with the task definition, comparison baseline, test-set composition, statistical uncertainty, and potential leakage paths.

## 推荐流程
## Recommended Workflow

第一遍在十五分钟内完成定位：研究问题、主要数据、核心方法、最重要结果和作者声称的贡献。

Use the first fifteen minutes for orientation: identify the research question, main data, core method, most important result, and claimed contribution.

第二遍建立结构化证据表，逐图核对输入、对照、指标、误差线和消融实验。

Use the second pass to build a structured evidence table and inspect each figure for inputs, controls, metrics, error bars, and ablation studies.

第三遍进行批判性审计，重点检查数据泄漏、负样本、批次效应、分布外泛化、统计功效和复现条件。

Use the third pass for critical auditing, focusing on data leakage, negative sampling, batch effects, out-of-distribution generalization, statistical power, and reproduction conditions.

最后将信息压缩为一页结论摘要、完整精读报告和四至八页组会结构。

Finally compress the information into a one-page conclusion summary, a full reading report, and a four-to-eight-slide journal-club structure.

## 仓库结构
## Repository Structure

```text
bioinformatics-paper-reading-workflow/
├─ prompts/
├─ templates/
├─ checklists/
├─ examples/
├─ CONTRIBUTING.md
└─ README.md
```

`prompts` 保存可复用分析指令，`templates` 保存报告与汇报骨架，`checklists` 保存方法学审计清单，`examples` 保存不依赖论文版权内容的演示。

`prompts` stores reusable analysis instructions, `templates` stores report and presentation skeletons, `checklists` stores methodological audit lists, and `examples` stores demonstrations that do not depend on copyrighted paper content.

## 最小使用方法
## Minimal Usage

选择一篇论文，先填写 `templates/paper-report-template.md` 的元信息和研究问题，再依次使用三个 prompt，最后完成数据泄漏与复现性清单。

Choose a paper, first complete the metadata and research-question sections in `templates/paper-report-template.md`, then use the three prompts in sequence, and finally complete the leakage and reproducibility checklists.

输出内容应引用 DOI、PubMed、期刊页面、代码仓库或数据集页面，而不是上传论文全文。

Outputs should cite DOI, PubMed, journal pages, code repositories, or dataset pages rather than uploading the full paper.

## 当前边界
## Current Boundaries

工作流不能替代领域专家判断，也不能仅凭摘要评估实验质量。涉及关键图、表格或补充材料时，必须直接查看原始内容。

The workflow cannot replace domain-expert judgment and cannot evaluate experimental quality from the abstract alone. Key figures, tables, and supplementary materials must be inspected directly.

自动生成的术语解释、数学公式和统计结论必须回到原文、代码或权威资料核验。

Automatically generated terminology explanations, equations, and statistical conclusions must be verified against the paper, code, or authoritative references.

## 许可
## License

模板与原创文字采用 MIT 许可证。引用具体论文时，请遵守相应出版商、作者和数据提供方的许可条件。

Templates and original text are licensed under the MIT License. When citing specific papers, follow the licensing conditions of the relevant publisher, authors, and data providers.
