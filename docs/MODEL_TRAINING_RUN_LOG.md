# Model Training Run Log

Scope: Hungry Studio internship, 2026-07-21 onward  
Last synced: 2026-08-10 20:01 Asia/Shanghai

This page records detailed daily model-training work: how many runs were completed, what changed in each run, how long it took, what improved, and which directions were rejected. It is public-safe and does not publish raw company data, credentials, internal URLs, or unreviewed business details.

## Summary

| Period | Completed top-level training runs | Effective training/runtime | Main outcome |
|---|---:|---:|---|
| 2026-08-03 to 2026-08-06 | 50 | About 13h 22m 32s | Built Block Blast baselines, ablations, trajectory experiments, Mahjong C8, full CatBoost/rank-target experiments. |
| 2026-08-07 | 18 | About 6h 26m 42s | Added Block Crush baseline/optimization/stability checks, Mahjong C17 challenge model, Block Blast full CatBoost trajectory and growth-interaction checks. |
| Total captured so far | 68 | About 19h 49m 14s | Clear model lineage across Block Blast, Block Crush, and Mahjong Tile. |

Counting rule: one top-level training task counts once, even if it contains multiple folds, candidates, or sub-models. Failed runs, interrupted runs, calibration-only work, scoring-only work, and report generation are tracked separately.

## 2026-08-10 Shared Scoring / Deployment Update

No new successful model-training run was detected for 2026-08-10 during this sync. The new work is engineering validation, shared-table migration evidence, release packaging, runtime verification, fail-safe testing, scratch-table safety, workbook validation, and reporting.

| Area | Detail | Outcome |
|---|---|---|
| Shared-table schema | Verified `hs_market.ads_game_hourly_value_score_hi` has 17 business columns after adding `distinct_id`; partitions remain `dt/hour/bundle_id`. | `DDL_APPLIED_AND_VERIFIED`; identity columns and partition contract are ready for BB/MJ/BC shared scoring. |
| Block Blast release | Prepared V2 shared-sink mapping and materialized-tunnel archive for `bb_model006_trajectory_positive_blend_015_20260809_v2`. | BB remote gate passed on an exact `dt=2026-08-07/hour=10/bundle_id=com.block.juggle` partition with 27,362 rows and zero invalid/hash/rank rows. |
| Mahjong release | Prepared C17 shared-sink `distinct_id` v5 archive for `mahjongtile_c17_probability_only_rank_blend_20260807_v1`. | MJ remote gate passed on `dt=2026-08-05/hour=08/bundle_id=com.nebula.mahjongtile` with 8,041 rows; BB row count stayed unchanged and BC remained empty. |
| Block Crush release | Upgraded BC shared-hourly release to `BC-V6-SHARED-HOURLY-20260809-R3-HF1`. | Hotfix defaults missing full-population `population_weight` to 1.0, rejects invalid weights, adds LightGBM runtime dependency, and preserves exact-partition write scope. |
| Unified command | Installed unified DSW command `run run_score.sh --biz_date ... --hour ...`. | Dry-run passed for all three games with `ALL_THREE_MODELS_DRY_RUN_SUCCESS`. |
| Runtime gate | Real no-publish chain proved the functional path but BB SQL exceeded the 120s SLA. | Fail-safe candidate cancelled the remote BB instance at the SLA boundary, returned `124`, blocked MJ/BC, and wrote nothing to the shared table. |
| Reporting | Generated weekly algorithm internship report and three-model final-version reports with visual analysis. | Public log records artifact names only; raw internal documents and private data remain local. |
| BB direct-select release | Packaged `bb_model006_v2_single_reducer_direct_select_20260810_v3` for model `bb_model006_trajectory_positive_blend_015_20260809_v2`. | Status is `READY_FOR_DSW_UPLOAD`; compressed checksum `3ef72bfe7537c3280864abf6f90e7f2b2c5359b6bb24c5556c83f5fbbe1cdfda` is tracked for release integrity. |
| BB single-reducer candidate | Prepared `bb_model006_v2_single_reducer_direct_20260810_v1` with the SQL change limited to final reducer distribution. | Status is `LOCAL_VERIFIED_CANDIDATE_PENDING_REMOTE_GATE`; no promotion until remote gate passes. |
| Scratch-table handoff | Documented scratch-admin path for the authoritative 147-column historical result schema plus `run_id` partition cleanup. | Keeps create/drop permissions isolated from the shared production table and avoids broad mutation access. |
| Combined workbook | Validated `three_games_combined_visible_20260810.xlsx` for three-game review. | 40,331 rows total; BB 27,362 / MJ 8,041 / BC 4,928; all identity checks pass and formula error count is 0. |

