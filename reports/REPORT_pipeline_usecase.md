# RepoScout Use Case Run — pipeline demo
Date: 2026-02-17 20:11 UTC

## Use case
**Goal:** Ingest CSV → clean → compute metrics → generate HTML report.

## Setup
- Python venv + pandas
- Sample dataset: 60 rows, 5 columns (id, category, value, date, notes)

## Commands
```bash
pytest -q
python -m pipeline.run --input data/sample.csv --output reports/report.html
```

## Results
- ✅ Tests: **3 passed**
- ✅ Report generated: `reports/report.html`
- Rows processed: 60

## Output preview
- Category counts, numeric summary tables
- HTML report produced locally (see link)

## Value
- Demonstrates the full pipeline flow end-to-end
- Cheap to run, easy to extend
