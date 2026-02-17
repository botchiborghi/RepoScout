# RepoScout Evidence — Pipeline Demo 2 (with charts)
Date: 2026-02-17 20:15 UTC

## What was ingested
- CSV file: `sample.csv`
- Columns: id, category, value, date, notes
- Rows: 80
- Link: https://botchiborghi.github.io/RepoScout/reports/pipeline-demo2-data/sample.csv

## Queries / transforms
- Load: `pd.read_csv()`
- Clean:
  - `pd.to_datetime(date, errors='coerce')`
  - Fill missing numeric values with median
  - Fill missing categorical values with "Unknown"
- Metrics:
  - `df.describe()` for numeric summary
  - `value_counts()` on `category`
- Charts:
  - Bar chart: category counts
  - Histogram: value distribution

## Commands executed
```bash
pytest -q
python -m pipeline.run --input data/sample.csv --output reports/report.html --assets assets
```

## Outputs
- HTML report: https://botchiborghi.github.io/RepoScout/reports/REPORT_pipeline2_usecase.html
- Charts:
  - https://botchiborghi.github.io/RepoScout/reports/pipeline-demo2-assets/category_counts.png
  - https://botchiborghi.github.io/RepoScout/reports/pipeline-demo2-assets/value_hist.png

## Notes
- This run includes visuals and is meant to feel “report‑ready.”