### 2026-08-10 Training Count

| Type | Count | Runtime | Notes |
|---|---:|---:|---|
| New successful model-training runs | 0 | 0h | No algorithm/feature/target retraining was detected in the evening increment. |
| Release or deployment packaging | 3 | Postprocessing only | BB direct-select, BB single-reducer candidate, and scratch-table handoff packages/docs were updated. |
| Workbook/report validation | 1 workbook + reports | Postprocessing only | Three-game visible workbook and audience-specific report files were validated or indexed. |
| Failed/interrupted training | 0 | 0h | No new failed or restarted model-training task was detected in this increment. |

## 2026-08-09 Deployment / Validation Update

No new successful model-training run was detected for 2026-08-09 in the local artifacts scanned during this sync. The new work is deployment packaging and frozen-evaluation preparation for Block Crush V6.

| Area | Detail | Outcome |
|---|---|---|
| Block Crush identity lock | Project `block_crush_gp`, package `com.wood.block.sudoku.puzzle.bm`, target `y_ltv_24_72h`. | Prevents accidental BB/Mahjong data, model, encoder, parameter, or calibration mixing. |
| V10 CatBoost final status | V10 method-transfer training previously completed on 1,872,347 BC rows with 45 BC features in about 45.5 minutes. | V10 is not promoted; locked selection remains `BC_38_locked`, current best release remains BC V6 R2. |
| V6 development evidence | Aug-01 to Aug-03 diagnostic set: Spearman `0.514552`, NDCG@10% `0.722238`, Top10 revenue capture `82.6369%`, total amount error `4.1688%`, max daily amount error `9.7779%`. | Development gate looks strong but is not treated as final unseen OOT because it participated in V6 safety-factor selection. |
| Aug-04 frozen OOT | Local SQL, scorer, date guard, bundle guard, and three unit tests are ready. | One-time scoring is deferred until BC receives remote gate access in the BB -> MJ -> BC rollout order. |
| Shared-hourly release | Prepared `BC-V6-SHARED-HOURLY-20260809-R1` with runner, scoring scripts, DSW preflight/publish scripts, acceptance SQL, release manifest, and SHA256 archive. | Ready for DSW-side verification; writes must target only the exact `dt/hour/bundle_id` BC partition. |

## 2026-08-07 Detailed Runs

Completed training: 18 runs, about 6h 26m 42s.

