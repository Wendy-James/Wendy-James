# 中文简历项目描述

> 目标岗位：AI算法实习生、机器学习算法实习生、大模型算法实习生、推荐算法实习生、Agent / AIGC 实习生  
> GitHub主页：https://github.com/Wendy-James

本文档用于将 GitHub 精选项目转化为中文简历可直接使用的项目描述。表述尽量突出算法设计、模型理解、实验指标和工程实现，同时避免超过公开仓库证据的夸大描述。

## 1. LLM RAG System

项目链接：https://github.com/Wendy-James/llm-rag-system

### 1行版本

- 构建 Hybrid RAG 检索系统，实现 BM25、稠密检索基线、Query Rewrite、RRF 多路融合、Reranker，并使用 Recall/MRR/nDCG 评估检索质量。

### 3行版本

- 设计可复现的 RAG 检索链路，覆盖本地语料加载、标注查询集、BM25 稀疏召回、稠密检索基线、Query Rewrite、RRF 融合和 Reranker 重排。
- 实现 CLI 运行与实验结果导出，使用 Recall@3、MRR@3、nDCG@3 衡量检索效果，并补充中英文 README、架构图、算法文档和面试讲解文档。
- 将单路检索升级为多路混合召回 + 重排流程，突出 RAG 系统中检索质量优化、工程可复现和可解释评估能力。

### STAR 面试讲解版

Situation：单路 RAG 检索在面对技术关键词、缩写和语义改写时容易漏召回相关证据。

Task：构建一个可评估的检索实验系统，用于对比稀疏检索、稠密检索、多路融合和重排策略。

Action：实现 BM25、稠密检索基线、Query Rewrite、RRF 融合、Lexical Reranker、CLI 运行入口和 Recall/MRR/nDCG 指标导出。

Result：完成可运行的 RAG 检索项目，具备实验指标、架构说明、算法文档和后续扩展到 Embedding、FAISS、Cross-Encoder Reranker 的路线。

## 2. Multi-Agent Assistant

项目链接：https://github.com/Wendy-James/multi-agent-assistant

### 1行版本

- 构建本地多Agent研究助手，实现 Planner、Researcher、Writer、Verifier、Summarizer 多角色协作、状态图流转、工具调用日志和验证指标。

### 3行版本

- 将 Agent 工作流建模为显式状态图，拆分 Planner、Researcher、Writer、Verifier、Summarizer 等角色，提升流程可观测性和可维护性。
- 实现本地工具调用、轻量记忆、Verifier 反馈、CLI 运行和 CSV/JSON 执行轨迹导出，用于分析工具调用与任务完成情况。
- 补充架构设计、角色职责、工具调用日志、可靠性指标和面试讲解文档，体现 Agent 系统工程化和多智能体协作理解。

### STAR 面试讲解版

Situation：Agent 系统如果把规划、工具调用、记忆和验证都混在单一循环里，容易出现难调试、难复现的问题。

Task：构建一个本地可运行的多Agent工作流，将角色职责拆开，并记录完整执行轨迹。

Action：实现 Planner / Researcher / Writer / Verifier / Summarizer 状态图，加入本地工具注册、轻量记忆、验证环节、CLI 运行和 trace 导出。

Result：完成可解释的 Agent 项目，能够讲清状态管理、工具调用可观测性、Verifier 可靠性控制，以及向 LangGraph / MCP 工具体系扩展的路径。

## 3. Recommendation System

项目链接：https://github.com/Wendy-James/recommendation-system

### 1行版本

- 构建 CTR 预估与排序实验系统，实现特征工程、特征交叉、Logistic Regression、GBDT 风格基线，并使用 AUC、LogLoss、nDCG@5 评估。

### 3行版本

- 设计可复现 CTR 实验流程，包含合成曝光数据、类别/数值特征编码、category-device 特征交叉、训练/验证切分和实验结果导出。
- 对比 Logistic Regression 与轻量 GBDT 风格 Stump Boosting 基线，使用 AUC、LogLoss 和用户级 nDCG@5 同时评估点击预测和排序质量。
- 生成 CSV/JSON 实验结果，并补充模型假设、特征设计、指标解释、系统架构和面试问题文档。

### STAR 面试讲解版

Situation：推荐排序既需要准确预估点击概率，也需要保证 Top-K 排序质量。

Task：构建一个 CTR 实验项目，体现特征工程、模型对比和排序指标评估能力。

Action：实现曝光数据生成、特征编码、特征交叉、Logistic Regression、Stump Boosting、AUC、LogLoss、nDCG@5、CLI 运行和实验报告。

Result：完成推荐算法项目，能够展示机器学习工程能力、CTR 指标理解和后续扩展到 LightGBM、XGBoost、CatBoost、DeepFM、xDeepFM 的路线。

## 4. Transformer Model Lab

项目链接：https://github.com/Wendy-James/transformer-model-lab

### 1行版本

- 构建轻量 Transformer 模型实验，实现分词、Embedding、Q/K/V Self-Attention、分类器训练、阈值校准和 Attention Trace 导出。

