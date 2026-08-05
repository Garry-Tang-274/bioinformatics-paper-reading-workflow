# 生物信息学论文精读与汇报工作流
# Bioinformatics Paper Reading and Presentation Workflow

![Status](https://img.shields.io/badge/status-active-2f81f7)
![Scope](https://img.shields.io/badge/scope-methodological%20audit-8957e5)
![Language](https://img.shields.io/badge/docs-bilingual-d8aa56)
![License](https://img.shields.io/badge/license-MIT-3fb950)

这是一个面向生物信息学学习、科研讨论和组会汇报的可复用工作流。它把论文阅读拆分为研究问题、数据、方法、证据、局限、复现性与项目启发，并明确区分作者结论、实验事实和读者推断。

This is a reusable workflow for bioinformatics study, research discussion, and journal-club presentation. It separates paper reading into research questions, data, methods, evidence, limitations, reproducibility, and project implications while distinguishing author claims, observed results, and reader inference.

> **一分钟使用方法：** 填写报告模板，依次运行定位、逐图分析和批判性审计提示词，最后完成数据泄漏、基线公平性与复现性清单。
>
> **One-minute workflow:** Fill in the report template, run the orientation, figure-analysis, and critical-audit prompts in order, then complete the leakage, baseline-fairness, and reproducibility checklists.

[报告模板](templates/) · [分析提示词](prompts/) · [审计清单](checklists/) · [示例](examples/) · [个人主页](https://garry-tang-274.github.io)

[Report templates](templates/) · [Analysis prompts](prompts/) · [Audit checklists](checklists/) · [Examples](examples/) · [Portfolio](https://garry-tang-274.github.io)

## 核心原则
## Core Principles

先解释作者解决的生物学问题，再解释模型；先核对数据来源和划分，再讨论指标；把作者结论、直接证据与自己的推断明确分开。

Explain the biological question before the model; verify data sources and splits before discussing metrics; clearly separate author conclusions, direct evidence, and your own inference.

任何性能数字都应同时记录任务定义、比较基线、测试集组成、统计不确定性、调参预算和潜在泄漏路径。

Every performance number should be recorded together with the task definition, comparison baseline, test-set composition, statistical uncertainty, tuning budget, and potential leakage paths.

## 推荐流程
## Recommended Workflow

### 1. 快速定位
### 1. Orientation

在十五分钟内识别研究问题、主要数据、核心方法、最重要结果和作者声称的贡献。

Within fifteen minutes, identify the research question, main data, core method, most important result, and claimed contribution.

### 2. 建立证据表
### 2. Build an Evidence Table

逐图核对输入、对照、指标、误差线、消融实验和结果适用范围。

Inspect each figure for inputs, controls, metrics, error bars, ablations, and the valid scope of the result.

### 3. 批判性审计
### 3. Critical Audit

重点检查数据泄漏、负样本、批次效应、分布外泛化、统计功效、预训练数据重叠和复现条件。

Audit data leakage, negative sampling, batch effects, out-of-distribution generalization, statistical power, pretraining-data overlap, and reproduction conditions.

### 4. 压缩输出
### 4. Compress the Output

将信息整理为一页结论摘要、完整精读报告和四至八页组会结构。

Compress the analysis into a one-page conclusion summary, a full reading report, and a four-to-eight-slide journal-club structure.

## 最新方法学补充
## Latest Methodological Addition

[`checklists/claim-and-baseline-audit.md`](checklists/claim-and-baseline-audit.md) 专门核查“提升百分比”“最佳模型”“泛化能力”和“优于基线”等主张。

[`checklists/claim-and-baseline-audit.md`](checklists/claim-and-baseline-audit.md) specifically audits claims about improvement percentages, best models, generalization, and superiority over baselines.

它要求确认比较对象、数据划分、训练与调参预算、预训练数据重叠、指标与不确定性，并将无法定位的证据登记为待核验事项。

It requires checking comparison targets, data splits, training and tuning budgets, pretraining-data overlap, metrics, and uncertainty, while registering unresolved evidence explicitly.

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

`prompts` stores reusable analysis instructions, `templates` stores report and presentation skeletons, `checklists` stores methodological audits, and `examples` stores demonstrations that do not depend on copyrighted paper content.

## 使用边界
## Boundaries

本仓库不收录受版权保护的论文全文或高清图表。示例只使用原创概括、合成数据和可公开引用的书目信息。

This repository does not include copyrighted full papers or high-resolution figures. Examples use original summaries, synthetic data, and openly citable bibliographic information only.

工作流不能替代领域专家判断，也不能仅凭摘要评估实验质量。涉及关键图、表格或补充材料时，必须查看原始内容。

The workflow cannot replace domain-expert judgment and cannot evaluate experimental quality from an abstract alone. Key figures, tables, and supplementary materials must be inspected directly.

自动生成的术语解释、数学公式和统计结论必须回到论文、代码或权威资料核验。

Automatically generated terminology explanations, equations, and statistical conclusions must be verified against the paper, code, or authoritative sources.

## 许可
## License

模板与原创文字采用 MIT 许可证。引用具体论文时，请遵守相应出版商、作者和数据提供方的许可条件。

Templates and original text are licensed under the MIT License. When citing specific papers, follow the licensing conditions of the relevant publisher, authors, and data providers.
