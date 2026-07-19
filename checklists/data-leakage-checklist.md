# 数据泄漏检查清单
# Data-Leakage Checklist

- [ ] 同一个体是否跨训练集和测试集？
- [ ] Does the same individual appear across training and test sets?
- [ ] 相同或近重复序列是否跨集合？
- [ ] Do identical or near-duplicate sequences cross splits?
- [ ] 预处理参数是否使用了测试集统计量？
- [ ] Were preprocessing parameters estimated using test-set statistics?
- [ ] 特征中是否包含结果发生后才可获得的信息？
- [ ] Do features contain information available only after the outcome?
- [ ] 负样本来源是否与正样本来源形成批次捷径？
- [ ] Does the source of negative samples create a batch shortcut relative to positives?
- [ ] 超参数是否反复根据最终测试集选择？
- [ ] Were hyperparameters repeatedly selected using the final test set?
- [ ] 外部验证集是否真正独立于训练数据来源？
- [ ] Is the external validation set genuinely independent of training-data sources?
