# Hungry Studio Internship Visual Summary

Last synced: 2026-08-07 17:45 Asia/Shanghai

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
    BC / BB / MJ full-data training              :active, 2026-08-07, 1d

    section Deployment
    Scoring package and SQL hotfix archives      :active, 2026-08-07, 1d
    GitHub profile auto-sync                     :active, 2026-08-07, 1d
```

## Deliverable Mix

```mermaid
pie showData
    title Public deliverable categories
    "SQL and DataWorks audits" : 14
    "Feature engineering specs" : 12
    "Model evaluation reports" : 18
    "Visualization reports" : 10
    "Deployment packages" : 4
    "Work logs and documentation" : 8
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
    H --> I["Public work-log deployment"]
```

## Work Content vs Work Output

| Area | Work Content | Work Output |
|---|---|---|
| Data audit | Checked table scale, field quality, missingness, time-window boundaries, and leakage risk. | DataWorks SQL, TSV evidence tables, audit JSON, data-quality reports. |
| Feature engineering | Built staged Block Blast GP feature plans and reduced redundant or unstable features. | Feature specs, manifests, phase SQL, redundancy/stability CSVs, processing reports. |
| Modeling | Compared model variants across ranking, amount prediction, device hierarchy, CPI/manufacturer/RAM, and country/device/carrier settings. | Metrics CSVs, feature importance, SHAP-style reports, robustness checks, holdout predictions. |
| Visualization | Built readable HTML/PDF/PNG summaries for audits, feature behavior, OOT maturity, ablation, and final model effect. | Visual reports, comparison charts, full-stage workflow summary PDFs. |
| Deployment | Prepared MahjongTile hourly scoring package, model manifests, SQL hotfixes, and deployment archives. | `mahjongtile_hourly_model`, C17 deploy update archive, C17 SQL hotfix archive. |
| Profile sync | Maintained public GitHub profile logs for daily internship work. | `README.md`, `DAILY_WORK_LOG.md`, internship log, visual summary, scheduled sync task. |

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
    "GitHub profile sync": [0.82, 0.55]
```

## Public Boundary

- The charts show progress categories and public-safe artifact types.
- Raw business data, credentials, private repository details, internal URLs, and unreviewed sensitive tables are not published.
- Visual summaries are updated together with the daily work log three times per day.