### 3行版本

- 从源码层面实现 Transformer 前向路径，覆盖词表编码、Token Embedding、Q/K/V projection、`[CLS]` Self-Attention Pooling、Sigmoid 分类器和指标评估。
- 搭建可运行实验流程，输出 Accuracy、F1、Threshold Calibration 和 Attention Trace，并补充中英文 README、架构图、算法原理和面试讲解文档。
- 将项目定位为模型理解训练，后续可扩展到 PyTorch Transformer、BERT Fine-tuning、LoRA 参数高效微调和 Attention 可视化。

### STAR 面试讲解版

Situation：很多 Transformer 项目只调用预训练模型 API，面试时难以解释模型内部路径。

Task：构建一个小型可运行项目，展示 token id 如何经过 embedding、attention、pooling 和 classifier 形成分类结果。

Action：实现分词、Embedding Lookup、Q/K/V projection、Scaled Dot-Product Attention、分类器训练、阈值校准、指标评估和 Attention Trace 导出。

Result：完成深度学习模型理解项目，能够讲清 Transformer 前向计算路径，并为 BERT 微调和参数高效微调实验打基础。

## 5. Time Series Forecast

项目链接：https://github.com/Wendy-James/time-series-forecast

### 1行版本

- 构建时间序列预测与异常检测实验，实现 Moving Average、Trend Seasonal 基线、残差阈值检测，并使用 MAE、RMSE、MAPE、Anomaly F1 评估。

### 3行版本

- 设计可复现时间序列实验流程，包含趋势 + 周期性数据生成、训练/验证切分、Moving Average 预测、Trend Seasonal 预测和残差分析。
- 基于预测残差实现阈值异常检测，使用 MAE、RMSE、MAPE、F1 同时评估预测误差和异常检测效果，并导出 CSV/JSON 实验结果。
- 补充架构图、算法原理、实验记录、优化方案和面试问答，体现数据挖掘、时间序列建模和监控场景理解。

### STAR 面试讲解版

Situation：时间序列监控场景既需要预测未来趋势，也需要及时发现异常波动。

Task：构建一个可复现的数据挖掘项目，对比预测基线，并将预测残差转化为异常告警。

Action：实现合成数据生成、Moving Average、Trend Seasonal、残差阈值检测、MAE/RMSE/MAPE/F1 指标、CLI 运行和实验报告导出。

Result：完成时间序列预测项目，能够讲清趋势/周期性建模、残差异常检测、指标选择，并可扩展到滚动回测和 Transformer Forecasting。

## 6. Document Intelligence

项目链接：https://github.com/Wendy-James/project-briefs/tree/main/case-studies/adaptive-document-structuring-model

### 1行版本

- 参与文档智能研究项目，围绕结构化信息抽取、Schema 设计、验证规则和多场景文档理解构建分析方案。

### 3行版本

- 设计文档结构化流程，将非结构化内容映射到场景化字段、Schema 和验证规则。
- 分析不同文档类型的抽取需求，梳理系统边界、数据流、可解释输出和结构化结果格式。
- 输出公开项目材料，体现信息抽取、文档理解、结构设计和 AI 应用流程拆解能力。

### STAR 面试讲解版

Situation：文档密集型业务需要将非结构化文本转化为可靠的结构化字段。

Task：设计一个面向多场景的文档智能工作流，使抽取结果可验证、可解释。

Action：定义 Schema、抽取字段、验证规则、场景需求和结构化输出形式。

Result：形成文档智能项目说明，能够展示文档理解、结构化抽取和 AI 工作流设计能力。

## 7. AI Job Application Agent

项目链接：https://github.com/Wendy-James/project-briefs/tree/main/case-studies/ai-career-interview-system

### 1行版本

- 设计 AI 求职申请工作流，覆盖 JD 解析、候选人匹配、简历草稿生成和面试准备，并保留人工审核环节。

### 3行版本

- 设计 JD 解析、候选人画像结构化、岗位要求匹配、定制化简历生成和面试问题生成流程。
- 规划 FastAPI、PostgreSQL、Redis、Celery、Docker、LLM 工作流模块和 LaTeX 简历生成等后端架构。
- 梳理系统边界、人工审核节点、数据流转和工程模块，体现 LLM 应用工作流和后端工程设计能力。

### STAR 面试讲解版

Situation：技术岗位申请需要反复将岗位要求映射到个人经历，并生成针对性材料。

Task：设计一个结构化、可审核的 AI 求职工作流，辅助 JD 匹配、简历生成和面试准备。

Action：拆分 JD 解析、画像结构化、要求匹配、简历生成、面试题生成和人工审核模块。

Result：形成清晰的 AI 应用系统设计，展示 LLM 工作流设计、后端架构规划和产品化工程思维。

## 简历 GitHub 链接写法

推荐放入简历：

```text
GitHub: https://github.com/Wendy-James
```

推荐个人简介补充：

```text
GitHub 项目组合覆盖 LLM/RAG、Agent 工作流、CTR 排序、推荐算法、Transformer 模型理解和时间序列预测。
```

