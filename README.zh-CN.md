<div align="center">

# Wendy

### 构建可验证学习系统

**LLM Post-training × Agentic RL · 基础模型训练系统**

关注语言模型智能体如何从**可验证反馈、工具交互与多步环境**中学习。希望通过可复现实现、严格评测与失败分析，让后训练研究结论有清晰的证据链。

[研究作品集 ↗](https://wendy-james.github.io/) &nbsp;·&nbsp; [English](README.md) &nbsp;·&nbsp; [公开工程证据 ↓](#公开工程证据)

</div>

---

## 研究主线

**长期方向：Post-training × Agentic Reinforcement Learning。** 重点研究奖励质量、Verifier、数据配方与环境设计如何影响可使用工具的语言模型智能体的学习与泛化。

| 方向 | 重点技术问题 | 状态 |
| :--- | :--- | :--- |
| **可验证反馈** | 答案抽取、Verifier 一致性、错误奖励和 Reward Hacking | 研究进行中；代码及中间结果暂不公开 |
| **SFT → RLVR** | 数据选择、难度分层、固定算力对照实验 | 正在研究；不宣称已验证 RL 收益 |
| **Tool-using Agents** | 多步任务、轨迹级评测、环境反馈 | **下一阶段研究计划**，不是已交付系统 |
| **训练系统工程** | Tokenizer、Decoder、测试、优化与 Profiling | 见下方 WendyFM 公开证据 |

以上是**研究问题及工程优先级**，不代表已发表论文、完成 Agentic RL 训练或达到前沿模型水平。

## 公开工程证据

### 01 / [WendyFM：基础模型训练系统](https://github.com/Wendy-James/wendy-foundation-model)

从底层组件入手，按照**实现 → 正确性测试 → 可复现实验 → 局限性分析**建立基础模型工程能力。

**已完成并公开可验证：** 确定性 Byte-level BPE 分词器、朴素及索引优化训练器、多语言差分测试、本地 CPU 合成数据基准测试。

| 测试语料 | 索引版相对朴素版 |
| :--- | ---: |
| 英文 | **7.25×** |
| 代码 | **4.55×** |
| 混合多语言 | **4.57×** |
| 中文 | **0.70×（变慢）** |

测试场景中两种训练器生成的 tokenizer 规格一致，但索引优化版测得的 Python 内存分配峰值更高。以上是**小规模合成语料 CPU 结果**，不代表大模型预训练或线上吞吐。

[技术报告](https://github.com/Wendy-James/wendy-foundation-model/blob/main/report/tokenizer.md) · [测量 CSV](https://github.com/Wendy-James/wendy-foundation-model/blob/main/benchmarks/tokenizer/results.csv) · [复现步骤](https://github.com/Wendy-James/wendy-foundation-model#reproduce-the-tokenizer-milestone)

**进行中：** [Decoder-only Transformer M2 草稿 PR #24](https://github.com/Wendy-James/wendy-foundation-model/pull/24)。草稿报告了隔离环境的 Toy CPU Smoke Tests；PR **尚未合并**，不宣称已完成真实预训练、独立复核或 GPU Profiling。

### 02 / [推荐系统召回与离线评测](https://github.com/Wendy-James/short-video-recsys-reproduce)

可检查的**离线复现项目**：Two-Tower/DSSM、负采样、时间切分、TopK 指标、消融分析及数据泄漏检查。

该仓库使用的**模拟/匿名化离线数据**中，记录的时间切分 Recall@50 从 **0.112 提升至 0.126**（不同配置对比）。这**不代表线上 A/B 实验或雇主真实业务收益**。

[实验材料](https://github.com/Wendy-James/short-video-recsys-reproduce/tree/main/evidence_pack) · [消融记录](https://github.com/Wendy-James/short-video-recsys-reproduce/blob/main/experiments/ablation.csv)

### 03 / 相关工程与评测

[多模态检索](https://github.com/Wendy-James/ecommerce-multimodal-retrieval) · [RAG 检索评估](https://github.com/Wendy-James/llm-rag-system) · [Transformer 实验](https://github.com/Wendy-James/transformer-model-lab)

这些项目展示公开离线实验与复现能力，**不冒充内部生产部署或其他开源项目的原创成果**。

## 研究与工程原则

**研究问题 → Baseline → 实现 → 测试 → 受控对照 → 失败分析 → 可复现证据。**

- **证据优先：** 区分已完成、实验草稿、私有研究及未来计划。
- **重视评测可信度：** 检查 Verifier 分歧、奖励失效、数据切分与不确定性。
- **优先复用成熟开源：** 正确标注来源、许可与他人贡献，不为重复造轮子投入算力。
- **严守公开边界：** 不公开公司资产、私有数据、内部指标、密钥、未公开论文或个人身份线索。

---

[公开发布原则](PUBLICATION_POLICY.md) · [作品集维护规范](PORTFOLIO_MAINTENANCE.md) · [研究作品集](https://wendy-james.github.io/)

<sub>公开证据核验日期：2026-10-22。项目路线图不等于已完成成果。</sub>