| # | Game / Package | Training run | Duration | Change made | Result / improvement | Decision |
|---:|---|---|---:|---|---|---|
| 1 | Block Blast / `com.block.juggle` | CatBoost rank-target full retrain 003 | 2h 25m 30s; fitting 2h 24m 09s | Re-ran full rank-target CatBoost on 6,112,059 TRAIN users. | Spearman `0.500156`, slightly below 002 `0.500190`; Top10 rose to `0.628838`. | Reproducible and better head capture, but does not replace 002. |
| 2 | Block Crush / `com.wood.block.sudoku.puzzle.bm` | Full LightGBM A/B | 6m 09s | Compared BC38 vs BC41; trained positive classifiers and amount models. | BC38 won with OOT Spearman `0.457211`, Top10 `0.842066`. | Establishes Block Crush ranking baseline. |
| 3 | Mahjong Tile / `com.nebula.mahjongtile` | C17 full trajectory model | 15m 51s | Trained LTV positive, future 48-72h positive, and conditional amount stages with 140 features. | Historical OOT Spearman `0.539771`, +`0.006611` vs C8; Top10 `0.813123`. | Strong challenge model; waits for unseen August OOT before replacing C8. |
| 4 | Block Blast / `com.block.juggle` | Component Stacker | 3m 30s | Built 3-fold OOF stacker over 19 component features. | Spearman moved from `0.500190` to `0.500279`, only +`0.000089`. | Too small for stable gain; not promoted. |
| 5 | Block Blast / `com.block.juggle` | Recency positive precheck | 7m 47s; fitting 6m 21s | Tested 3-day half-life recency weighting. | Strategy search gave new model weight 0. | Recency weighting does not improve final LTV ranking. |
| 6 | Block Crush / `com.wood.block.sudoku.puzzle.bm` | Full optimization V2 | 1m 28s | Expanded from 38 to 45 features; trained 1 classifier and 8 amount candidates. | Best Huber tail-weighted amount model improved amount error but Spearman fell to `0.446761`. | Keep BC38 for ranking. |
| 7 | Block Blast / `com.block.juggle` | Retention-LTV precheck | 14m 21s; fitting 11m 27s | Added real retention target and historical CPI to LTV fusion. | Retention PR-AUC `0.595237`; final LTV fusion weight 0. | Useful standalone retention model, not useful for main LTV ranking. |
| 8 | Block Blast / `com.block.juggle` | 211-feature LightGBM trajectory hurdle | 3m 28s; fitting about 51s | Added four-window trajectory raw fields and trend/concentration derived features. | Positive-user amount Spearman `0.697775`; full LTV fusion weight 0. | Reject direct transfer of Mahjong trajectory hurdle design to Block Blast. |
| 9 | Block Crush / `com.wood.block.sudoku.puzzle.bm` | CatBoost method migration | 12m 09s; effective fitting about 8m 52s | Migrated CatBoost method using only Block Crush data/features. | Final selection still chose BC38; CatBoost did not beat LightGBM baseline. | Method migration rejected for ranking replacement. |
| 10 | Block Blast / `com.block.juggle` | 211-feature CatBoost trajectory A/B | 16m 31s; fitting 12m 39s | Compared trajectory-enhanced CatBoost with 152-feature baseline. | Positive PR-AUC +`0.003085`, ROC-AUC +`0.002672`; LTV strategy still gave new model weight 0. | Trajectory helps positive classification, not final LTV ordering. |
| 11 | Block Crush / `com.wood.block.sudoku.puzzle.bm` | Weekday amount model V5 | 1m 48s | Trained 47-feature positive classifier and conditional amount model. | Fresh diagnostic total amount error fell to `5.22%`, but max daily error `10.89%`. | Does not pass daily stability gate. |
| 12 | Block Blast / `com.block.juggle` | Full-population trajectory positive CatBoost 014 | 1h 31m 01s; fitting about 1h 30m 17s | Trained 211-feature positive CatBoost on the full population with full hourly trajectories. | Frozen selection PR-AUC `0.626720`, Spearman `0.498541`. | Full positive modeling is useful evidence, but does not replace rank-target 002. |
| 13 | Block Crush / `com.wood.block.sudoku.puzzle.bm` | Weekday V5 seed 20260819 | 40s | Changed random seed to test V5 stability. | Fresh Spearman `0.455039`, total amount error `6.49%`, max daily error `12.44%`. | Shows V5 is seed-sensitive; not promoted. |
| 14 | Block Crush / `com.wood.block.sudoku.puzzle.bm` | Weekday V5 seed 20260829 | 40s | Ran a second random-seed stability check. | Fresh Spearman `0.452364`, total amount error `4.78%`, max daily error `10.38%`. | Total error improved but daily stability still failed. |
| 15 | Block Crush / `com.wood.block.sudoku.puzzle.bm` | Tweedie amount V7 | 1m 52s | Tested Tweedie amount objective candidates. | Fresh Spearman fell to `0.421192`, max daily error `15.74%`. | Reject Tweedie as the current amount objective. |
| 16 | Block Crush / `com.wood.block.sudoku.puzzle.bm` | Recency-weighted V8 | 3m 08s | Tested three time-decay half-lives with classifier and regressor pairs. | Best 7-day half-life still only reached Spearman `0.449429`, max daily error `16.10%`. | Simple recency weighting hurts stability; not promoted. |
| 17 | Block Blast / `com.block.juggle` | Growth-interaction CatBoost preflight 016 | 15m 17s; fitting about 12m 57s | Expanded to 219 features with growth interactions and higher CTR interaction complexity. | Spearman `0.499093`, candidate weight `0.025`; stability gate failed. | Weak incremental signal exists, but not enough for full promotion. |
| 18 | Block Crush / `com.wood.block.sudoku.puzzle.bm` | Deep CatBoost V10-R2 | 45m 31s | Trained deeper positive and rank CatBoost models. | Did not beat BC38 after final selection. | Confirms the current bottleneck is not simply model capacity. |

### 2026-08-07 By Game

| Game | Completed runs | Runtime |
|---|---:|---:|
| Block Blast | 8 | 4h 57m 25s |
| Block Crush | 9 | 1h 13m 26s |
| Mahjong Tile | 1 | 15m 51s |
| Total | 18 | 6h 26m 42s |

