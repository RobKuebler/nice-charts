# nice-charts

A Claude Code skill that prevents common data visualization mistakes and guides toward the right chart for the right problem.

## What It Does

Claude automatically applies this skill whenever a chart, graph, or visualization is being created, evaluated, or improved. It catches beginner mistakes before they happen — like using a pie chart with 12 segments, truncating a bar chart's Y-axis, or picking the wrong chart type for the data.

Covers:
- Chart type selection (which chart for which goal)
- Color scales and accessibility
- Y-axis rules (bar vs. line charts)
- Typography and text placement
- Layout and small multiples
- Common mistakes and how to fix them

Based on Datawrapper's editorial guidelines.

## Usage

Just describe what you want to visualize — the skill activates automatically:

```
"I have sales data for 8 products and want to show market share"
"My line chart starts at 0 but all values are between 85k and 92k"
"Which chart type is best for showing correlation?"
"My pie chart has 12 slices and looks terrible"
```

## Installation

```
/plugin install RobKuebler/nice-charts
```
