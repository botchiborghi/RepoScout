# RepoScout Evidence — Pipeline Demo 2 (airquality time series)
Date: 2026-02-18 01:30 UTC

## What was ingested
- CSV file: `airquality.csv`
- Source: https://vincentarelbundock.github.io/Rdatasets/csv/datasets/airquality.csv
- Local copy: https://botchiborghi.github.io/RepoScout/reports/pipeline-demo2-data/airquality.csv
- Columns: rownames, Ozone, Solar.R, Wind, Temp, Month, Day
- Rows: 153

## Queries / transforms
- Load: `pd.read_csv()`
- Clean:
  - `pd.to_datetime` not applicable (dataset has Month/Day columns)
  - Fill missing numeric values with median
- Metrics:
  - `df.describe()` for numeric summary
  - `value_counts()` on `category` (not used for this dataset)
- Charts:
  - Histogram: `value` (not present) → replaced by histogram of `Ozone`
  - Bar chart: counts by `Month`

## Commands executed
```bash
pytest -q
python -m pipeline.run --input data/airquality.csv --output reports/report.html --assets assets
```

## Outputs
- HTML report: https://botchiborghi.github.io/RepoScout/reports/REPORT_pipeline2_usecase.html
- Charts:
  - https://botchiborghi.github.io/RepoScout/reports/pipeline-demo2-assets/category_counts.png
  - https://botchiborghi.github.io/RepoScout/reports/pipeline-demo2-assets/value_hist.png

## Notes
- Dataset is a classic air quality time series (May–Sep, daily observations).
- This run uses a real public dataset instead of synthetic data.
