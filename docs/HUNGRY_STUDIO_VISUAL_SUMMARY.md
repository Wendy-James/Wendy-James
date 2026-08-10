# Hungry Studio Internship Visual Summary

Last synced: 2026-08-10 20:01 Asia/Shanghai

This page visualizes public-safe Hungry Studio internship outcomes from 2026-07-21 onward. It uses summaries and artifact categories only; raw company data and sensitive implementation details are not published.

## Work Timeline

```mermaid
gantt
    title Hungry Studio Internship Progress
    dateFormat  YYYY-MM-DD
    axisFormat  %m-%d

    section Setup
    Internship baseline and workspace setup      :done, 2026-07-21, 2d
    Modeling environment and tooling             :done, 2026-07-24, 1d

    section DataWorks / SQL
    Growth SQL and data exploration              :done, 2026-07-28, 2d
    Data quality and leakage audits              :done, 2026-07-29, 2d

    section Feature Engineering
    CAPI/LTV feature package                     :done, 2026-07-27, 2d
    Block Blast GP phased feature reports        :active, 2026-07-29, 10d

    section Modeling
    MahjongTile model variants and SHAP reports  :active, 2026-08-04, 4d
    BC / BB / MJ full-data training              :done, 2026-08-07, 1d

    section Deployment
    Scoring package and SQL hotfix archives      :active, 2026-08-07, 1d
    BC V6 shared-hourly release                  :active, 2026-08-09, 1d
    Shared 17-column scoring contract            :active, 2026-08-09, 2d
    Unified BB / MJ / BC command verification    :active, 2026-08-10, 1d
    BB single-reducer release packaging          :active, 2026-08-10, 1d
    Three-game workbook validation               :active, 2026-08-10, 1d
    GitHub profile auto-sync                     :active, 2026-08-07, 4d
```

## Deliverable Mix

```mermaid
pie showData
    title Public deliverable categories
    "SQL and DataWorks audits" : 14
    "Feature engineering specs" : 12
    "Model evaluation reports" : 25
    "Visualization reports" : 10
    "Deployment packages" : 11
    "Work logs and documentation" : 17
```

## Training Run Volume

```mermaid
xychart-beta
    title "Completed top-level training runs"
    x-axis ["08-03", "08-04", "08-05", "08-06", "08-07"]
    y-axis "Runs" 0 --> 22
    bar [9, 11, 20, 10, 18]
```

## Training Runtime

```mermaid
xychart-beta
    title "Effective training/runtime by day"
    x-axis ["08-03", "08-04", "08-05", "08-06", "08-07"]
    y-axis "Hours" 0 --> 7
    bar [5.43, 1.06, 1.04, 5.85, 6.45]
```

## Modeling Iteration Map

```mermaid
flowchart LR
    A["DataWorks tables and downloaded evidence"] --> B["Data quality audit"]
    B --> C["Feature engineering phases"]
    C --> D["Baseline model"]
    D --> E["Ablation and leakage checks"]
    E --> F["OOT validation"]
    F --> G["Model variant comparison"]
    G --> H["Scoring package and SQL hotfix"]
    H --> I["Scratch-table and single-reducer safety gate"]
    I --> J["Three-game workbook validation"]
    J --> K["Public work-log deployment"]
```

## Work Content vs Work Output

| Area | Work Content | Work Output |
|---|---|---|
| Data audit | Checked table scale, field quality, missingness, time-window boundaries, and leakage risk. | DataWorks SQL, TSV evidence tables, audit JSON, data-quality reports. |
| Feature engineering | Built staged Block Blast GP feature plans and reduced redundant or unstable features. | Feature specs, manifests, phase SQL, redundancy/stability CSVs, processing reports. |
| Modeling | Compared model variants across ranking, amount prediction, device hierarchy, CPI/manufacturer/RAM, and country/device/carrier settings. | Metrics CSVs, feature importance, SHAP-style reports, robustness checks, holdout predictions. |
| Visualization | Built readable HTML/PDF/PNG summaries for audits, feature behavior, OOT maturity, ablation, and final model effect. | Visual reports, comparison charts, full-stage workflow summary PDFs. |
| Deployment | Prepared MahjongTile hourly scoring package, model manifests, SQL hotfixes, and deployment archives. | `mahjongtile_hourly_model`, C17 deploy update archive, C17 SQL hotfix archive. |
| Shared scoring | Packaged Block Crush V6 for the shared three-game hourly value table with exact partition protection. | `BC-V6-SHARED-HOURLY-20260809-R1`, DSW rollout notes, acceptance SQL, release manifest. |
| Unified runtime | Verified 17-column BB/MJ/BC shared-table contract, command format, dry-run path, and fail-safe cancellation. | Shared schema migration evidence, unified command verification JSON, runtime effect JSON, release package index. |
| BB packaging | Prepared direct-select and single-reducer Block Blast deployment candidates while preserving remote-gate separation. | `bb_model006_v2_single_reducer_direct_select_20260810_v3`, `bb_model006_v2_single_reducer_direct_20260810_v1`, release manifests. |
| Scratch safety | Converted scratch-admin needs into a minimal-permission handoff with isolated table scope and exact `run_id` partition cleanup. | Scratch handoff docs, 147-column schema contract, privilege-boundary notes. |
| Workbook validation | Built a visible three-game review workbook and checked identity/rank/formula contracts. | `three_games_combined_visible_20260810.xlsx`, validation JSON, acceptance screenshots. |
| Profile sync | Maintained public GitHub profile logs for daily internship work. | `README.md`, `DAILY_WORK_LOG.md`, internship log, visual summary, scheduled sync task. |

