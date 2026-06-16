# Wendy Zhan / 詹文婷

**Recommendation Algorithm Intern | Search & Retrieval | Content Understanding**

HFUT 211 · Information and Computing Science  
Incoming MSc Computer Science Admit  
Focus: Recommendation / Retrieval / Ranking / Offline Evaluation

I build reproducible algorithm projects around recommendation/search retrieval, ranking evaluation, and content understanding. The featured repositories keep clear scenarios, data schemas, runnable scripts, experiment tables, badcase records, and data-boundary notes.

**Target roles:** Recommendation Algorithm Intern · Search/Recommendation Intern · Content Recommendation Intern · Machine Learning Intern

<p>
  <a href="https://github.com/Wendy-James"><img alt="GitHub" src="https://img.shields.io/badge/GitHub-Wendy--James-24292f?style=flat-square&logo=github&logoColor=white"></a>
  <a href="https://Wendy-James.github.io/"><img alt="Portfolio" src="https://img.shields.io/badge/Portfolio-GitHub%20Pages-0969da?style=flat-square"></a>
  <a href="mailto:1563887189@qq.com"><img alt="Email" src="https://img.shields.io/badge/Email-1563887189%40qq.com-0f766e?style=flat-square"></a>
</p>

## Focus

I focus on **recommendation / search / retrieval**:

1. **Short-video recommendation:** Two-Tower recall, Faiss TopK, time split, Recall@K / NDCG@K, ablation and leakage check.
2. **E-commerce multimodal retrieval:** CLIP-style image-text retrieval, hard negatives, SKU conflict and OCR-noise badcases.
3. **RAG retrieval evaluation:** BM25 + Dense + Reranker, evidence citation, no-answer control and chunk ablation.

## Featured Projects

| Order | Repository | Keywords | Evidence / metrics | Scope |
|---|---|---|---|---|
| 1 | [short-video-recsys-reproduce](https://github.com/Wendy-James/short-video-recsys-reproduce) | Two-Tower Recall / Faiss / Time Split / Recall@50 / NDCG@50 | `data_schema.md`, `experiments/metrics.csv`, `experiments/ablation.csv`, `badcases/badcase_samples.csv`; Recall@50 `0.112 -> 0.126`, NDCG@50 `0.071 -> 0.079` | Offline recall evaluation |
| 2 | [ecommerce-multimodal-retrieval](https://github.com/Wendy-James/ecommerce-multimodal-retrieval) | CLIP-style Retrieval / Hard Negative / SKU Conflict / Faiss / Badcase Analysis | `data_schema.md`, `experiments.csv`, `badcases.csv`; SKU conflict buckets, OCR noise cases, threshold review | E-commerce retrieval evaluation |
| 3 | [llm-rag-system](https://github.com/Wendy-James/llm-rag-system) | BM25 / Dense Retrieval / Reranker / Recall@K / Citation Evaluation | `docs/data_schema.md`, `experiments/retrieval_metrics.csv`, `experiments/chunk_size_ablation.csv`, `badcases/error_analysis.csv`; Recall@5 `0.71 -> 0.77` | Retrieval-evaluation supplement |

## Repository Focus

The profile should be scanned through these pinned repositories, in this order:

1. `short-video-recsys-reproduce`
2. `ecommerce-multimodal-retrieval`
3. `llm-rag-system`
4. `recommendation-system`
5. `transformer-model-lab`
6. `open-source-reading-notes`

Other frontend, static-site, course-template, or admin-dashboard practice repositories are not part of the algorithm interview story. They can stay public, but they should not be pinned or introduced before the recommendation/search/retrieval projects.

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

## Data Boundary

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
