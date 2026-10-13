# 詹文婷 / Wendy Zhan

**基础模型 · LLM 后训练 · 机器学习研究工程**  
合肥工业大学信息与计算科学本科（2026 年毕业）

我关注**模型如何被训练、评估与改进**，包括从零构建训练组件、数据与验证器设计，以及具有可复现证据的机器学习实验。希望长期积累基础模型的研究和系统工程能力。

[英文主页](README.md) · [GitHub](https://github.com/Wendy-James) · [邮箱](mailto:1563887189@qq.com)

## 当前研究与工程

### [WendyFM：从零理解基础模型训练系统](https://github.com/Wendy-James/wendy-foundation-model)

**已完成并公开：Byte-level BPE Tokenizer（里程碑 1）。**

- 具有确定性的 BPE 合并规则、多语言预分词和特殊 Token 处理。
- 对朴素与索引优化版本做了输出完全一致性验证。
- 在**小规模合成数据、CPU 本地 benchmark**中，优化版在英文、代码、混合文本上分别达到 7.25×、4.55×、4.57× 速度；中文场景仅 0.70×，且 Python 分配内存更高。
- [技术报告（含方法和局限）](https://github.com/Wendy-James/wendy-foundation-model/blob/main/report/tokenizer.md) · [原始 Benchmark CSV](https://github.com/Wendy-James/wendy-foundation-model/blob/main/benchmarks/tokenizer/results.csv)

后续计划包括 Decoder-only Transformer、训练与评估、GPU Profiling 和 Scaling 实验。**这些是计划，而不是已完成成果。**

### LLM 后训练与可验证奖励研究（进行中）

目前重点研究 SFT 数据配方、数学答案验证、一致性检查、难度剖析与后续 RLVR 实验设计。仓库暂未公开；不宣称已有论文发表、完成 RL 训练或已经得到可复现的研究结论。

## 公开项目

| 项目 | 研究 / 工程主题 | 成果边界 |
| --- | --- | --- |
| [WendyFM](https://github.com/Wendy-James/wendy-foundation-model) | 分词器、模型训练系统 | 已完成分词器，其他模块逐步推进 |
| [短视频推荐复现](https://github.com/Wendy-James/short-video-recsys-reproduce) | 双塔召回、负采样、时间切分、离线指标 | 使用伪造/脱敏数据做离线实验，不代表线上业务提升 |
| [电商多模态检索](https://github.com/Wendy-James/ecommerce-multimodal-retrieval) | 图文检索、难负样本、错误案例 | 离线评估项目 |
| [RAG 检索评估](https://github.com/Wendy-James/llm-rag-system) | BM25、稠密检索、重排与消融 | 检索工程补充项目，不是预训练成果 |

## 工作方法

**研究问题 → 基线 → 实现 → 测试 → 对照实验 → 局限性。**

坚持优先复用并标注来源可靠的开源成果；评价指标、失败案例和复现实验优先于泛泛的技术标签。个人公开仓库不应包含雇主代码、内部数据、内部指标和凭证。

欢迎交流基础模型研究工程、训练系统和可复现评估：[邮箱](mailto:1563887189@qq.com)。
