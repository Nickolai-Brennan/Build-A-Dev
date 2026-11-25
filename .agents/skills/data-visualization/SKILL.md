---
name: data-visualization
description: Build or review a data visualization project, dashboard, or chart from a reproducible metric and tabular data.
---

# Data Visualization Project

1. Identify the audience, question, data source, grain, units, population, time window, and filters. Inspect source coverage and define aggregation, denominator, and missing-value rules before plotting. If source data is unavailable, provide a specification and label sample data as synthetic.
2. Choose encodings for the question. Keep exact values available and retain the difference between missing data and true zero. Delegate product integration to the relevant visualization specialist when supported. Start with lines for trends, bars for comparisons, histograms for distributions, and scatterplots for paired observations.
3. Implement using the app's existing chart library and contract. Verify loading, empty, error and success states and check filters update both the values and labels.
4. Reconcile at least one displayed value against a source calculation and record the formula, data coverage, filters, reproducibility steps, and any limits.

Report the files changed, verification run, and any unavailable environment or access.

[Product documentation](https://www.data-to-viz.com/)
