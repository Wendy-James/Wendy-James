<div align="center">

# Wendy

**LLM Post-training × Agentic RL · 基础模型训练系统 · 研究工程**

研究语言模型如何通过可验证反馈、多步决策与工具交互实现持续改进；重视可复现训练、系统工程、严格评估和失败分析。

**当前方向：** 可验证奖励、智能体评测与高效模型训练系统。

[**研究作品集 ↗**](https://wendy-james.github.io/) &nbsp;·&nbsp; [English](README.md) &nbsp;·&nbsp; [项目索引 ↓](#当前主线)

</div>

---

## 当前主线

| 方向 | 研究重点 | 公开状态 |
| :--- | :--- | :--- |
| **基础模型训练系统** | Tokenizer → Transformer → 训练与系统优化 | [WendyFM：已完成分词器里程碑](https://github.com/Wendy-James/wendy-foundation-model) |
| **Post-training × Agentic RL** | 可验证反馈、工具使用评测、SFT-to-RL 研究问题 | **进行中** · 研究仓库暂为私有 |
| **工业机器学习** | 时间外评估、召回、排序、消融与排错 | [推荐算法离线复现](https://github.com/Wendy-James/short-video-recsys-reproduce) |

## 代表性工程证据

### 01 / [WendyFM：从零构建基础模型训练系统](https://github.com/Wendy-James/wendy-foundation-model)

**已完成：** Byte-level BPE 分词器。包含确定性合并规则、朴素版和索引优化版训练器、多语言测试与本地 CPU benchmark。

| 英文 | 代码 | 混合多语言 | 中文 |
| :---: | :---: | :---: | :---: |
| **7.25×** 加速 | **4.55×** 加速 | **4.57×** 加速 | **0.70×**（退化） |

*优化版对比朴素版，小规模合成语料。训练结果逐项一致，但优化版测得的 Python 内存分配峰值更高。以上不代表大模型预训练、GPU 加速或生产性能。*

[**代码**](https://github.com/Wendy-James/wendy-foundation-model) · [**实验报告**](https://github.com/Wendy-James/wendy-foundation-model/blob/main/report/tokenizer.md) · [**原始测量 CSV**](https://github.com/Wendy-James/wendy-foundation-model/blob/main/benchmarks/tokenizer/results.csv) · [**复现说明**](https://github.com/Wendy-James/wendy-foundation-model#reproduce-the-tokenizer-milestone)

**下一阶段（尚未完成）：** [Decoder-only Transformer 工程草稿 PR #24](https://github.com/Wendy-James/wendy-foundation-model/pull/24) 已通过独立环境的 Toy CPU 测试，仍待本人复核、依赖和复现环境验证、真实训练与评估。GPU/Attention profiling 和 Scaling 仍属于计划。

### 02 / Post-training × Agentic RL 研究

现阶段关注 **Verifier 一致性、数据选择、数学推理评估与 SFT-to-RL 实验设计**，下一阶段将研究工具调用奖励、多步交互环境与 Agentic RL。上述未来方向**不代表已完成智能体 RL 训练、验证过 RL 性能收益或发表论文**。

研究代码暂为私有，待结果核验且满足公开条件后再发布。

### 03 / [推荐系统召回与离线评估](https://github.com/Wendy-James/short-video-recsys-reproduce)

使用公开字段结构和模拟/脱敏样例，复现 Two-Tower/DSSM、负采样、时间切分、Faiss 风格 TopK 检索、消融实验及错误分析。

其他公开项目：[多模态检索](https://github.com/Wendy-James/ecommerce-multimodal-retrieval) · [RAG 检索评估](https://github.com/Wendy-James/llm-rag-system) · [Transformer 原理实验](https://github.com/Wendy-James/transformer-model-lab)。

## 研究与工程方法

**研究问题 → Baseline → 实现 → 测试 → 对照实验 → 局限性。**

优先复用、验证并标注可靠开源实现；关注正确性、失败案例、可复现命令与工程约束，不为 GitHub Contributions 的数量而提交。

工业实践是工程思维的来源，但**公司私有数据、内部实现、模型资产、业务指标与凭证不属于公开作品集**。模拟数据上的离线结果不代表线上业务效果。

---

[公开发布与证据核验原则](PUBLICATION_POLICY.md) · **公开代码、实验数据与复现说明已在上方项目中列出。**
