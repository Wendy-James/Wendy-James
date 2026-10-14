<div align="center">

# Wendy

**Foundation Model Systems · LLM Post-training · ML Research Engineering**

Building and evaluating model systems from first principles — with reproducible experiments, measured trade-offs, and honest failure analysis.

B.Sc. Information and Computing Science · Hefei University of Technology · 2026

[**Research portfolio ↗**](https://wendy-james.github.io/) &nbsp;·&nbsp; [中文](README.zh-CN.md) &nbsp;·&nbsp; [Email](mailto:1563887189@qq.com)

</div>

---

## Currently building

| Track | Current focus | Public status |
| :--- | :--- | :--- |
| **Foundation model systems** | Tokenizer → Transformer → training & systems | [WendyFM: tokenizer milestone completed](https://github.com/Wendy-James/wendy-foundation-model) |
| **Post-training research** | Verifier reliability, mathematical difficulty, SFT-to-RL questions | **Ongoing** · research repository private |
| **Applied machine learning** | Time-aware evaluation, retrieval, ranking, ablation | [Offline recommendation reproduction](https://github.com/Wendy-James/short-video-recsys-reproduce) |

## Featured engineering evidence

### 01 / [WendyFM — From-Scratch Foundation Model Systems](https://github.com/Wendy-James/wendy-foundation-model)

**Shipped milestone:** a deterministic byte-level BPE tokenizer with two trainers, multilingual correctness tests, and CPU-local benchmarks.

| English | Code | Mixed multilingual | Chinese |
| :---: | :---: | :---: | :---: |
| **7.25×** faster | **4.55×** faster | **4.57×** faster | **0.70×** (slower) |

*Indexed trainer vs. naive reference on small synthetic corpora. All specifications matched exactly; indexed training had higher tracked Python allocation peaks. These figures are **not** LLM pretraining, GPU, or production results.*

[**Code**](https://github.com/Wendy-James/wendy-foundation-model) · [**Benchmark report**](https://github.com/Wendy-James/wendy-foundation-model/blob/main/report/tokenizer.md) · [**Measurements (CSV)**](https://github.com/Wendy-James/wendy-foundation-model/blob/main/benchmarks/tokenizer/results.csv) · [**Reproduction steps**](https://github.com/Wendy-James/wendy-foundation-model#reproduce-the-tokenizer-milestone)

**Next (planned, not completed):** decoder-only Transformer, end-to-end training/evaluation baseline, GPU and attention profiling, scaling experiments.

### 02 / Post-Training and RL Trainability Research

Exploring how **data selection, difficulty profiling, and answer verification** could influence learning under a fixed compute budget. Current work emphasizes verifier agreement, conservative extraction, and experimental design; SFT/RL findings and publication are **not claimed**.

Research code stays private until validation and release review. This section will be updated only when safe, reproducible findings are ready.

### 03 / [Recommendation Retrieval & Evaluation](https://github.com/Wendy-James/short-video-recsys-reproduce)

A public **offline reproduction** of a Two-Tower/DSSM short-video recall pipeline, with temporal splits, negative sampling, Faiss-style TopK retrieval, ablations, leakage checks, and failure analysis.

Other public evidence: [multimodal retrieval](https://github.com/Wendy-James/ecommerce-multimodal-retrieval) · [RAG retrieval evaluation](https://github.com/Wendy-James/llm-rag-system) · [Transformer model lab](https://github.com/Wendy-James/transformer-model-lab).

## Research practice

**Question → baseline → implementation → tests → measured comparison → limitations.**

I prefer mature, properly credited open-source foundations over unnecessary reinvention. I care about correctness, negative results, clear reproduction commands, and practical engineering constraints — not the number of green squares on a contribution chart.

Industry experience informs my engineering approach, but **employer-owned data, internal model artifacts, implementation details, and private metrics are not portfolio content**. Public sample-based experiments are not presented as online business outcomes.

---

**Interested in discussing foundation models, training systems, reproducible evaluation, or research engineering?** [Get in touch →](mailto:1563887189@qq.com)
