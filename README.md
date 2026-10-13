# Wendy Zhan · Foundation Models & ML Research Engineering

**B.Sc. in Information and Computing Science, Hefei University of Technology (2026)**  
Interested in **foundation-model training, post-training, verifiable evaluation, and ML systems**.

I build experiments that can be inspected and reproduced: **implementation → correctness checks → benchmarks → failure analysis**. My current emphasis is on understanding the training stack, not just calling hosted model APIs.

## Currently building

### [WendyFM — foundation-model training from first principles](https://github.com/Wendy-James/wendy-foundation-model)

An incremental, from-scratch implementation of language-model training components.

**Completed and documented: byte-level BPE tokenizer (Milestone 1).**
- Deterministic merge selection, Unicode-aware pre-tokenization, and special-token handling.
- Naive and indexed trainers checked for **exact specification equality** across test cases.
- On small, synthetic, CPU-local benchmarks, the indexed trainer was **7.25× faster on English**, **4.55× on code**, and **4.57× on mixed text**; it was **slower on Chinese (0.70×)** and used more measured Python allocations.
- [Technical report and limitations](https://github.com/Wendy-James/wendy-foundation-model/blob/main/report/tokenizer.md) · [Benchmark data](https://github.com/Wendy-James/wendy-foundation-model/blob/main/benchmarks/tokenizer/results.csv)

**Planned next:** decoder-only Transformer, RoPE/RMSNorm/SwiGLU, pretraining experiments, evaluation, GPU profiling, and training-system scaling. These are roadmap items, **not completed results**.

### LLM post-training research — work in progress

Investigating how **SFT data selection, automatic verification, and RL trainability** interact under controlled evaluation budgets. The research repository is currently private. I am **not claiming completed SFT/RL training, a publication, or publicly reproducible findings** at this stage.

## Selected public engineering projects

| Project | What to inspect | Evidence boundary |
| --- | --- | --- |
| **[WendyFM](https://github.com/Wendy-James/wendy-foundation-model)** | Tokenizer implementation, differential tests, benchmark report, limitations | Completed tokenizer milestone; the broader training stack is planned |
| **[Short-video recommendation reproduction](https://github.com/Wendy-James/short-video-recsys-reproduce)** | Two-Tower retrieval, time-based split, negative sampling, Recall@50 / NDCG@50, ablations | Offline reproduction on pseudo/anonymized data; no production lift claim |
| **[E-commerce multimodal retrieval](https://github.com/Wendy-James/ecommerce-multimodal-retrieval)** | Image–text retrieval, hard negatives, SKU/OCR bad-case analysis | Public evaluation exercise, not an online production system |
| [RAG retrieval evaluation](https://github.com/Wendy-James/llm-rag-system) | BM25 + dense retrieval, reranking, retrieval metrics and chunk-size ablation | Supporting retrieval project, not LLM pretraining |

## Research & engineering principles

- **Start from a baseline:** define the task, data boundary, metric, and expected failure modes.
- **Prefer reproducibility over claims:** keep runnable commands, test cases, configurations, experiment tables, and negative results.
- **Reuse open source responsibly:** inspect licenses and maintenance; cite original authors; adapt rather than rebuild without a reason.
- **Separate evidence from ambition:** label prototypes, offline experiments, and future milestones clearly.
- **Respect data boundaries:** no employer source code, internal metrics, private user data, credentials, or production artifacts in public repositories.

## Contact

[GitHub](https://github.com/Wendy-James) · [Email](mailto:1563887189@qq.com)

*Open to conversations about foundation-model research engineering, training systems, and reproducible ML experimentation.*
