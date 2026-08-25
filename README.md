<div align="center">

# 医保欺诈识别与风险防控

**从异常识别，走到可解释的风控策略——一段诚实保留的数据科学历史。**

*Historical data-science experiment: from anomaly detection to explainable risk strategy.*

</div>

这是一个早期数据科学项目快照，研究如何把 CMS Medicare Part B 数据与 OIG LEIE 排除名单连接起来，从异常识别继续走到模型解释和风险策略。

## 当时的问题

单纯得到一个高风险分数并不能直接支持业务动作。风控人员还需要知道：

- 哪些行为模式推动了风险；
- 模型判断能否被解释；
- 高风险样本应该进入什么复核或规则；
- 阈值变化会怎样影响漏判与误判。

仓库保留了逻辑回归、随机森林、XGBoost、DNN、SHAP 解释和策略生成的实验代码。

## 诚实边界

这个仓库**不是可直接部署的生产系统**，当前版本也不能独立复现实验：

- 原始 CMS / LEIE 数据未随仓库发布；
- 配置仍包含当时的本地 Windows 数据路径；
- 历史 README 中的部分目录、Agent 架构和性能数字无法由当前仓库独立验证；
- 当前没有完整依赖文件和自动化测试。

因此，本次整理移除了无法复现的性能主张。这个仓库只作为一段历史探索保留：它记录了我从「训练模型」转向「解释结果、连接业务策略」的起点。

## 可见代码

```text
base_model.py / logistic.py / random_forest.py / xgboost_model.py / dnn.py
model_explainer.py      模型解释
strategy_generator.py  风险规则与策略输出
run_experiment.py       历史实验入口
evaluation.py           评估工具
```

## 如果重新开始

我不会先堆模型，而会先补齐：可公开的小型样本、数据契约、可复现实验环境、基线模型、成本敏感指标、策略验收方式和测试。只有这些证据成立后，项目才有资格重新成为主页旗舰。

> Kept as learning history; not presented as a current production project.
