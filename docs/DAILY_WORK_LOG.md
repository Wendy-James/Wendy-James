# Daily Work Log

Last synced: 2026-08-10 20:01 Asia/Shanghai

This page is a public-facing index of Codex-assisted Hungry Studio internship outcomes from 2026-07-21 onward. It summarizes deliverables and keeps sensitive raw files out of the profile repository unless they are explicitly prepared for public release.

For the internship-specific version, see [Hungry Studio Internship Log](HUNGRY_STUDIO_INTERNSHIP_LOG.md). For charts and visual analysis, see [Hungry Studio Internship Visual Summary](HUNGRY_STUDIO_VISUAL_SUMMARY.md). For detailed model counts, duration, changes, and improvements, see [Model Training Run Log](MODEL_TRAINING_RUN_LOG.md).

## 2026-08-07

- Hungry Studio internship: continued Block Blast GP / MahjongTile / BC full-data modeling and deployment packaging.
- Model training detail: completed 18 training runs, about 6h 26m 42s; see the model run log for per-run changes, durations, metrics, and decisions.
- Final 8/7 update: added Block Blast full-population trajectory positive CatBoost, growth-interaction preflight, Block Crush seed stability, Tweedie, recency, and deep CatBoost checks.
- GitHub profile sync: confirmed the GitHub account `Wendy-James` and prepared a recurring sync workflow for daily work outcomes.
- Feature engineering model work: continued Block Blast GP / Mahjong / BC full-data model training and comparison tasks.
- Local cleanup: scanned desktop and project files for redundant or unused files.

## 2026-08-08

- Scheduled sync check: no new public-ready local artifact detected after the finalized 2026-08-07 model-training summary.
- Maintenance: kept the GitHub profile automation active for three daily updates and preserved the rule that newly discussed work content, outputs, model-training details, and visualization needs are included in the next sync.

## 2026-08-09

- Hungry Studio internship: packaged the Block Crush V6 shared-hourly adapter for the three-game shared output table.
- Work output: prepared release `BC-V6-SHARED-HOURLY-20260809-R1`, including scoring scripts, DSW preflight/publish scripts, acceptance SQL, shared-contract documentation, release manifest, and SHA256 archive.
- Validation summary: confirmed BC project identity `block_crush_gp / com.wood.block.sudoku.puzzle.bm`, target `y_ltv_24_72h`, 45 BC-only features, no cross-game data mixing, and V10 CatBoost non-promotion.
- Deployment gate: Aug-04 frozen OOT SQL/scorer/test chain is locally ready, but remote MaxCompute/OSS execution is deferred by the BB -> MJ -> BC rollout order.

## 2026-08-10

- Hungry Studio internship: consolidated the three-game hourly value scoring contract and unified DSW command path for Block Blast, Mahjong Tile, and Block Crush.
- Work output: generated weekly algorithm internship report PDF and three-model final-version reports, including framework and metric-context visualizations.
- Shared-table contract: verified the 17-column schema migration for `hs_market.ads_game_hourly_value_score_hi`, including `distinct_id`, `sample_key_hash`, `app_name`, and unchanged `dt/hour/bundle_id` partitions.
- Release updates: recorded Block Blast V2 materialized tunnel archive, Mahjong C17 shared-sink v5 archive, and Block Crush R3-HF1 hotfix release package.
- Runtime validation: dry-run command passed for all three games; real no-publish chain exposed BB SQL SLA failure, so fail-safe cancellation blocked MJ/BC and prevented shared-table writes.
- Evening deployment work: prepared Block Blast single-reducer and direct-select release packages, including `bb_model006_v2_single_reducer_direct_select_20260810_v3`, now marked `READY_FOR_DSW_UPLOAD` with compressed checksum `3ef72bfe7537c3280864abf6f90e7f2b2c5359b6bb24c5556c83f5fbbe1cdfda`.
- Scratch-table safety: documented isolated scratch-table handoff with exact `run_id` partition cleanup, 147-column historical schema alignment, and no shared-table mutation privilege.
- Combined workbook validation: produced `three_games_combined_visible_20260810.xlsx` with 40,331 rows across BB 27,362 / MJ 8,041 / BC 4,928; all identity contracts passed and formula error count was 0.
- Reporting outputs: added editable weekly/work-summary and three-model summary documents, including `8.3-8.9工作总结.docx`, `三个小时价值模型目标梳理_数据分析师简版_20260810.pdf`, and `最终版本—总结.pdf`.

## 2026-08-05

- Hungry Studio internship: ran MahjongTile modeling variants and ML-SHAP-style evaluations.
- Model training detail: part of the 2026-08-03 to 2026-08-06 block with 50 completed top-level runs and about 13h 22m 32s total runtime.
- Model comparison: compared model performance across parallel Codex tasks, focusing on accuracy, stability, and multi-dimensional capability.

## 2026-08-03