### 2026-08-07 Non-Training Work

| Game | Work item | Duration | Contribution |
|---|---|---:|---|
| Block Crush | Dual-output V3 | About 48s | Kept BC38 for ranking and switched amount output to BC45; total amount error improved from `11.37%` to `2.22%`. |
| Block Crush | Segment reranking | About 32s | Kept BC38 head and CatBoost reranked middle/tail; historical OOT Spearman rose from `0.457211` to `0.507762`. |
| Block Crush | Fresh OOT locked evaluation | About 19s | Ranking passed, amount total error `24.73%`; stayed offline. |
| Block Crush | Dual-output fresh OOT evaluation | About 11s | Amount error improved to `14.55%`, still above 10% gate. |
| Block Crush | Amount calibration V4 | About 13s | Amount error improved to `9.87%`; treated as diagnostic because the batch had already been observed. |
| Block Crush | Online candidate V6 | About 9s | Spearman `0.514552`, amount error `4.17%`; development gate passed, still needs unseen OOT. |
| Block Blast | Positive blend 015 | Inference/fusion only | Reused existing models; Spearman reached `0.500463`, +`0.000273` over the previous Block Blast best, but it remains a fusion diagnostic rather than a fresh training run. |
| Block Crush | Multi-seed robustness check | About 6s | Compared seed stability and found Seed09 V6 remained the most stable; multi-seed ensemble increased daily amount error. |
| Block Crush | Lag7 Weekday V9 | Reused models | Adjusted calibration and strategy only; improvement was too small, so V6 remained preferred. |

### 2026-08-07 Failed / Extra Runtime

- Block Crush LightGBM had three incomplete starts; one run completed core training in about 6m 18s but failed during report generation.
- Component Stacker first attempt ran about 5m 02s and completed only one candidate before restart.
- Retention-LTV first two attempts totaled about 3m 34s because of label and alignment fixes.
- Block Crush CatBoost produced models before report failure; postprocessing reused trained models without retraining.
- Block Blast full trajectory CatBoost first attempt ran about 48m 33s before interruption and restart.
- Block Crush Deep CatBoost V10 first attempt ran about 10m 07s before interruption; V10-R2 completed successfully.
- Block Blast full trajectory rank 017 consumed about 1h 30m 07s, but it did not write a model, metrics, or completion marker, so it is tracked as incomplete rather than successful.

### 2026-08-07 Final State

- Mahjong official frozen model remains C8; C17 is the latest challenge model.
- Block Blast best Spearman remains rank-target 002 at `0.500190`.
- Block Crush ranking baseline remains BC38; V6 is a development-stage online candidate.
- Retention, recency, stacker, direct trajectory-hurdle, Tweedie amount, and deep-capacity directions did not stably improve final promotion decisions.

## 2026-08-03 to 2026-08-06 Daily Detail

### 2026-08-03

Completed training: 9 runs, about 5h 25m 32s.

| Training run | Duration | Change made | Result / contribution |
|---|---:|---|---|
| MODEL-001 initial dual-target CatBoost | 4m 26s | Built strict time-split baseline for ad-revenue classification and LTV hurdle amount. | TEST PR-AUC `0.447888`, amount Spearman `0.385420`; baseline established. |
| ABLATION-001 group ablation | 24m 02s | Ran about 36 fits over feature groups. | Found R09 features critical for classification; some behavior features hurt amount ranking. |
| ABLATION-002 joint subset search | 15m 17s | Ran about 32 fits and selected a 55-feature variant. | VALID PR-AUC +`0.000208`; later OOT showed it was not stable enough. |
| MODEL-001 rerun | 3m 32s | Reproduced baseline artifacts and split logic. | Confirmed reproducibility. |
| ML-SHAP first pass | About 9m 04s | Added SHAP, nonlinear thresholds, and feature explanation. | Helped explain feature direction and next candidates. |
| MODEL-002 first real OOT | 4m 16s | Scored frozen features against real OOT. | PR-AUC `0.462481`, amount Spearman `0.389815`; reference61 proved more stable than selected55. |
| MODEL-002 rerun | 4m 16s | Rechecked OOT and deliverables. | Confirmed model and outputs reproduce. |
| MODEL-002 diagnostic rerun | 4m 16s | Added diagnostics, calibration, and model comparison. | Confirmed CatBoost classification advantage and LightGBM amount tradeoff. |
| MODEL-003 hourly trajectory A/B | 4h 16m 23s | Trained six sub-models comparing static features vs full hourly trajectories. | Classification PR-AUC +`0.013052`, Top10 +`0.004663`; proved trajectories mainly help monetization-positive classification. |

