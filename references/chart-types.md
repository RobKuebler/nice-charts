# Chart Types: Design Rules Reference

Design rules for chart types not covered inline in SKILL.md. Read the relevant section when one of these comes up.

---

## Scatter Plot

- Use for paired numerical data to reveal correlation, clustering, or outliers between two continuous variables.
- Add a trend line to make the direction and strength of correlation explicit.
- **Critical caveat: correlation ≠ causation.** Always acknowledge that an unseen variable may explain the pattern.
- Use a bubble chart when a third numerical variable should be encoded as circle size.
- For overlapping points in dense data, use transparency, jitter, or a 2D density/hexbin plot instead.

## Box & Whisker Plot

- Shows median, quartiles, and outliers at a glance — compact enough to compare many groups side by side.
- Use to compare distributions across groups (e.g., salary by department, test scores by school).
- Better than a bar chart for showing spread; more compact than a histogram for group comparisons.
- Outliers plotted as individual dots reveal anomalies immediately.
- Limitation: doesn't show the *shape* of the distribution. If bimodality or skew matters, use a violin plot.

## Heatmap

- A matrix (rows × columns) where each cell's color encodes a third variable.
- Use for: temperature by city × month, activity by day × hour, correlation matrices.
- Good for spotting patterns and overall trends; poor for reading precise values — color perception is imprecise.
- Show data values directly in cells whenever exact numbers also matter.
- A legend is essential. Limit to a single sequential or diverging scale per heatmap.
- Sort rows and columns intentionally — clustering similar values reveals patterns that default alphabetical order hides.

## Bullet Graph

- A compact bar with a target line and background performance bands — the space-efficient alternative to gauge/speedometer charts.
- Use for KPI dashboards where you need actual vs. target in minimal space.
- Keep background performance bands to a maximum of 5 shades; more becomes unreadable.
- Audiences unfamiliar with the format may need a one-line explanation in the chart description.

## Radar / Spider Chart

- Frequently misused — direct comparison between non-adjacent axes is nearly impossible on a radial layout.
- **Better alternatives:** small multiples of bar charts or parallel coordinates for multivariate comparison.
- Only use when: (a) you have 5–10 variables of the same unit, (b) the overall *profile shape* is the message, (c) comparing at most 2–3 groups.
- Never fill polygons when showing multiple series — the top polygon covers those beneath it. Use transparent outlines.

## Gantt Chart

- Tasks as horizontal bars on a time axis; shows duration, sequence, dependencies, and parallel workstreams.
- The standard for project planning, roadmap communication, and editorial production schedules.
- Add dependency arrows to show which tasks block others. Add a vertical "today" line for current status.
- Filter to milestone-level for executive audiences — too many tasks creates an unreadable wall.

---

## Niche Chart Types

Reference these when one of the less common types below comes up.

---

## Violin Plot

- Combines box plot statistics with density curves showing the full distribution shape on both sides.
- Use when you need to see if a distribution is bimodal, skewed, or multimodal — things a box plot hides.
- Requires sufficient data (at least ~30 points) to produce a meaningful density curve.
- More visually complex than a box plot — use a box plot when audience unfamiliarity is a concern.

## Span / Range Chart

- Horizontal bars showing min-to-max per category — makes the *spread* between extremes the visual focus.
- Use when the range itself is the message (temperature ranges, salary bands, price ranges by region).
- Shows only extremes — if you also need median or shape of distribution, use a box plot instead.

## Stream Graph

- A stacked area chart flowing around a centered baseline — emphasizes shape and flow over time.
- Use for high-volume, multi-category time series where the *overall wave pattern* is the story (e.g., music genre popularity over decades).
- Cannot be read precisely (no fixed baseline) — switch to a stacked area chart if readers need exact values.
- Works best in interactive contexts where hovering reveals values. Avoid as a static print chart.
- Small categories get buried under large ones — limit to 5–7 prominent categories.

## Network Diagram

- Nodes (entities) connected by edges (relationships) — maps how things are interconnected.
- Use to identify hubs (highly connected nodes), clusters, or shortest paths between entities.
- Falls apart with large datasets — dozens of crossing lines create unreadable "hairballs."
- For dense networks: filter to the most significant nodes/edges, or switch to a matrix adjacency view.

## Chord Diagram

- Entities arranged in a circle with curved arcs showing bidirectional flows or relationships between pairs.
- Use when the *proportion* of flows between each pair matters (e.g., migration between countries, trade between regions).
- Becomes unreadable beyond ~8–10 entities — prefer a Sankey diagram for directed flows with many categories.

## Bubble Map

- Proportional circles on a map where circle area encodes a value — avoids the distortion of large-area, low-value regions in choropleth maps.
- Use when absolute quantities matter more than density (e.g., total GDP, not GDP per capita).
- Always scale by **area**, not radius — scaling by radius makes large values appear far too dominant.
- Watch for overlap in dense regions; large bubbles obscure neighboring ones.

## Dot Map

- Individual dots on a map, one per data point or one per N, to show spatial distribution.
- Use to reveal clustering and where phenomena concentrate geographically (disease cases, business locations, events).
- Not for reading precise regional values — use a choropleth or bubble map for that.
- Dense areas create overlapping dots that hide rather than reveal. Use a one-to-many ratio to prevent this.

## Venn Diagram

- Overlapping circles showing which elements belong to multiple sets simultaneously.
- Use for showing shared membership across 2–3 sets with a qualitative focus.
- Maximum 3 sets — 4+ sets become geometrically impossible to read clearly.
- Not for precise quantitative comparisons; circles don't accurately scale to values.

