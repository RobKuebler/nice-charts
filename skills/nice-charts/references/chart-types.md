# Niche Chart Types: When to Use & Key Rules

Reference these when the user asks about one of the chart types below. For common chart types (line, bar, scatter, pie, choropleth, heatmap, box plot, bullet graph, radar, Gantt) see the main SKILL.md.

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
