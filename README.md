# Wendy Zhan (詹文婷)

**Foundation Models · LLM Post-training · ML Research Engineering**  
B.Sc. in Information and Computing Science, Hefei University of Technology (2026)

I'm interested in understanding **how models are trained, evaluated, and improved**, from reproducible systems components to verifiable reasoning experiments. My work emphasizes *correctness, measured trade-offs, and inspectable evidence* over broad technology claims.

[中文简介](README.zh-CN.md) · [GitHub](https://github.com/Wendy-James) · [Email](mailto:1563887189@qq.com)

---

## Research & engineering

### 01 · [WendyFM — foundation-model training from first principles](https://github.com/Wendy-James/wendy-foundation-model)

Building an educational, from-scratch language-model training stack, one reproducible milestone at a time.

**Completed: byte-level BPE tokenizer**
- Implemented deterministic byte-level BPE with special-token handling and multilingual pre-tokenization.
- Checked *exact equality* between naive and indexed training outputs before benchmarking.
- In small **synthetic CPU benchmarks**, the indexed trainer reached **7.25×** naive speed on English, **4.55×** on code, and **4.57×** on mixed text, but only **0.70×** on Chinese and with higher measured Python allocations.
- **Evidence:** [technical report](https://github.com/Wendy-James/wendy-foundation-model/blob/main/report/tokenizer.md) · [benchmark CSV](https://github.com/Wendy-James/wendy-foundation-model/blob/main/benchmarks/tokenizer/results.csv) · [source repository](https://github.com/Wendy-James/wendy-foundation-model)

**Next milestones (planned, not yet completed):** decoder-only Transformer, training loop and evaluation, attention and GPU profiling, and scaling experiments.

### 02 · LLM post-training & RL trainability — research in progress

Exploring **data selection × supervised fine-tuning × verifiable rewards / evaluation**: which examples and verification choices might lead to useful learning under a fixed compute budget?

- Current emphasis: rigorous math-answer extraction, verifier agreement, difficulty profiling, and experimental controls.
- Research code is **private** while the study is underway. No publication, publicly reproducible RL result, or completed large-scale training is claimed here.
- Public methods, results, or code will be linked **only after verification and release review**.

## Selected public projects

| Project | Focus | What the public repository actually demonstrates |
| --- | --- | --- |
| **[WendyFM](https://github.com/Wendy-James/wendy-foundation-model)** | Tokenization and foundation-model systems | Completed tokenizer milestone, differential checks, measured gains *and regressions* |
| [Short-video recommender reproduction](https://github.com/Wendy-James/short-video-recsys-reproduce) | Two-Tower retrieval, negative sampling, temporal validation | Reproducible **offline** evaluation on pseudo/anonymized data; no online A/B claims |
| [Multimodal product retrieval](https://github.com/Wendy-James/ecommerce-multimodal-retrieval) | Image–text retrieval and hard-negative analysis | Offline retrieval experiments, SKU/OCR failure cases |
| [RAG retrieval evaluation](https://github.com/Wendy-James/llm-rag-system) | BM25, dense retrieval, reranking, ablation | A supporting evaluation project, **not** evidence of LLM pretraining |

## How I approach research

**Question → baseline → implementation → tests → controlled experiments → limitations.**

I prefer to reuse and credit mature open-source work, check licenses and reproducibility, and measure changes before claiming improvements. Negative results and failure modes belong alongside successful experiments.

My longer-term interests include **foundation-model research, training infrastructure, and translating research into useful AI systems**. These are directions of interest—not achievements or company affiliations.

---

**Research/engineering discussions:** [Email me](mailto:1563887189@qq.com).  
*Public projects use shareable or synthetic data. No employer code, internal datasets, private metrics, or credentials are intentionally published.*
