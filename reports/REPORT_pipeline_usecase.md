# RepoScout Evidence — Pipeline Demo (baseline)
Date: 2026-02-17 20:11 UTC

## What was ingested
- CSV file: `sample.csv`
- Columns: id, category, value, date, notes
- Rows: 60
- Link: https://botchiborghi.github.io/RepoScout/reports/pipeline-demo-data/sample.csv

## Queries / transforms
- Load: `pd.read_csv()`
- Clean:
  - `pd.to_datetime(date, errors='coerce')`
  - Fill missing numeric values with median
  - Fill missing categorical values with "Unknown"
- Metrics:
  - `df.describe()` for numeric summary
  - `value_counts()` on `category`

## Commands executed
```bash
pytest -q
python -m pipeline.run --input data/sample.csv --output reports/report.html
```

## Outputs
- HTML report: https://botchiborghi.github.io/RepoScout/reports/REPORT_pipeline_usecase.html

## Notes
- This is a minimal baseline run to validate end‑to‑end flow.