### 2026-08-04

Completed training: 11 runs, about 1h 03m 50s.

| Training run | Duration | Change made | Result / contribution |
|---|---:|---|---|
| ML-SHAP rerun | About 9m | Stabilized explanations and reports. | Confirmed core feature directions. |
| MODEL-004 trajectory-family ablation | 38m 50s | Trained 24 models over trajectory families. | Kept monetization timing, trajectory change, and coverage families for classification/LTV positive stages; no trajectory family passed amount-stage gate. |
| MODEL-005 joint family search | 14m 09s | Trained 16 models over compressed family combinations. | Classification VALID PR-AUC `0.457292`, +`0.013434`; LTV positive PR-AUC +`0.018022`. |
| MODEL-006 streaming precheck 1 | 9s | Tested FeatureHasher, SGD three-head model, chunked reading, memory path. | Full-data linear pipeline proved runnable. |
| MODEL-006 streaming precheck 2 | 10s | Rechecked streaming path. | Confirmed technical path. |
| Mahjong A-fast | 2.9s | Minimal smoke test. | Verified Mahjong data/labels/training path. |
| Mahjong A-42k | 5.4s | Expanded sample size. | Checked metric stability. |
| Mahjong A sampled full pass | 22.9s | Built initial Mahjong hurdle baseline. | Established early Mahjong value model baseline. |
| Mahjong B | 16.8s | Tested amount targets and calibration. | Showed long-tail amount cannot rely on plain regression. |
| Mahjong C0 | 23.8s | Introduced strict 0-23h feature window and historical CPI direction. | Started leakage and time-window cleanup. |
| Mahjong C1 | 20.1s | Rechecked strict-window configuration. | Provided stable reference for C2-C5 ablations. |

Additional cost: MODEL-006 full-file attempts failed four times; longest ran 54m 41s and read 720,970 rows before a bad CSV record stopped it. This is data-format troubleshooting, not successful training.

### 2026-08-05

Completed training: 20 runs, about 1h 02m 26s.

| Training run | Duration | Change made | Result / contribution |
|---|---:|---|---|
| Mahjong C2 / C2a / C2b | 20.3s / 24.9s / 27.7s | Tested strict windows, CPI/device fields, and ablation combinations. | Quickly rejected unstable configurations. |
| Mahjong C3 / C4 | 21.5s / 24.9s | Continued feature and hurdle-structure compression. | Prepared C5 baseline structure. |
| Mahjong C5 sampled | 22.8s | Checked final full-run baseline setup. | Confirmed full baseline could run. |
| Mahjong C6 ranking model | About 1m 37s | Tried LambdaRank/rank_xendcg and C5 fusion. | Independent ranker could not stably replace hurdle ranking. |
| Mahjong C7 | 24.7s | Supplemented ranking-fusion direction. | Did not beat C5/C8. |
| Mahjong C8 sampled | About 22s | Prechecked L1, L2, Huber, Fair, Tweedie, and tail-weighted targets. | Narrowed full C8 search. |
| Mahjong C5 full | Runtime 2m 24s; end-to-end 4m 39s | Ran 3,183,064-row full baseline. | OOT Spearman `0.509631`, Top10 `0.802577`; became challenge reference. |
| Mahjong C8 full | 1m 51s | Selected tail-weighted `log_l2_tail_w4`. | OOT Spearman `0.533160`, Top10 `0.807091`; key Mahjong upgrade over C5. |
| Mahjong C9 full | 1m 01s | Multi-seed tail ensemble. | Top10 `0.808213`, but Spearman `0.530927`; head-income backup only. |
| MODEL-006 full streaming linear | 11m 46s | Trained all 7,578,579 rows for 3 epochs. | VALID Spearman `0.369473`, Top10 `0.720953`; fast but limited ranking ceiling. |
| MODEL-006 manufacturer-RAM full linear | 12m 03s | Added device cross features. | Spearman fell to `0.368863`; single cross feature direction rejected. |
| Mahjong C10 | 2m 06s | High-value-user specialist. | Fusion Spearman `0.532247`; worse than C8. |
| Mahjong C11 | 3m 24s | Direct amount model. | Fusion Spearman `0.532318`; hurdle split remains better. |
| Mahjong C12 | 2m 29s | Full ranking model. | Fusion Spearman `0.532489`; below C8. |
| Mahjong C13 | 6m 22s | Value-weighted positive-probability model. | Spearman `0.532711`, Top10 `0.807526`; slight head gain, still below C8. |
| MODEL-006 CatBoost 83-feature precheck first run | 7m 13s | Trained nonlinear model; completion marker incomplete. | Showed nonlinear model may beat same-sample linear. |
| MODEL-006 CatBoost 83-feature rerun | 7m 01s | Fully reproduced and saved artifacts. | Spearman `0.372507`, +`0.005336` vs linear; Top10 +`0.083836`. |

