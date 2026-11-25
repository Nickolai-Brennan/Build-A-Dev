---
name: data-visualization
description: Build and verify charts or dashboard views from tabular data. Use when asked to visualize a metric, compare groups, show trends or distributions, or add a chart to a web app.
---

# Build a data visualization

1. Identify the question, grain, units, population, time window, filters, and source. Inspect the data or schema before picking a chart. If data is unavailable, produce a chart specification and mark any examples as synthetic.
2. Define the aggregation, denominator, and missing-value rule before plotting. Keep missing periods distinct from zero observations. For a percentage, state which records qualify for the denominator.
3. Use a line chart for time, bars for group comparisons, a histogram for distributions, or a scatterplot for paired observations. Keep labels and units visible, and offer access to exact values through the app's existing table or chart details.
4. Reuse the app's chart library and data contract. Define the loading, empty, and error states. Verify that filter changes update the displayed values and the labels together.
5. Compare at least one plotted value to a direct calculation from the source. Report the source, formula, coverage, and how to verify the chart.
