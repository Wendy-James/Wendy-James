<div align="center">

# Wendy

**LLM Post-training × Agentic RL · Foundation Model Systems · Research Engineering**

Exploring how language-model systems learn from verifiable feedback, multi-step decisions, and tool interaction. I build reproducible training and evaluation pipelines, and document both positive and negative results.

**Current focus:** verifiable rewards, agent evaluation, and efficient model-training workflows.

[**Research portfolio ↗**](https://wendy-james.github.io/) &nbsp;·&nbsp; [中文](README.zh-CN.md) &nbsp;·&nbsp; [Selected work ↓](#currently-building)

</div>

---

## Currently building

| Track | Current focus | Public status |
| :--- | :--- | :--- |
| **Foundation model systems** | Tokenizer → Transformer → training & systems | [WendyFM: tokenizer milestone completed](https://github.com/Wendy-James/wendy-foundation-model) |
| **Post-training × Agentic RL** | Verifiable feedback, tool-use evaluation, SFT-to-RL research questions | **Ongoing** · research repository private |
| **Applied machine learning** | Time-aware evaluation, retrieval, ranking, ablation | [Offline recommendation reproduction](https://github.com/Wendy-James/short-video-recsys-reproduce) |

## Featured engineering evidence

### 01 / [WendyFM — From-Scratch Foundation Model Systems](https://github.com/Wendy-James/wendy-foundation-model)

**Shipped milestone:** a deterministic byte-level BPE tokenizer with two trainers, multilingual correctness tests, and CPU-local benchmarks.

| English | Code | Mixed multilingual | Chinese |
| :---: | :---: | :---: | :---: |
| **7.25×** faster | **4.55×** faster | **4.57×** faster | **0.70×** (slower) |

*Indexed trainer vs. naive reference on small synthetic corpora. All specifications matched exactly; indexed training had higher tracked Python allocation peaks. These figures are **not** LLM pretraining, GPU, or production results.*

[**Code**](https://github.com/Wendy-James/wendy-foundation-model) · [**Benchmark report**](https://github.com/Wendy-James/wendy-foundation-model/blob/main/report/tokenizer.md) · [**Measurements (CSV)**](https://github.com/Wendy-James/wendy-foundation-model/blob/main/benchmarks/tokenizer/results.csv) · [**Reproduction steps**](https://github.com/Wendy-James/wendy-foundation-model#reproduce-the-tokenizer-milestone)

**Next (not yet completed):** [Decoder-only Transformer engineering draft — PR #24](https://github.com/Wendy-James/wendy-foundation-model/pull/24) has passed isolated toy CPU smoke tests and awaits owner review, environment reproducibility checks, and real training/evaluation. GPU/attention profiling and scaling remain planned.

### 02 / Post-training × Agentic RL Research

Current investigations cover **verifier reliability, data selection, mathematical reasoning evaluation, and SFT-to-RL experimental design**. Longer-term questions include tool-use rewards, multi-step environments, and agentic RL. These are research directions, **not claims of completed agent training, validated RL gains, or publication**.

Research code stays private until validation and release review. This section will be updated only when safe, reproducible findings are ready.

### 03 / [Recommendation Retrieval & Evaluation](https://github.com/Wendy-James/short-video-recsys-reproduce)

A public **offline reproduction** of a Two-Tower/DSSM short-video recall pipeline, with temporal splits, negative sampling, Faiss-style TopK retrieval, ablations, leakage checks, and failure analysis.

Other public evidence: [multimodal retrieval](https://github.com/Wendy-James/ecommerce-multimodal-retrieval) · [RAG retrieval evaluation](https://github.com/Wendy-James/llm-rag-system) · [Transformer model lab](https://github.com/Wendy-James/transformer-model-lab).

## Research practice

**Question → baseline → implementation → tests → measured comparison → limitations.**

I prefer mature, properly credited open-source foundations over unnecessary reinvention. I care about correctness, negative results, clear reproduction commands, and practical engineering constraints — not the number of green squares on a contribution chart.

Industry experience informs my engineering approach, but **employer-owned data, internal model artifacts, implementation details, and private metrics are not portfolio content**. Public sample-based experiments are not presented as online business outcomes.

---

[Responsible publication policy](PUBLICATION_POLICY.md) · **Public projects, evidence, and reproduction instructions are linked above.**
