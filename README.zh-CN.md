<div align="center">

# Wendy

**基础模型训练系统 · LLM 后训练 · 机器学习研究工程**

从底层实现模型系统，用可复现的实验衡量收益、成本与失败案例。

合肥工业大学 · 信息与计算科学本科 · 2026

[**个人研究作品集 ↗**](https://wendy-james.github.io/) &nbsp;·&nbsp; [English](README.md) &nbsp;·&nbsp; [邮箱](mailto:1563887189@qq.com)

</div>

---

## 当前主线

| 方向 | 研究重点 | 公开状态 |
| :--- | :--- | :--- |
| **基础模型训练系统** | Tokenizer → Transformer → 训练与系统优化 | [WendyFM：已完成分词器里程碑](https://github.com/Wendy-James/wendy-foundation-model) |
| **Post-training 研究** | 答案验证器、数学难度分层、SFT-to-RL 问题 | **进行中** · 研究仓库暂为私有 |
| **工业机器学习** | 时间外评估、召回、排序、消融与排错 | [推荐算法离线复现](https://github.com/Wendy-James/short-video-recsys-reproduce) |

## 代表性工程证据

### 01 / [WendyFM：从零构建基础模型训练系统](https://github.com/Wendy-James/wendy-foundation-model)

**已完成：** Byte-level BPE 分词器。包含确定性合并规则、朴素版和索引优化版训练器、多语言测试与本地 CPU benchmark。

| 英文 | 代码 | 混合多语言 | 中文 |
| :---: | :---: | :---: | :---: |
| **7.25×** 加速 | **4.55×** 加速 | **4.57×** 加速 | **0.70×**（退化） |

*优化版对比朴素版，小规模合成语料。训练结果逐项一致，但优化版测得的 Python 内存分配峰值更高。以上不代表大模型预训练、GPU 加速或生产性能。*

[**代码**](https://github.com/Wendy-James/wendy-foundation-model) · [**实验报告**](https://github.com/Wendy-James/wendy-foundation-model/blob/main/report/tokenizer.md) · [**原始测量 CSV**](https://github.com/Wendy-James/wendy-foundation-model/blob/main/benchmarks/tokenizer/results.csv) · [**复现说明**](https://github.com/Wendy-James/wendy-foundation-model#reproduce-the-tokenizer-milestone)

**下一阶段（未完成）：** Decoder-only Transformer、训练与评测基线、GPU/Attention profiling、Scaling 实验。

### 02 / Post-Training 与 RL Trainability 研究

正在探索 **数据选择、难度剖析、数学答案验证**与后续训练结果之间的关系。当前重点为 verifier 一致性、保守答案抽取和受控实验设计，**不宣称完成 SFT/RL 实验、论文发表或取得已验证的研究结论**。

研究代码暂为私有，待结果核验且满足公开条件后再发布。

### 03 / [推荐系统召回与离线评估](https://github.com/Wendy-James/short-video-recsys-reproduce)

使用公开字段结构和模拟/脱敏样例，复现 Two-Tower/DSSM、负采样、时间切分、Faiss 风格 TopK 检索、消融实验及错误分析。

其他公开项目：[多模态检索](https://github.com/Wendy-James/ecommerce-multimodal-retrieval) · [RAG 检索评估](https://github.com/Wendy-James/llm-rag-system) · [Transformer 原理实验](https://github.com/Wendy-James/transformer-model-lab)。

## 研究与工程方法

**研究问题 → Baseline → 实现 → 测试 → 对照实验 → 局限性。**

优先复用、验证并标注可靠开源实现；关注正确性、失败案例、可复现命令与工程约束，不为 GitHub Contributions 的数量而提交。

工业实践是工程思维的来源，但**公司私有数据、内部实现、模型资产、业务指标与凭证不属于公开作品集**。模拟数据上的离线结果不代表线上业务效果。

---

**欢迎交流基础模型、训练系统、可复现评估与研究工程。** [联系我 →](mailto:1563887189@qq.com)