## Word Cloud

- Words sized by frequency — primarily aesthetic.
- Long words get disproportionate visual weight regardless of actual frequency. Color is usually decorative.
- **Avoid for any serious analysis** — use a ranked bar chart of word frequencies instead.
- Acceptable for: general audience engagement pieces, brainstorming displays, tag/topic overviews where rough impression is enough.

## Parallel Coordinates Plot

- Multiple vertical axes side by side; each item drawn as a line crossing all axes.
- Use to compare many entities across many attributes simultaneously (e.g., cars by speed, weight, MPG, price).
- **Axis order matters** — relationships are only visible between adjacent axes; experiment with reordering.
- Becomes unreadable as a static chart with more than ~50 lines. Interactivity (brushing/highlighting) is essential for dense datasets.

## Timeline

- A chronological list of events on a time axis.
- Use for: historical narratives, project milestones, editorial timelines.
- Use a **scale-based** timeline (proportional spacing) when the intervals between events matter. Non-scaled timelines imply equal intervals when they're not.
- Combine with span bars to show event duration, not just start points.

---

## Bump Chart

- Shows rank order changes across many time periods (unlike a slope chart, which connects only two).
- Every entity gets a line; lines cross as ranks change. The y-axis is rank (1 = top), not a quantitative value.
- Best for: sports standings over a season, country rankings across years, poll position over an election campaign.
- Use a consistent color per entity across all time points. Bold the entity of interest; gray the rest.
- Label start and end points directly — mid-chart labels cause clutter when lines cross.
- Limit to ~10–15 entities before it becomes a tangle. More: filter to the most interesting ones.

## Calendar Heatmap

- A grid of days/weeks where each cell's color encodes a value. Typically one year = one row of weeks; each cell = one day.
- Use for: activity patterns over time (e.g., GitHub contributions, energy usage by hour/day, website traffic).
- Excellent at revealing weekly rhythms, seasonal patterns, and anomalous days at a glance.
- Not for reading precise values — color perception is imprecise. If exact numbers matter, use a table or line chart.
- Use a sequential color scale (light = low, dark = high). Diverging only if there's a meaningful midpoint (e.g., profit/loss by day).
- Add a clear legend. Month labels and day-of-week labels are essential for orientation.

## Fan Chart

- A line chart where the historical portion is a solid line and the future projection fans out into a cone of uncertainty — the cone widens the further forward it extends.
- Use when communicating forecast uncertainty is important: economic projections, epidemiological models, climate scenarios.
- The cone should represent genuine confidence intervals (e.g., 50%, 80%, 95%) — label them explicitly.
- Clearly mark the boundary between historical data and the projection with a vertical line or a color shift.
- Readers often misread the widening cone as showing a "range of outcomes" rather than uncertainty — explain in the subtitle what the bands represent.
- Don't use a fan chart just to add visual interest to a forecast. The uncertainty must be quantified and meaningful.

## Connected Scatter Plot

- A scatter plot where points are connected in chronological order, tracing how the relationship between two variables evolves over time.
- Use when you want to show both the correlation *and* how it changes (e.g., GDP vs. CO₂ emissions by year).
- The path itself tells the story — loops, reversals, and direction changes are the insight.
- Label start and end points, plus any key inflection points. Without labels the time direction is invisible.
- Works poorly with noisy data — the path becomes tangled. Consider smoothing before connecting.
- Compare to: scatter plot (no time), line chart (one variable over time). Connected scatter is the intersection of both.

## Dot Strip Plot

- Individual data points arranged along a single axis (or per-group axis). Every observation gets a dot.
- Use when: the dataset is small-medium (<200 points) and you want readers to see every individual value; or when comparing groups where both spread and individual outliers matter.
- Superior to a box plot for small samples where showing every point is possible.
- Jitter dots horizontally when values overlap (especially for discrete/integer data).
- Add a mean or median marker per group in a contrasting color so the center is still readable.
- Falls apart with very large datasets — points overlap into a solid mass. Switch to violin or histogram.

## Cumulative Curve

- The y-axis shows the cumulative share of a total; the x-axis shows the cumulative share of the population sorted from lowest to highest value. The diagonal (45°) represents perfect equality.
- Classic use: Lorenz curve for income or wealth inequality. Also useful for showing how concentrated any distribution is (e.g., top 10% of customers = 80% of revenue).
- The further the curve bows below the diagonal, the more unequal the distribution.
- Label the diagonal explicitly as "perfect equality" so readers have the reference.
- Can compare multiple groups on one chart (each gets its own curve). Limit to 3–4 curves before it clutters.

## Cartogram (Equalised)

- Every geographic unit (country, state, constituency) is redrawn as an equally-sized shape — usually a square or hexagon. Geography is sacrificed for representational equality.
- Use when each unit should carry the same visual weight regardless of physical size (election results by constituency, policy comparisons by country).
- The challenge: spatial arrangement should still loosely reflect actual geography so readers can orient themselves.
- Label every unit (or at least key ones) — readers can't rely on shape recognition as they would with a normal map.
- Pair with a conventional map in an inset so readers can switch between the two framings.

## Cartogram (Scaled / Value-by-Area)

- Geographic boundaries are stretched and shrunk so each area's physical size is proportional to a data value (e.g., population, GDP).
- Use to directly counteract the misleading visual dominance of large-but-sparse regions in choropleth maps.
- The distortion is the message — use it to make the contrast between data value and physical area viscerally clear.
- Always show a conventional map alongside for orientation. The distorted version alone is hard to decode.
- Not for precise reading — the irregular shapes make exact comparison difficult. Pairs best with tooltips.
