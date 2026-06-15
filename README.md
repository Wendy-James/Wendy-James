# Wendy Zhan / 詹文婷

**Recommendation Algorithm Intern | Search & Retrieval | Content Understanding**

HFUT 211 · Information and Computing Science  
Incoming MSc Computer Science Admit  
Focus: Recommendation / Retrieval / Ranking / Offline Evaluation

I am preparing for algorithm internship roles around recommendation/search retrieval, ranking evaluation, and content understanding. This profile highlights reproducible algorithm experiments: each featured repository keeps a clear scenario, data schema, runnable scripts, experiment tables, badcase records, and explicit data boundaries.

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

## Featured Projects

| Order | Repository | Keywords | Evidence / metrics | Interview boundary |
|---|---|---|---|---|
| 1 | [short-video-recsys-reproduce](https://github.com/Wendy-James/short-video-recsys-reproduce) | Two-Tower Recall / Faiss / Time Split / Recall@50 / NDCG@50 | `data_schema.md`, `experiments/metrics.csv`, `experiments/ablation.csv`, `badcases/badcase_samples.csv`; Recall@50 `0.112 -> 0.126`, NDCG@50 `0.071 -> 0.079` | Public-field offline reproduction; no company data, no online A/B claim |
| 2 | [ecommerce-multimodal-retrieval](https://github.com/Wendy-James/ecommerce-multimodal-retrieval) | CLIP / Hard Negative / SKU Conflict / Faiss / Badcase Analysis | `data_schema.md`, `experiments.csv`, `badcases.csv`; SKU conflict buckets, OCR noise cases, threshold review | Sanitized public reproduction; not full production owner |
| 3 | [llm-rag-system](https://github.com/Wendy-James/llm-rag-system) | BM25 / Dense Retrieval / Reranker / Recall@K / Citation Evaluation | `docs/data_schema.md`, `experiments/retrieval_metrics.csv`, `experiments/chunk_size_ablation.csv`, `badcases/error_analysis.csv`; Recall@5 `0.71 -> 0.77` | Supporting project only; not positioned as large-model training |
| 4 | [recommendation-system](https://github.com/Wendy-James/recommendation-system) | CTR / Feature Crossing / AUC / LogLoss / nDCG | ranking fundamentals, feature engineering notes, baseline metrics | Basic ranking practice; lower priority than short-video recall |
| 5 | [transformer-model-lab](https://github.com/Wendy-James/transformer-model-lab) | Transformer / Attention / PyTorch / Training Notes | sequence modeling and model-structure practice | Foundation repo; used to support model understanding, not claimed as large-model training |
| 6 | [open-source-reading-notes](https://github.com/Wendy-James/open-source-reading-notes) | Papers / Source Reading / Retrieval / Recommendation Notes | reading notes and implementation checklists | Learning record; supports interview discussion but not a business project |

## Repository Display Rule

The first screen should only show the algorithm line above. Older Vue, HTML e-commerce practice, admin dashboard, document workflow, and generic backend demos are engineering exercises and should stay unpinned or archived so they do not dilute the recommendation/search positioning.

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
