# Hungry Studio Internship Log

Internship start date: 2026-07-21  
Last synced: 2026-08-10 20:01 Asia/Shanghai

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
| 2026-08-07 | Completed 18 top-level model-training tasks across Block Blast, Block Crush, and Mahjong Tile; finalized full-data CatBoost, trajectory, recency, seed-stability, Tweedie, deep-capacity, and deployment-oriented checks; prepared GitHub profile automation and work-log deployment. | Detailed model run log; `mahjongtile_c17_deploy_update_20260807.tar.gz`; `mahjongtile_c17_sql_hotfix_20260807_v2.tar.gz`; GitHub profile sync automation. |
| 2026-08-08 | Scheduled sync maintenance; no new public-ready local artifact detected beyond the finalized 2026-08-07 model-training summary. | Automation check record; updated daily log boundary. |
| 2026-08-09 | Packaged Block Crush V6 into a shared-hourly scoring adapter for the three-game table, locked partition safety, documented DSW rollout, and prepared one-time Aug-04 OOT evaluation materials. | `BC-V6-SHARED-HOURLY-20260809-R1`; release manifest; DSW rollout notes; acceptance SQL; Aug-04 OOT SQL/scorer/test assets. |
| 2026-08-10 | Unified BB/MJ/BC hourly scoring command and release evidence; verified 17-column shared-table contract; confirmed dry-run success and fail-safe behavior when BB SQL exceeded SLA; prepared BB single-reducer/direct-select packages, scratch-table handoff, combined three-game workbook validation, and weekly/three-model reports. | Weekly report PDF/DOCX; three-model final-version PDF/DOCX; `bb_model006_v2_single_reducer_direct_select_20260810_v3`; `bb_model006_v2_single_reducer_direct_20260810_v1`; `three_games_combined_visible_20260810.xlsx`; `unified_three_game_runtime_effect_20260810.json`; shared schema migration evidence. |

## Artifact Index

### Feature Engineering And Audit

- Block Blast GP feature plans and phase SQL: `block_blast_gp_feature_engineering_plan.md`, `block_blast_gp_feature_engineering_phase2.sql`, `block_blast_gp_feature_engineering_phase3.sql`, `block_blast_gp_feature_engineering_phase4.sql`.
- Data quality/audit evidence: `block_blast_gp_dataworks_audit.json`, `block_blast_gp_feature_engineering_audit.json`, `block_blast_gp_verification.json`.
- Stability and segmentation CSVs: phase-2 daily stability, phase-3 numeric/media/category signals, phase-4 redundancy/decile/blank-media checks.

### Modeling And Evaluation

- Block Blast GP reports: baseline analysis, feature processing, D0 audit, OOT maturity/target stability, hourly trajectory diagnostics, ablation reports, final OOT model effect, and full workflow summary.
- MahjongTile model runs: C0/C2/C2A/C4/C5/C6/C7/C8/C17 variants with metrics, feature importance, robustness checks, threshold reports, and holdout predictions.
- 2026-08-07 model-training summary: 18 successful top-level runs, about 6h 26m 42s, with separate tracking for failed, interrupted, and postprocessing-only work.
- Model artifacts: selected `.joblib` models and feature transform manifests kept locally; public profile records only summary-level deliverables.

### Deployment-Oriented Work

- MahjongTile scoring package: `mahjongtile_hourly_model` with `train.py`, `score.py`, `run_hour.py`, `train_data.sql`, `score.sql`, and model manifest.
- Deployment archives prepared on 2026-08-07: `mahjongtile_c17_deploy_update_20260807.tar.gz` and `mahjongtile_c17_sql_hotfix_20260807_v2.tar.gz`.
- Block Crush shared-hourly release prepared on 2026-08-09: `BC-V6-SHARED-HOURLY-20260809-R1`, with exact `dt/hour/bundle_id` partition-scope protection and DSW rollout checks.
- Shared-table deployment evidence prepared on 2026-08-10: 17-column migration evidence, unified command verification, BB/MJ/BC release package index, fail-safe runtime report, and cross-game acceptance checklist.
- Block Blast 2026-08-10 release packaging: `bb_model006_v2_single_reducer_direct_select_20260810_v3` is marked `READY_FOR_DSW_UPLOAD` with compressed checksum `3ef72bfe7537c3280864abf6f90e7f2b2c5359b6bb24c5556c83f5fbbe1cdfda`; `bb_model006_v2_single_reducer_direct_20260810_v1` remains a local-verified candidate pending remote gate.
- Scratch-admin handoff: documented isolated scratch-table creation using the 147-column historical result schema plus `run_id` partition cleanup, without shared-table or project-wide mutation privilege.
- Combined three-game workbook: `three_games_combined_visible_20260810.xlsx` validates 40,331 rows across BB 27,362 / MJ 8,041 / BC 4,928, with all identity contracts passing and zero formula errors.

### Reporting Outputs

- Weekly report: `算法工程实习生周报_2026-08-03至2026-08-09.pdf`.
- Three-model final summary: `三个小时价值模型最终版本总结_20260810.pdf` and visual-optimized version.
- Visual assets: `three_model_metric_context_20260810.png`, `three_model_metric_context_visual_20260810.png`, `three_model_training_framework_20260810.png`.
- Editable and audience-specific summaries: `8.3-8.9工作总结.docx`, `三个小时价值模型目标梳理_数据分析师简版_20260810.pdf`, `三个小时价值模型最终版本总结_简洁楷体版_20260810.docx`, and `最终版本—总结.pdf`.
- Block Crush handoff docs: `BC_V6_R2_下游交付与接入说明_v1.0.docx` and `BC_V6_R2_下游数据分析师接入手册_精简版_v1.0.docx`.

## Visual Analysis

- Timeline, deliverable mix, workflow map, and maturity snapshot are maintained in [Hungry Studio Internship Visual Summary](HUNGRY_STUDIO_VISUAL_SUMMARY.md).
- Detailed model counts, run durations, changes, improvements, failures, and decisions are maintained in [Model Training Run Log](MODEL_TRAINING_RUN_LOG.md).
- Future sync runs should update both daily text records and visual summaries when new work content or deliverables appear.

## Public Boundary

- Raw company datasets, internal credentials, access keys, private URLs, and unreviewed business-sensitive tables are not published.
- This profile repository publishes public summaries, artifact names, and sanitized deliverable descriptions.
- Detailed files remain local unless explicitly reviewed for public release.
