# Hungry Studio Internship Log

Internship start date: 2026-07-21  
Last synced: 2026-08-07 17:35 Asia/Shanghai

This is a public-facing internship work log. It records daily outcomes and deliverable categories, while avoiding raw private company data, credentials, internal URLs, and unreviewed business details.

## Current Focus

- User value prediction for game growth.
- Retention and ad-revenue LTV modeling.
- DataWorks / MaxCompute SQL audits.
- Feature engineering, leakage checks, OOT validation, model comparison, and deployment packaging.

## Daily Outcomes

| Date | Work Content | Public Deliverables |
|---|---|---|
| 2026-07-21 | Started Hungry Studio internship; set up internship tracking scope and work log baseline. | Internship log baseline. |
| 2026-07-22 | Organized dated Codex workspaces and output folders for later artifact tracking. | Workspace/output directory structure. |
| 2026-07-23 | Drafted project memo material and recovered a long-running task into a cleaner workspace. | `project_memo_draft.docx`; recovered task workspace. |
| 2026-07-24 | Installed and prepared LightGBM/XGBoost-related modeling environment; checked network and desktop code environment issues. | Environment setup notes; `desktop_code_fix_report.pdf`. |
| 2026-07-25 | Continued data and modeling preparation; no public-ready artifact detected in Codex output folders. | Internal work record placeholder. |
| 2026-07-26 | Continued data and modeling preparation; no public-ready artifact detected in Codex output folders. | Internal work record placeholder. |
| 2026-07-27 | Built a Block Blast GP CAPI/LTV feature engineering delivery package, including feature specs, manifests, MaxCompute SQL, validation scripts, visual analysis builders, and summary images. | `00_bb_capi_ltv_delivery_guide.md`; `01_bb_capi_ltv_feature_specification.md`; `02_bb_capi_ltv_feature_manifest.csv`; SQL, validator, and visual analysis artifacts. |
| 2026-07-28 | Prepared DataWorks growth-analysis SQL, feature-engineering data exploration SQL, project-scale audit framing, and LTV + retention modeling objective. | DataWorks SQL examples; feature-engineering exploration SQL; data口径 notes. |
| 2026-07-29 | Produced Block Blast GP DataWorks audit outputs, baseline prediction analysis, data integrity checks, leakage/sample filtering tables, and staged TSV evidence. | DataWorks stage-3 TSV outputs; Block Blast GP baseline/audit report. |
| 2026-07-30 | Continued follow-up project work and maintained generated artifacts under dated workspace folders. | Updated output index. |
| 2026-07-31 | Continued feature engineering experiments and spreadsheet artifact organization. | Spreadsheet/artifact handling notes. |
| 2026-08-01 | Weekend or low-public-output day; no public-ready artifact detected. | Internal work record placeholder. |
| 2026-08-02 | Weekend or low-public-output day; no public-ready artifact detected. | Internal work record placeholder. |
| 2026-08-03 | Standardized downloaded spreadsheet naming, analyzed code structure, ran model evaluation, and compared Spearman-related model metrics. | Renaming workflow; code analysis summary; model evaluation outputs. |
| 2026-08-04 | Generated full-stage Block Blast GP work summary, local training strategy comparison, MahjongTile preflight/recovery reports, and multiple SHAP-style model runs. | `Block_Blast_GP_全阶段工作梳理说明_20260804.pdf`; MahjongTile ML-SHAP reports. |
| 2026-08-05 | Ran MahjongTile modeling variants C0/C2/C2A/C4/C5/C6/C7/C8, generated feature audits, model metrics, robustness checks, comparison PDFs/PNGs, and workbook outputs. | ML-SHAP output folders; model comparison artifacts; feature importance and robustness reports. |
| 2026-08-06 | Prepared BC-related OSS/model execution context and continued deployment-oriented checks. | OSS path review notes; deployment preparation record. |
| 2026-08-07 | Continued Block Blast GP / MahjongTile / BC full-data model training and deployment packaging; prepared GitHub profile automation and work-log deployment. | `mahjongtile_c17_deploy_update_20260807.tar.gz`; `mahjongtile_c17_sql_hotfix_20260807_v2.tar.gz`; GitHub profile sync automation. |

## Artifact Index

### Feature Engineering And Audit

- Block Blast GP feature plans and phase SQL: `block_blast_gp_feature_engineering_plan.md`, `block_blast_gp_feature_engineering_phase2.sql`, `block_blast_gp_feature_engineering_phase3.sql`, `block_blast_gp_feature_engineering_phase4.sql`.
- Data quality/audit evidence: `block_blast_gp_dataworks_audit.json`, `block_blast_gp_feature_engineering_audit.json`, `block_blast_gp_verification.json`.
- Stability and segmentation CSVs: phase-2 daily stability, phase-3 numeric/media/category signals, phase-4 redundancy/decile/blank-media checks.

### Modeling And Evaluation

- Block Blast GP reports: baseline analysis, feature processing, D0 audit, OOT maturity/target stability, hourly trajectory diagnostics, ablation reports, final OOT model effect, and full workflow summary.
- MahjongTile model runs: C0/C2/C2A/C4/C5/C6/C7/C8 variants with metrics, feature importance, robustness checks, threshold reports, and holdout predictions.
- Model artifacts: selected `.joblib` models and feature transform manifests kept locally; public profile records only summary-level deliverables.

### Deployment-Oriented Work

- MahjongTile scoring package: `mahjongtile_hourly_model` with `train.py`, `score.py`, `run_hour.py`, `train_data.sql`, `score.sql`, and model manifest.
- Deployment archives prepared on 2026-08-07: `mahjongtile_c17_deploy_update_20260807.tar.gz` and `mahjongtile_c17_sql_hotfix_20260807_v2.tar.gz`.

## Visual Analysis

- Timeline, deliverable mix, workflow map, and maturity snapshot are maintained in [Hungry Studio Internship Visual Summary](HUNGRY_STUDIO_VISUAL_SUMMARY.md).
- Future sync runs should update both daily text records and visual summaries when new work content or deliverables appear.

## Public Boundary

- Raw company datasets, internal credentials, access keys, private URLs, and unreviewed business-sensitive tables are not published.
- This profile repository publishes public summaries, artifact names, and sanitized deliverable descriptions.
- Detailed files remain local unless explicitly reviewed for public release.
