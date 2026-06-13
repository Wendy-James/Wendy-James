# Wendy Zhan / 詹文婷

**推荐算法实习生｜搜索召回｜内容理解检索**  
**Recommendation · Retrieval · Ranking · Multimodal Search**

I am preparing for algorithm internship roles around **recommendation/search retrieval, ranking evaluation, and content understanding**. This profile is organized as a resume evidence chain: every core repository should have a clear scenario, pseudo data schema, runnable scripts, experiment tables, badcase records, and interview-safe boundaries.

**Target roles:** Recommendation Algorithm Intern · Search/Recommendation Intern · Content Recommendation Intern · Machine Learning Intern

<p>
  <a href="https://github.com/Wendy-James"><img alt="GitHub" src="https://img.shields.io/badge/GitHub-Wendy--James-24292f?style=flat-square&logo=github&logoColor=white"></a>
  <a href="https://Wendy-James.github.io/"><img alt="Portfolio" src="https://img.shields.io/badge/Portfolio-GitHub%20Pages-0969da?style=flat-square"></a>
  <a href="mailto:1563887189@qq.com"><img alt="Email" src="https://img.shields.io/badge/Email-1563887189%40qq.com-0f766e?style=flat-square"></a>
</p>

## Positioning

My main line is **recommendation/search recall and ranking**, not a scattered AI-app portfolio.

- **Primary project:** short-video recommendation reproduction, Two-Tower recall, Faiss top-k retrieval, time split, Recall@50/NDCG@50, leakage check.
- **Supporting internship evidence:** e-commerce multimodal retrieval, CLIP-style dual encoder, hard negatives, SKU conflict and OCR-noise badcases.
- **Supporting retrieval project:** job knowledge-base RAG evaluation, BM25 + Dense + Reranker, Recall@5/MRR/citation hit rate.
- **Lower-priority work:** backend, document workflow, and frontend demos are kept only as engineering support.

## Core Evidence Repositories

| Priority | Repository | What it supports | Metrics / evidence to inspect | Interview boundary |
|---|---|---|---|---|
| 1 | [short-video-recsys-reproduce](https://github.com/Wendy-James/short-video-recsys-reproduce) | ByteDance-oriented recommendation recall/ranking project | `data_schema.md`, `experiments/metrics.csv`, `experiments/ablation.csv`, `badcases/badcase_samples.csv`; Recall@50 `0.112 -> 0.126`, NDCG@50 `0.071 -> 0.079`, tail Recall@50 `0.058 -> 0.071` | Offline reproduction on pseudo/public-field schema; no company data, no online A/B claim |
| 2 | [ecommerce-multimodal-retrieval](https://github.com/Wendy-James/ecommerce-multimodal-retrieval) | E-commerce content understanding and similar-product retrieval | `data_schema.md`, `experiments.csv`, `badcases.csv`; CLIP-style retrieval, hard negatives, SKU conflict buckets, OCR noise cases | Offline review/evaluation set; not full production owner |
| 3 | [llm-rag-system](https://github.com/Wendy-James/llm-rag-system) | Retrieval evaluation supplement for RAG/search ability | `docs/data_schema.md`, `experiments/retrieval_metrics.csv`, `experiments/chunk_size_ablation.csv`, `badcases/error_analysis.csv`; Recall@5 `0.71 -> 0.77` with reranking | Supporting project only; not positioned as large-model training |
| 4 | [ctr-ranking-lab](https://github.com/Wendy-James/ctr-ranking-lab) | Ranking fundamentals and feature/evaluation practice | CTR features, AUC/LogLoss, feature crossing, experiment tracking | Fundamentals repo, not the main resume project |

## Main Interview Story

If asked "which project is your strongest?", I will start from **short-video recommendation reproduction**:

1. **Scenario:** a recommendation recall module needs to retrieve candidate videos from exposure-level logs before ranking.
2. **Data口径:** pseudo/public-field schema inspired by KuaiRec/KuaiRand/Tenrec: user, item/video, exposure, click, finish, like, favorite, dwell time, author, category, timestamp.
3. **Split:** 7-day train / 1-day validation time split; random split is recorded only as a leakage-risk comparison.
4. **Model:** Two-Tower/DSSM recall baseline with user history, category preference, author interaction, item/category/author embeddings, and time features.
5. **Retrieval:** Faiss-style `IndexFlatIP` top-k retrieval for offline scale.
6. **Metrics:** Recall@50, NDCG@50, AUC, tail Recall@50, plus ablation and badcase analysis.

## Skills That Match The Evidence

| Area | Concrete evidence |
|---|---|
| Recommendation / Search | Two-Tower, DSSM, negative sampling, time split, Faiss, Recall@K, NDCG@K |
| Ranking / Evaluation | AUC, LogLoss, feature crossing, ablation records, leakage checks, tail recall |
| Multimodal Retrieval | CLIP dual encoder, hard negative mining, SKU conflict analysis, OCR-noise false positives |
| RAG Retrieval Support | BM25, dense retrieval, RRF, reranker, chunk-size ablation, citation hit rate |
| Engineering | Python, PyTorch-style training scripts, SQL/data schema thinking, Git, Linux, reproducible experiment logs |

## What This Profile Does Not Claim

- No private company data is published.
- No online ownership or production A/B lift is claimed.
- RAG is a retrieval-evaluation supplement, not my main large-model training direction.
- The profile is intentionally narrowed to **recommendation/search/content retrieval** for algorithm internship interviews.

## Links

- Portfolio: [https://Wendy-James.github.io/](https://Wendy-James.github.io/)
- Algorithm profile roadmap: [docs/ALGORITHM_PROFILE_PLAN.md](https://github.com/Wendy-James/Wendy-James/blob/main/docs/ALGORITHM_PROFILE_PLAN.md)
- Resume project descriptions: [docs/RESUME_PROJECT_DESCRIPTIONS.md](https://github.com/Wendy-James/Wendy-James/blob/main/docs/RESUME_PROJECT_DESCRIPTIONS.md)
- Chinese resume project descriptions: [docs/RESUME_PROJECT_DESCRIPTIONS.zh-CN.md](https://github.com/Wendy-James/Wendy-James/blob/main/docs/RESUME_PROJECT_DESCRIPTIONS.zh-CN.md)

## GitHub Stats

<p>
  <img height="165" alt="GitHub Stats" src="https://github-readme-stats.vercel.app/api?username=Wendy-James&show_icons=true&hide_border=true&theme=default">
  <img height="165" alt="Top Languages" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Wendy-James&layout=compact&hide_border=true&theme=default">
</p>