- Hungry Studio internship: evaluated model runs and organized downloaded model/result tables.
- Video annotation project: installed and deployed the current project environment.
- Downloaded spreadsheet cleanup: standardized downloaded spreadsheet names to improve retrieval and reuse.
- Code review: analyzed four code files and summarized their structure, risks, and improvement points.
- Model evaluation: ran model evaluation workflows and calculated metrics such as Spearman correlation.

## 2026-08-01 to 2026-08-02

- Hungry Studio internship: no public-ready artifact detected in Codex output folders; kept as internal work-log placeholders.

## 2026-07-31

- Model experiments: continued optimization and validation for feature engineering workflows.
- Spreadsheet and artifact handling: organized work outputs for later review.

## 2026-07-30

- Follow-up project work: continued Codex task outputs and maintained generated artifacts under dated workspace folders.

## 2026-07-29

- Hungry Studio internship: produced Block Blast GP DataWorks audit outputs and baseline prediction analysis.
- GitHub account setup: confirmed browser login for GitHub.
- DataWorks audit report: built an offline preview/report for Block Blast GP baseline prediction analysis.
- Output artifacts observed:
  - `2026-07-29_DataWorks_结果9_分层关联.tsv`
  - `2026-07-29_DataWorks_结果10_版本渠道OS交叉.tsv`
  - `2026-07-29_DataWorks_结果11_最终24h口径.tsv`
  - `2026-07-29_DataWorks_阶段3_01_数据完整性.tsv`
  - `2026-07-29_DataWorks_阶段3_02_13日24h覆盖曲线.tsv`
  - `2026-07-29_DataWorks_阶段3_03_14日质量与变现.tsv`
  - `2026-07-29_DataWorks_阶段3_04_0至72h行为变现曲线.tsv`
  - `2026-07-29_DataWorks_阶段3_05_特征分布分位数.tsv`
  - `2026-07-29_DataWorks_阶段3_06_时间边界污染.tsv`
  - `2026-07-29_DataWorks_阶段3_07_泄漏与样本筛选.tsv`

## 2026-07-28

- Hungry Studio internship: prepared DataWorks growth-analysis SQL and feature-engineering data exploration SQL.
- DataWorks SQL analysis: prepared growth-analysis SQL examples and feature-engineering data exploration SQL.
- Project scale assessment: estimated Block Blast GP data scale and framed the LTV + retention prediction objective.
- Data definition work: organized metric and field definitions for downstream modeling.

## 2026-07-27

- Hungry Studio internship: built the first public-friendly Block Blast GP CAPI/LTV feature engineering delivery package.
- Feature engineering package: produced a public-friendly Block Blast GP CAPI/LTV delivery package.
- Output artifacts observed:
  - `00_bb_capi_ltv_delivery_guide.md`
  - `01_bb_capi_ltv_feature_specification.md`
  - `02_bb_capi_ltv_feature_manifest.csv`
  - `03_bb_capi_ltv_maxcompute_train_24h_v2.sql`
  - `04_bb_capi_ltv_maxcompute_quality_check_v2.sql`
  - `05_bb_capi_ltv_offline_feature_engineering.py`
  - `06_bb_capi_ltv_delivery_validator.py`
  - `07_bb_capi_ltv_visual_analysis_builder.py`
  - `08_bb_capi_ltv_visual_analysis_artifact.json`
  - `09_bb_capi_ltv_visual_analysis_notes.md`
  - `10_bb_capi_ltv_static_visual_builder.py`
  - `10_bb_capi_ltv_visual_analysis_report.html`
  - `11_bb_capi_ltv_visual_summary.png`
- Weekly progress writing: drafted DingTalk weekly progress content.
- Document work: generated entry-date adjustment explanation documents.

## 2026-07-24

- Hungry Studio internship: prepared local modeling environment and network/tooling checks.
- Environment setup: deployed LightGBM / XGBoost and related tooling.
- Network check: diagnosed network connectivity.
- Desktop/code fix report: generated `desktop_code_fix_report.pdf`.

## 2026-07-25 to 2026-07-26

- Hungry Studio internship: continued setup and modeling preparation; no public-ready artifact detected in Codex output folders.

## 2026-07-23

- Document drafting: generated `project_memo_draft.docx`.
- Migration/recovery: recovered a long-running Codex task into a cleaner workspace.

## 2026-07-22

- Early workspace setup: created dated Codex workspaces and initial output folders.

## 2026-07-21

- Hungry Studio internship: internship start date; initialized public work-log baseline.

## Automation Plan

- Sync cadence: three times per day.
- Scope: Hungry Studio internship work, Codex tasks, and output folders from 2026-07-21 onward.
- Destination: GitHub profile repository `Wendy-James/Wendy-James`.
- Public boundary: publish summaries and prepared artifact indexes; avoid raw private documents unless explicitly reviewed.
