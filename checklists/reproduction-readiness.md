# 论文复现前检查清单
# Reproduction Readiness Checklist

在开始写复现代码前，先冻结“要复现什么”。复现目标可以是某个主结果、某张图、某个基线、某个数据预处理步骤或某个评价指标，但不能只写“复现整篇论文”。

Before writing reproduction code, freeze exactly what will be reproduced. The target may be a main result, figure, baseline, preprocessing step, or evaluation metric, but should not be described only as “reproduce the whole paper.”

## 1. 冻结论文与实现版本
## 1. Freeze the Paper and Implementation Version

- [ ] 记录论文标题、DOI / arXiv / PubMed 标识和阅读版本。
- [ ] Record the paper title, DOI / arXiv / PubMed identifier, and the exact version read.
- [ ] 记录作者代码仓库、commit / tag / release；没有代码时明确写“无官方实现”。
- [ ] Record the author repository and commit / tag / release; if no code is available, state “no official implementation.”
- [ ] 将论文正文、补充材料、代码 README 和实际默认配置之间的不一致单独登记。
- [ ] Log disagreements among the paper, supplement, repository README, and actual default configuration separately.

## 2. 冻结数据与划分
## 2. Freeze Data and Splits

- [ ] 记录数据集版本、下载来源、样本单位和纳入 / 排除条件。
- [ ] Record dataset version, source, sample unit, and inclusion / exclusion criteria.
- [ ] 明确训练、验证、测试的划分方式，以及是否按个体、时间、批次或其他分组划分。
- [ ] Specify how train, validation, and test sets are split, including subject-, time-, batch-, or group-level separation.
- [ ] 检查重复样本、近重复样本、预训练数据重叠和标签泄漏路径。
- [ ] Check duplicates, near-duplicates, pretraining overlap, and possible label-leakage paths.

## 3. 冻结基线与指标
## 3. Freeze Baselines and Metrics

- [ ] 对每个要比较的基线记录输入、特征、训练预算、调参预算和随机种子策略。
- [ ] For every baseline, record inputs, features, training budget, tuning budget, and random-seed policy.
- [ ] 记录指标的精确定义、平均方式、候选集大小、阈值和置信区间 / 误差线计算方法。
- [ ] Record the exact metric definition, averaging rule, candidate-set size, thresholds, and confidence-interval / error-bar method.
- [ ] 不把不同数据划分、不同候选集或不同预训练资源下的数字直接当作公平对比。
- [ ] Do not treat numbers from different splits, candidate sets, or pretraining resources as directly comparable.

## 4. 冻结环境
## 4. Freeze the Environment

- [ ] 记录 Python / R 版本、关键依赖版本、CUDA / CPU 环境和硬件约束。
- [ ] Record Python / R versions, key dependency versions, CUDA / CPU environment, and hardware constraints.
- [ ] 优先从官方 lock file、environment file、container 或 release 中恢复环境；缺失时记录替代版本及理由。
- [ ] Prefer official lock files, environment files, containers, or releases; when substitutes are necessary, record the version and reason.

## 5. 先定义“复现成功”
## 5. Define Success Before Running

- [ ] 写出允许的数值偏差或定性一致性标准。
- [ ] Define acceptable numerical deviation or qualitative agreement criteria.
- [ ] 区分 exact reproduction、close reproduction、conceptual reproduction 和 failed reproduction。
- [ ] Distinguish exact reproduction, close reproduction, conceptual reproduction, and failed reproduction.
- [ ] 如果结果不一致，先定位数据、实现、环境、随机性和论文描述差异，不要直接把差异解释成“论文错误”。
- [ ] If results differ, first localize differences in data, implementation, environment, randomness, and paper description rather than immediately concluding that the paper is wrong.

## 最终记录
## Final Record

复现完成后至少保存：目标版本、数据来源、环境文件、运行命令、随机种子、原始输出、处理脚本、最终图表，以及“与原文一致 / 不一致”的证据链。

After reproduction, retain at minimum the target version, data source, environment file, run commands, random seeds, raw outputs, processing scripts, final figures, and the evidence chain supporting agreement or disagreement with the paper.
