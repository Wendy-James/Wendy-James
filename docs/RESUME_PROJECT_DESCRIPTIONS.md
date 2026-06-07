# Resume Project Descriptions

> Target roles: AI Algorithm Intern, Machine Learning Intern, LLM Algorithm Intern, Recommendation Algorithm Intern, Agent / AIGC Intern  
> GitHub Profile: https://github.com/Wendy-James

This document converts the selected GitHub projects into resume-ready descriptions. The wording is designed for algorithm internship applications and keeps claims aligned with public repository evidence.

## 1. LLM RAG System

Repository: https://github.com/Wendy-James/hybrid-rag-lab

### One-Line Version

- Built a Hybrid RAG retrieval system with BM25, dense-style retrieval, query rewrite, RRF fusion, reranking, and Recall/MRR/nDCG evaluation.

### Three-Line Version

- Designed a reproducible RAG retrieval pipeline covering local corpus loading, labeled query evaluation, BM25 sparse retrieval, dense-style retrieval, query rewrite, RRF fusion, and reranking.
- Implemented evaluation scripts and experiment outputs for Recall@3, MRR@3, and nDCG@3, with bilingual README, architecture notes, algorithm documentation, and interview notes.
- Improved the retrieval workflow from single-route retrieval to hybrid multi-route retrieval with reranking, making the project explainable from both algorithm and engineering perspectives.

### STAR Interview Version

Situation: Single-route RAG retrieval can miss relevant evidence when exact technical terms and semantic paraphrases appear in different forms.

Task: Build a measurable retrieval pipeline that can compare sparse retrieval, dense retrieval, fusion, and reranking before adding answer generation.

Action: Implemented BM25, deterministic dense-style retrieval, query rewrite, Reciprocal Rank Fusion, lexical reranking, CLI execution, and Recall/MRR/nDCG evaluation outputs.

Result: Delivered a runnable RAG project with experiment metrics, architecture documentation, algorithm notes, and clear extension paths toward embeddings, FAISS, and cross-encoder reranking.

## 2. Multi-Agent Assistant

Repository: https://github.com/Wendy-James/multi-agent-research-lab

### One-Line Version

- Built a local multi-agent research workflow with planner, researcher, writer, verifier, summarizer agents, state graph execution, tool-call traces, and verification metrics.

### Three-Line Version

- Designed an Agent workflow as explicit state transitions across Planner, Researcher, Writer, Verifier, and Summarizer roles, improving observability and modularity.
- Implemented local tool calling, lightweight memory, verifier feedback, CLI execution, and experiment traces exported as CSV/JSON.
- Documented architecture, agent role design, tool-call logging, reliability metrics, and interview-ready explanations for Agent and multi-agent system roles.

### STAR Interview Version

Situation: Agent workflows are difficult to debug when planning, tool use, memory, and verification are mixed into one implicit loop.

Task: Build a local multi-agent workflow that separates responsibilities and records execution traces.

Action: Implemented a state-graph workflow with planner/researcher/writer/verifier/summarizer agents, local tool registry, memory, verification, CLI runs, and trace exports.

Result: Delivered a runnable Agent project that demonstrates state management, tool-call observability, verification logic, and a migration path toward LangGraph and MCP-style tools.

## 3. CTR Ranking Lab

Repository: https://github.com/Wendy-James/ctr-ranking-lab

### One-Line Version

- Built a CTR prediction and ranking lab with feature engineering, feature crossing, Logistic Regression, GBDT-style baseline, AUC, LogLoss, and nDCG@5 evaluation.

### Three-Line Version

- Created a reproducible CTR experiment pipeline with synthetic impression data, categorical/numerical feature encoding, category-device feature crossing, and train/validation split.
- Compared Logistic Regression with a lightweight GBDT-style stump boosting baseline using AUC, LogLoss, and user-level nDCG@5 ranking metrics.
- Generated CSV/JSON experiment artifacts and documented model assumptions, feature design, metric interpretation, architecture, and interview questions.

### STAR Interview Version

Situation: Recommendation ranking requires both accurate click probability estimation and strong top-K ordering quality.

Task: Build a CTR lab that demonstrates feature engineering, model comparison, and ranking-oriented evaluation.

Action: Implemented impression data generation, feature encoding, feature crossing, Logistic Regression, stump boosting, AUC, LogLoss, nDCG@5, CLI execution, and experiment reports.

Result: Delivered a runnable recommendation project that shows machine-learning engineering, metric understanding, and a clear path toward LightGBM, XGBoost, CatBoost, DeepFM, and xDeepFM experiments.

## 4. Document Intelligence

Repository: https://github.com/Wendy-James/project-briefs/tree/main/case-studies/adaptive-document-structuring-model

### One-Line Version

- Led a document intelligence research project focused on structured information extraction, schema design, validation rules, and multi-scenario document understanding.

### Three-Line Version

- Designed a document structuring workflow that maps unstructured content into scenario-specific fields, schemas, and validation rules.
- Analyzed extraction requirements across document types and documented the system boundary, data flow, explainability needs, and structured output format.
- Produced public project materials that demonstrate research planning, information extraction thinking, and practical AI application design.

### STAR Interview Version

Situation: Document-heavy workflows often require converting unstructured content into reliable structured fields.

Task: Design a research-oriented document intelligence workflow that supports multiple scenarios and clear validation.

Action: Defined schemas, extraction fields, validation rules, scenario requirements, and explainable output structures.

Result: Built a project brief that demonstrates document understanding, structured extraction design, and AI workflow decomposition.

## 5. AI Job Application Agent

Repository: https://github.com/Wendy-James/project-briefs/tree/main/case-studies/ai-career-interview-system

### One-Line Version

- Designed an AI job application workflow for JD parsing, candidate matching, resume draft generation, and interview preparation with human review.

### Three-Line Version

- Designed a workflow that parses job descriptions, structures candidate profiles, matches requirements, and generates tailored resume and interview-preparation outputs.
- Planned backend architecture with FastAPI, PostgreSQL, Redis, Celery, Docker, LLM workflow modules, and LaTeX resume generation.
- Documented system boundaries, human-review steps, data flow, and engineering modules to make the project understandable for AI engineering interviews.

### STAR Interview Version

Situation: Applying to technical roles requires repeatedly mapping job requirements to candidate experience and preparing targeted materials.

Task: Design an AI workflow that makes job matching, resume drafting, and interview preparation structured and reviewable.

Action: Broke the workflow into JD parsing, profile structuring, requirement matching, resume generation, interview question generation, and human review.

Result: Produced a clear AI application system design that demonstrates LLM workflow thinking, backend architecture planning, and product-oriented engineering.

## Resume GitHub Link

Recommended resume link:

```text
GitHub: https://github.com/Wendy-James
```

Recommended one-line profile summary:

```text
GitHub portfolio focused on LLM/RAG, Agent workflows, CTR ranking, recommendation algorithms, and machine-learning engineering.
```
