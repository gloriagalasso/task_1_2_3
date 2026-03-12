# Task 2 — Measure Overlap Intensity

## Descriptive Statistics and Distribution of Overlap

### Overall Counts

| Metric | Value |
|---|---|
| Total (patent_id, focal_term) pairs | 790 |
| Unique patents | 101 |
| Unique focal term strings | 494 |

> Note: 790 pairs across 101 patents but only 494 unique term strings — the same term (e.g. *"cell"*) can be a focal term in multiple patents.

### Distribution of Focal Terms per Patent

| Statistic | Value |
|---|---|
| Mean | 7.82 |
| Median | 6.00 |
| Std Dev | 6.83 |
| Min | 1 |
| 25th percentile | 3 |
| 75th percentile | 11 |
| Max | 30 |

### Interpretation

The 101 patents share on average **7.8 focal terms** with their cited scientific papers (median = 6), totalling **790 unique (patent_id, focal_term) pairs**. The distribution is **right-skewed**: most patents have few focal terms, but a small number have many.

- **25% of patents** have ≤ 3 focal terms → weak overlap with cited science
- **50% of patents** have ≤ 6 focal terms → moderate overlap
- **75% of patents** have ≤ 11 focal terms → only a minority shows strong overlap
- The high std (6.83 ≈ mean) confirms **high variability** across patents

### Illustrative Examples

| Patent ID | Focal Terms (n) | Example Terms |
|---|---|---|
| 7749408 | 1 (min) | *"room"* — very low terminological overlap |
| 7884261 | 6 (median) | *"increase", "plant", "promoter", "rice", "transgenic", "yield"* — typical moderate overlap in agricultural/biological science |
| 8280136 | 30 (max) | *"cardiac", "heart", "dyssynchrony", "myocardial", "device", "model", ...* — strongly grounded in medical/cardiac scientific literature |

### Visualisations

- `visualizations/histogram_focal_terms.png` — histogram of focal terms per patent with mean and median lines
- `visualizations/density_focal_terms.png` — KDE density plot of the same distribution