## Shared Deployment Gate Snapshot

| Gate | Status | Public-safe result |
|---|---|---|
| Shared schema migration | Passed | `distinct_id` added as the 17th business column; `dt/hour/bundle_id` partitions unchanged. |
| BB remote gate V2 | Passed | 27,362 rows; unique IDs and hashes match; rank and value checks pass. |
| MJ remote gate V2 | Passed | 8,041 rows; BB partition unchanged; BC partition not written yet. |
| BC R3-HF1 package | Ready | Hotfix package prepared with exact partition scope and runtime dependency guard. |
| Unified command dry-run | Passed | BB, MJ, and BC dry-run paths all succeeded. |
| Unified real no-publish SLA | Blocked safely | BB SQL exceeded the 120s SLA; fail-safe cancelled remote execution and prevented writes. |
| BB direct-select package | Ready | `bb_model006_v2_single_reducer_direct_select_20260810_v3` is ready for DSW upload after local packaging validation; compressed checksum `3ef72bfe7537c3280864abf6f90e7f2b2c5359b6bb24c5556c83f5fbbe1cdfda` is tracked. |
| BB single-reducer candidate | Pending remote gate | `bb_model006_v2_single_reducer_direct_20260810_v1` is local-verified; promotion waits for remote validation. |
| Scratch-table handoff | Ready | Uses isolated scratch table, authoritative 147-column schema, exact `run_id` partition cleanup, and no shared-table mutation privilege. |
| Three-game workbook | Passed | 40,331 total rows; BB 27,362 / MJ 8,041 / BC 4,928; all identity contracts pass and formula errors are 0. |

## Three-Game Workbook Distribution

```mermaid
xychart-beta
    title "Validated rows in combined review workbook"
    x-axis ["BB", "MJ", "BC"]
    y-axis "Rows" 0 --> 28000
    bar [27362, 8041, 4928]
```

## Evening Deployment Gate Flow

```mermaid
flowchart LR
    A["BB model version frozen"] --> B["Direct-select package ready"]
    A --> C["Single-reducer candidate local verified"]
    C --> D["Remote gate pending"]
    B --> E["DSW upload ready"]
    F["Scratch schema handoff"] --> G["Isolated run_id partition cleanup"]
    H["Three-game workbook"] --> I["Identity contracts passed"]
```

## 2026-08-07 Model Training Snapshot

| Game | Completed runs | Runtime | Main signal |
|---|---:|---:|---|
| Block Blast | 8 | 4h 57m 25s | Full CatBoost rank/positive, trajectory, retention, recency, stacker, and growth-interaction checks. |
| Block Crush | 9 | 1h 13m 26s | LightGBM baseline, seed stability, Tweedie, recency weighting, weekday amount, CatBoost migration, and deep-capacity checks. |
| Mahjong Tile | 1 | 15m 51s | C17 trajectory challenge model; C8 remains the official frozen baseline until fresh OOT validation. |
| Total | 18 | 6h 26m 42s | Successful runs are separated from interrupted, failed, scoring-only, and calibration-only work. |

## Readable Progress Snapshot

```mermaid
quadrantChart
    title Internship work maturity snapshot
    x-axis Low deployment readiness --> High deployment readiness
    y-axis Low analysis depth --> High analysis depth
    quadrant-1 Production candidates
    quadrant-2 Research-heavy
    quadrant-3 Early exploration
    quadrant-4 Engineering polish
    "DataWorks audit": [0.65, 0.78]
    "Feature engineering phases": [0.72, 0.82]
    "Block Blast GP final reports": [0.78, 0.86]
    "MahjongTile model variants": [0.70, 0.88]
    "C17 scoring package": [0.88, 0.68]
    "BC V6 shared-hourly release": [0.86, 0.74]
    "Shared scoring contract": [0.90, 0.80]
    "Unified command fail-safe": [0.72, 0.86]
    "BB direct-select package": [0.88, 0.78]
    "Scratch safety handoff": [0.84, 0.76]
    "Combined workbook validation": [0.86, 0.72]
    "GitHub profile sync": [0.82, 0.55]
    "2026-08-07 training log": [0.76, 0.92]
```

## Public Boundary

- The charts show progress categories and public-safe artifact types.
- Raw business data, credentials, private repository details, internal URLs, and unreviewed sensitive tables are not published.
- Visual summaries are updated together with the daily work log three times per day.
