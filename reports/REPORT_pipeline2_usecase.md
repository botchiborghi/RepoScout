# RepoScout Use Case Run — pipeline demo 2 (with charts)
Date: 2026-02-17 20:15 UTC

## Use case
**Goal:** Ingest CSV → clean → compute metrics → generate HTML report **with charts**.

## Setup
- Python venv + pandas + matplotlib
- Sample dataset: 80 rows, 5 columns (id, category, value, date, notes)

## Commands
```bash
pytest -q
python -m pipeline.run --input data/sample.csv --output reports/report.html --assets assets
```

## Results
- ✅ Tests: **3 passed**
- ✅ Report generated: `reports/report.html`
- ✅ Charts generated: `assets/category_counts.png`, `assets/value_hist.png`

## Output preview
- Category bar chart + value histogram
- HTML report embeds chart images (see link)

## Value
- Demonstrates full analysis + visualization pipeline end‑to‑end
- Easy to extend with new metrics or charts