Calibration-only items: OPT-001 and OPT-002 reused old predictions and did not retrain. OPT-001 raised selection Spearman from `0.364755` to `0.448841`, but sacrificed some Top10.

### 2026-08-06

Completed training: 10 top-level tasks, about 5h 50m 44s.

| Training run | Duration | Change made | Result / contribution |
|---|---:|---|---|
| Mahjong C14 behavior-efficiency features | 1m 28s | Expanded from 46 to 65 features. | Spearman `0.524763`, fusion `0.528606`; below C8. |
| MODEL-006 CatBoost hurdle precheck | 11m 28s | Trained positive classifier and three conditional amount models. | Spearman `0.475042`, Top10 `0.589155`; positive probability remains main signal. |
| LightGBM ordinal precheck | 2m 35s | Trained four cumulative-threshold classifiers. | Spearman `0.473996`, Top10 `0.601212`; ordinal target below hurdle. |
| LightGBM rank precheck | 3m 24s | Tested five rank regression candidates. | Best fusion Spearman `0.474909`, Top10 `0.603694`; head improved, ranking still insufficient. |
| CatBoost 152-feature positive precheck | 11m 15s | Added full hourly trajectory, contract fields, country-media and manufacturer-RAM crosses. | Spearman `0.494248`; strongest Block Blast precheck gain. |
| CatBoost positive full official | 2h 57m 44s; fitting 2h 50m 18s | Ran 6,112,059 TRAIN users with 152 features. | Frozen selection raw Spearman `0.477961`, tie-adjusted `0.497884`, Top10 `0.572990`; official nonlinear baseline. |
| CatBoost rank-target full official | 1h 20m 51s; fitting 1h 19m 41s | Changed target to cohort LTV percentile rank. | Spearman `0.500190`, Top10 `0.627486`; current Block Blast best official model. |
| Cohort LambdaRank precheck batch | Effective fitting 48m 29s | Tested binary, positive-Q5, positive-Q10, positive-Q20 candidates. | Best fusion Spearman `0.499204`, only +`0.000629`; not enough to replace rank-target. |
| Mahjong C16 CPI/version fix | 3m 00s | Added CPI fallback/source/tier and parsed version features. | Spearman `0.528885`, fusion weight 0; exposed need for fresh country-media CPI data. |
| MODEL-006 hurdle OOF precheck | 10m 30s | Built six OOF models plus one final ranker. | Fusion Spearman `0.497287`, below reference; Top10 `0.614457`, head-enhancement backup only. |

Not counted: LightGBM rank first attempt ran about 2m 34s before restart; LambdaRank full batch including restarts took about 1h 41m 18s, with about 52m 49s in restart/reuse/troubleshooting. C15, monotone ties, future monetization blend, and segment calibration reused old predictions.

## Time Concentration

| Work block | Runtime | Share |
|---|---:|---:|
| MODEL-003 hourly trajectory A/B | 4h 16m 23s | About 24.9% of captured training time |
| CatBoost positive full official | 2h 57m 44s | About 17.2% |
| CatBoost rank-target full official | 1h 20m 51s | About 7.8% |
| Cohort LambdaRank effective fitting | 48m 29s | About 4.7% |
| 2026-08-07 rank-target full retrain 003 | 2h 25m 30s | About 14.1% |

## Automation Requirement

Every scheduled sync should append:

- Daily count of completed training runs.
- Per-run game/package, duration, algorithm/target/features changed, metric movement, contribution, and decision.
- Separate section for failed/interrupted runs and postprocessing-only work.
- Visual summary updates for training count, runtime distribution, deliverable mix, and model lineage.
