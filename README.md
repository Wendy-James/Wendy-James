<div align="center">

# Wendy

### Building verifiable learning systems

**LLM Post-training × Agentic RL · Foundation-model Training Systems**

Interested in how language-model agents learn from **verifiable feedback, tool interaction, and multi-step environments**. I work toward rigorous post-training experiments backed by reproducible implementations, evaluation protocols, and honest failure analysis.

[Research portfolio ↗](https://wendy-james.github.io/) &nbsp;·&nbsp; [中文](README.zh-CN.md) &nbsp;·&nbsp; [Public evidence ↓](#public-engineering-evidence)

</div>

---

## Research focus

**North star: Post-training × Agentic Reinforcement Learning.** The goal is to understand how reward quality, verifiers, data recipes, and environment design affect the learning and generalization of tool-using language-model agents.

| Area | Technical questions | Status |
| :--- | :--- | :--- |
| **Verifiable feedback** | Answer extraction, verifier agreement, false rewards, reward hacking | Research in progress; code and intermediate results private |
| **SFT → RLVR** | Data selection, difficulty, controlled baselines, fixed-compute comparisons | Experiments under investigation; no public RL gain claim |
| **Tool-using agents** | Multi-step tasks, trajectory-level evaluation, environment feedback | **Planned research direction**, not a shipped agent |
| **Training systems** | Tokenization, decoder components, testing, optimization and profiling | Public WendyFM evidence below |

These are **research questions and engineering priorities**, not claims of a published paper, completed Agentic RL training, or frontier-model performance.

## Public engineering evidence

### 01 / [WendyFM — Foundation-model systems](https://github.com/Wendy-James/wendy-foundation-model)

A from-scratch training-systems lab organized around **implementation → correctness tests → reproducible measurement → limitations**.

**Completed and publicly inspectable:** deterministic byte-level BPE tokenizer; naive and indexed trainers; multilingual differential tests; CPU-local synthetic benchmarks.

| Benchmark corpus | Indexed vs. naive trainer |
| :--- | ---: |
| English | **7.25×** |
| Code | **4.55×** |
| Mixed multilingual | **4.57×** |
| Chinese | **0.70× — slower** |

The indexed trainer matched tokenizer specifications in the tested cases but used more tracked Python allocations. Results are **small synthetic CPU benchmarks**, not model pretraining or production throughput.

[Technical report](https://github.com/Wendy-James/wendy-foundation-model/blob/main/report/tokenizer.md) · [Measurements](https://github.com/Wendy-James/wendy-foundation-model/blob/main/benchmarks/tokenizer/results.csv) · [Reproduction instructions](https://github.com/Wendy-James/wendy-foundation-model#reproduce-the-tokenizer-milestone)

**Work in progress:** [Decoder-only Transformer M2 draft, PR #24](https://github.com/Wendy-James/wendy-foundation-model/pull/24). Isolated toy CPU smoke tests were reported in the draft; the PR is **not merged**, and real pretraining, independent review, and GPU profiling are not claimed.

### 02 / [Recommendation retrieval & evaluation](https://github.com/Wendy-James/short-video-recsys-reproduce)

A publicly inspectable **offline reproduction**, covering Two-Tower/DSSM retrieval, negative sampling, temporal holdouts, TopK metrics, ablations, and leakage checks.

On the repository's **pseudo/anonymized offline dataset**, reported time-split Recall@50 moves from **0.112 to 0.126** across the documented configurations. This is **not** an online experiment or evidence of an employer's business improvement.

[Experiment evidence](https://github.com/Wendy-James/short-video-recsys-reproduce/tree/main/evidence_pack) · [Ablations](https://github.com/Wendy-James/short-video-recsys-reproduce/blob/main/experiments/ablation.csv)

### 03 / Related systems and evaluation

[Multimodal retrieval](https://github.com/Wendy-James/ecommerce-multimodal-retrieval) · [RAG retrieval evaluation](https://github.com/Wendy-James/llm-rag-system) · [Transformer experiments](https://github.com/Wendy-James/transformer-model-lab)

These supporting repositories show **offline experiments or reproductions**; they are not presented as proprietary deployments or original contributions to upstream systems.

## How I work

**Question → baseline → implementation → tests → controlled comparison → failure analysis → reproducible evidence.**

- **Evidence over labels.** Separate completed milestones, experimental drafts, private research, and future plans.
- **Verifier and evaluation rigor.** Check disagreement, reward failure modes, split integrity, and uncertainty before interpreting results.
- **Reuse before reinvention.** Build on mature, properly credited open-source tools where that improves validity and speed.
- **Clear publication boundaries.** No employer-owned code, private data, internal metrics, credentials, unpublished manuscripts, or identifying personal details.

---

[Publication policy](PUBLICATION_POLICY.md) · [Portfolio maintenance standards](PORTFOLIO_MAINTENANCE.md) · [Research portfolio](https://wendy-james.github.io/)

<sub>Public evidence reviewed: 2026-10-22. A project roadmap is not a statement of completed work.</sub>
