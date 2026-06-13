# Wendy Zhan / 詹文婷

**推荐算法 / 搜索召回 / 内容理解**  
**Recommendation · Retrieval · Ranking · Multimodal Search**

I am preparing for algorithm internship roles with a focus on recommendation, retrieval, ranking, and content understanding. My GitHub is being reorganized as an evidence chain for resume projects: clear README, pseudo data schema, runnable scripts, experiment logs, and badcase analysis.

**Target roles:** Recommendation Algorithm Intern · Search/Recommendation Intern · Content Recommendation Intern · Machine Learning Intern

<p>
  <a href="https://github.com/Wendy-James"><img alt="GitHub" src="https://img.shields.io/badge/GitHub-Wendy--James-24292f?style=flat-square&logo=github&logoColor=white"></a>
  <a href="https://Wendy-James.github.io/"><img alt="Portfolio" src="https://img.shields.io/badge/Portfolio-GitHub%20Pages-0969da?style=flat-square"></a>
  <a href="mailto:1563887189@qq.com"><img alt="Email" src="https://img.shields.io/badge/Email-1563887189%40qq.com-0f766e?style=flat-square"></a>
</p>

## Main Direction

- **Recommendation / Retrieval:** Two-Tower, DSSM, negative sampling, Faiss, Recall@K, NDCG@K.
- **Ranking / Evaluation:** AUC, feature crossing, time-based split, leakage checks, ablation records.
- **Content Understanding:** CLIP-style image-text retrieval, hard negative mining, SKU conflict analysis.
- **RAG as Support:** BM25 + Dense + Reranker, evidence recall, MRR, citation hit rate.

## Featured Evidence Repositories

| Repository | Focus | Evidence |
|---|---|---|
| [short-video-recsys-reproduce](https://github.com/Wendy-James/short-video-recsys-reproduce) | Short-video recommendation, Two-Tower retrieval, Faiss top-k recall | `README`, `data_schema.md`, `experiments.csv`, `badcases.csv`, training/evaluation scripts |
| [ecommerce-multimodal-retrieval](https://github.com/Wendy-James/ecommerce-multimodal-retrieval) | E-commerce image-text retrieval, CLIP dual encoder, hard negatives | SKU conflict buckets, OCR noise cases, retrieval metrics, badcase examples |
| [hybrid-rag-lab](https://github.com/Wendy-James/hybrid-rag-lab) | Retrieval evaluation support | BM25 + Dense + Reranker, Recall@K, MRR, citation hit rate |
| [ctr-ranking-lab](https://github.com/Wendy-James/ctr-ranking-lab) | Ranking fundamentals | CTR features, AUC/LogLoss, feature crossing, experiment tracking |

## Current Interview Story

My main project is **short-video recommendation reproduction**:

- Build exposure-level samples with click, finish, like, favorite, dwell time, author, category, and timestamp fields.
- Use **7-day train / 1-day validation time split** instead of random split to reduce leakage.
- Train a **Two-Tower retrieval baseline** and evaluate with **Recall@50, NDCG@50, AUC, tail Recall@50**.
- Use **Faiss IndexFlatIP** for exact inner-product retrieval at offline scale.
- Keep `experiments.csv` and `badcases.csv` to explain metric changes and failure cases.

The e-commerce multimodal retrieval project is a supporting evidence chain for content understanding and similar-product retrieval. RAG is only a retrieval-evaluation supplement, not the main positioning.

## Core Skills

| Area | Skills |
|---|---|
| Recommendation / Search | Two-Tower, DSSM, recall, ranking, reranking, cold start, offline evaluation |
| Metrics | Recall@K, NDCG@K, AUC, LogLoss, MRR, citation hit rate |
| Multimodal Retrieval | CLIP dual encoder, hard negative mining, SKU conflict analysis, Faiss |
| Engineering | Python, PyTorch, SQL, Git, Linux, experiment tracking |
| RAG Support | BM25, dense retrieval, reranker, chunk evaluation, evidence citation |

## Project Standards

Each core project should include:

- project background and value
- pseudo/anonymized data schema
- runnable training or evaluation commands
- experiment results in `experiments.csv`
- badcase examples in `badcases.csv`
- interview questions and STAR-style explanation

## Links

- GitHub: [https://github.com/Wendy-James](https://github.com/Wendy-James)
- Portfolio: [https://Wendy-James.github.io/](https://Wendy-James.github.io/)
- Algorithm profile roadmap: [docs/ALGORITHM_PROFILE_PLAN.md](https://github.com/Wendy-James/Wendy-James/blob/main/docs/ALGORITHM_PROFILE_PLAN.md)
- Resume project descriptions: [docs/RESUME_PROJECT_DESCRIPTIONS.md](https://github.com/Wendy-James/Wendy-James/blob/main/docs/RESUME_PROJECT_DESCRIPTIONS.md)
- Chinese resume project descriptions: [docs/RESUME_PROJECT_DESCRIPTIONS.zh-CN.md](https://github.com/Wendy-James/Wendy-James/blob/main/docs/RESUME_PROJECT_DESCRIPTIONS.zh-CN.md)

## GitHub Stats

<p>
  <img height="165" alt="GitHub Stats" src="https://github-readme-stats.vercel.app/api?username=Wendy-James&show_icons=true&hide_border=true&theme=default">
  <img height="165" alt="Top Languages" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Wendy-James&layout=compact&hide_border=true&theme=default">
</p>
