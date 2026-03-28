---
name: nice-charts
description: >-
  Prevents common data visualization mistakes and guides toward the right chart
  for the right problem. Covers chart type selection, color scales, axes,
  typography, layout, and accessibility — based on Datawrapper's editorial
  guidelines.

  Use this skill whenever a chart, graph, diagram, or visualization is being
  created, evaluated, or improved — regardless of library or tool. Apply it for:
  chart type questions ("which chart for X?"), fixing bad charts ("my pie chart
  has 12 slices", "looks unprofessional"), color or axis problems, and any
  request to visualize data. Also triggers on German terms: Diagramm, Grafik,
  Balkendiagramm, Liniendiagramm, Kreisdiagramm, Säulendiagramm, Heatmap,
  visualisieren, darstellen. Use it even when the user doesn't mention design
  intent — the defaults here catch beginner mistakes before they happen.
---

# Nice Charts

Good charts do one thing: make a point land. Everything else — color, type, labels, layout — is in service of that.

## When this skill activates

This skill exists to prevent common chart mistakes — wrong chart type for the data, misleading axes, too many colors, missing context. Apply it whenever a chart is being created, suggested, or reviewed, regardless of library or tool.

**Workflow:**
1. Write the message in one sentence — this is your compass for every design decision
2. Choose the chart type that best communicates that message (→ Section 1)
3. Add comparison data so the reader has context ("comparisons are what make data vis into data vis")
4. Apply color and annotations to emphasize the main point
5. Verify: title states the message, legend is clear, source is cited

---

## 1. Choose the Right Chart Type

Match the chart to your goal:

| Goal | Best options | Avoid |
|------|-------------|-------|
| **Change over time** | Line chart, column chart (few time points), slope chart (first/last only), area chart (when totals matter) | Pie chart |
| **Proportions/shares** | Stacked bar, grouped bar, bar chart | Pie/donut (hard to compare) |
| **Comparing quantities** | Bar chart (horizontal scales better on mobile), dot plot | 3D anything |
| **Comparison vs. a target** | Bullet graph | Gauge/speedometer (wastes space) |
| **Correlation** | Scatter plot, bubble chart | Line chart |
| **Distribution (one group)** | Histogram, density plot | Pie chart |
| **Distribution (multiple groups)** | Box plot, violin plot, small multiples | Single histogram |
| **Multivariate comparison** | Heatmap, parallel coordinates | Radar/spider chart |
| **Range / min-max** | Span chart, box plot | Bar chart (hides spread) |
| **Geographic patterns** | Choropleth map (relative data), bubble map (proportional values), dot map (density/clustering) | Choropleth for absolute counts |
| **Flow / Sankey** | Sankey/alluvial diagram, chord diagram | Pie chart |
| **Relationship / network** | Network diagram | — |
| **Survey / Likert data** | Stacked bar | Pie chart |
| **Hierarchical data** | Treemap, Marimekko, sunburst | Stacked pie |
| **Age/gender breakdowns** | Population pyramid | — |
| **Project planning / schedules** | Gantt chart | — |
| **Event sequence (qualitative)** | Timeline | Line chart |
| **Set overlap / membership** | Venn diagram (≤3 sets) | — |
| **Text / tag frequency** | Bar chart of frequencies | Word cloud (for analysis) |

**Rules:**
- Prefer familiar chart types (bar, line, scatter) — unusual types require reader learning curves. Introduce complexity gradually.
- Bar charts > column charts on mobile (grow vertically, not horizontally).
- Pie/donut charts only work when: (a) values sum to 100%, (b) there are ≤ 5 slices, and (c) differences are obvious. Two-value data? State the percentage in text instead.
- Small multiples (separate panels per category) beat spaghetti line charts when 4+ lines overlap.
- When data is simple, let it be simple — don't add complexity where it doesn't exist.

---

## 2. Chart-Type Design Rules

### Line Charts

- **Time data only.** Never use a line chart for comparing values across categories — use bars.
- Line charts don't require starting at zero (unlike bar charts). Show the range that matters.
- If data approaches zero, include the baseline so readers can compare against it.
- If showing percentages near 100%, extend the y-axis to 100%.
- Add context: comparison data (averages, benchmarks, other regions) makes the story visible.
- Use color, line width, and dashes to create hierarchy — gray de-emphasizes, saturation emphasizes.
- **Limit to 5–6 lines maximum.** More than that: use small multiples.
- Add line symbols only if time intervals are inconsistent.
- Annotate transitions: highlight ranges when data switches from historical to projected.
- Use smoothing cautiously — curves can distort impressions. "Curved" is safer than "Curved (natural)."
- Labels: place manually for speed of reading; match label color to line color.

### Area Charts

- **Time data only.** Not for categorical comparisons.
- Use when both the totals and the breakdown matter. If only trends matter, use a line chart.
- Works best with large differences between values. Small differences → line chart.
- Use with 10+ time periods; fewer periods → stacked column chart.
- Place the most important series at the bottom with a distinct color (it has a stable baseline).
- Group minor series into "Others" to reduce clutter.
- Area charts are harder to read than line charts — always ask if a simpler type works.

### Stacked Column/Bar Charts

- Best when the focus is comparing **totals** and **one part of the total** across categories.
- Use for ≤ 10 categories. More than that: switch to stacked bars.
- Never include the total itself as a separate bar — it's already visible as the sum.
- Place the most important segment at the bottom (stable baseline for comparison).
- Place the second-most-important at the top (second baseline).
- Group minor segments into "Others."
- Use percentage stacking when relative proportions matter more than absolute values.
- If the total is irrelevant, a line chart is usually more readable.

### Pie & Donut Charts

- **Only use when:** values sum to 100%, there are ≤ 5 slices, and size differences are visually obvious.
- Best for values near 25%, 50%, or 75% — readers can recognize these proportions.
- For two values: state the percentage directly in text rather than drawing a chart.
- For comparisons across multiple datasets: switch to stacked bars.
- Color: highlight the key slice with a distinct color; use tints of one hue for the rest (not a rainbow).
- Use external labels for small slices.
- Group small slices into "Others."
- Place pie charts in sidebars or narrow columns — they create wasted white space at full width.
- Donut variant: the hole can hold a single key figure.
- Never use 3D effects, drop shadows, or exploded slices — they distort area perception and add no information.

### Choropleth Maps

- Use for regional patterns in **relative data** (rates, percentages, per-capita). Absolute numbers usually just show population density.
- Use the smallest geographic units available (counties > states) for more nuanced patterns.
- Consider cartograms when population distribution matters more than physical area.
- Use diverging color scales when both extremes relative to a midpoint are meaningful.
- Reserve the brightest and darkest colors for the data extremes.
- Continuous color scales can reveal more nuance than discrete class breaks.
- Always include tooltips with region name, value, and extra context.
- Add labels when readers may not know the geography.
- Color key must show at minimum: lowest value, highest value, and midpoint color.
- **Use a map only when geography is the insight.** If the pattern could be shown more clearly with a bar chart sorted by value, use the bar chart.

**Maps as guides** — when the map's purpose is to help readers navigate or orient:
- Include a major recognizable landmark beyond the focal area (a river, coastline, famous building) so readers know where they are in the world.
- Add a scale bar so readers can judge distances and plan logistics.
- Add directional arrows or labels pointing toward nearby major landmarks, even if they're off-map.
- Add operational specifics: entry/exit points, transport stops, opening times — anything the audience needs to act on the map.
- Imagine your specific audience's knowledge gaps. A local map for tourists needs far more hand-holding than one for specialists.

**Map annotations** — when adding text callouts to a map:
- Add ~5% padding around the map border so annotations don't crowd the edges.
- Remove generic background labels (city names, region names) that compete with your annotations. If your annotations already name enough places to orient the reader, the background labels are noise.
- Use **circles** to indicate regional patterns (a loose area); use **arrows** only when pointing to a specific data point or location.
- Match annotation marker colors to the map's data palette so they integrate visually instead of demanding attention. Annotations should sit on the map, not jump off it.
- Let readers explore annotations in any order — don't number them or force a reading sequence unless the order genuinely matters.

### Tables

When to use a **table** instead of a chart:
- Readers need to look up their own specific value (by location, age, name, etc.)
- Exact numbers matter for decisions (interest rates, prices, rankings)
- Two-way comparisons (comparing across both rows and columns)
- Ranking display — ordinal position doesn't need to be visualized

Design rules:
- More rows than columns — vertical scanning is easier than horizontal.
- **Right-align numbers, left-align text.** This makes columns of numbers scannable by magnitude without effort.
- Use consistent number formatting within a column: same decimal places, same thousands separator, same currency symbol.
- Round numbers aggressively. "1.3m" beats "1,300,000". Remove trailing zeros.
- Abbreviate column headers; use icons where possible to compress width.
- Use zebra striping (alternating light gray rows) only for wide tables with many columns.
- Adjust row height: spacious for few rows, compact for many.
- Add search and sort functionality when relevance varies by reader.
- Sort order is a design choice — default to what matters most (highest value, most recent, etc.).
- Color in tables: bright colors for text highlights; pale/pastel backgrounds for cells or rows.
- Add sparklines or small bar charts within cells to show trends without extra columns.
- Heatmap coloring works well for dense numeric grids.
- Pagination signals to readers that more rows exist — use it for long lists.
- Tables tell a story too: state your message in the title, don't just label the data.

### Scatter Plot

- Use for paired numerical data to reveal correlation, clustering, or outliers between two continuous variables.
- Add a trend line to make the direction and strength of correlation explicit.
- **Critical caveat: correlation ≠ causation.** Always acknowledge that an unseen variable may explain the pattern.
- Use a bubble chart when a third numerical variable should be encoded as circle size.
- For overlapping points in dense data, use transparency, jitter, or a 2D density/hexbin plot instead.

### Box & Whisker Plot

- Shows median, quartiles, and outliers at a glance — compact enough to compare many groups side by side.
- Use to compare distributions across groups (e.g., salary by department, test scores by school).
- Better than a bar chart for showing spread; more compact than a histogram for group comparisons.
- Outliers plotted as individual dots reveal anomalies immediately.
- Limitation: doesn't show the *shape* of the distribution. If bimodality or skew matters, use a violin plot.

### Heatmap

- A matrix (rows × columns) where each cell's color encodes a third variable.
- Use for: temperature by city × month, activity by day × hour, correlation matrices.
- Good for spotting patterns and overall trends; poor for reading precise values — color perception is imprecise.
- Show data values directly in cells whenever exact numbers also matter.
- A legend is essential. Limit to a single sequential or diverging scale per heatmap.
- Sort rows and columns intentionally — clustering similar values reveals patterns that default alphabetical order hides.

### Bullet Graph

- A compact bar with a target line and background performance bands — the space-efficient alternative to gauge/speedometer charts.
- Use for KPI dashboards where you need actual vs. target in minimal space.
- Keep background performance bands to a maximum of 5 shades; more becomes unreadable.
- Audiences unfamiliar with the format may need a one-line explanation in the chart description.

### Radar / Spider Chart

- Frequently misused — direct comparison between non-adjacent axes is nearly impossible on a radial layout.
- **Better alternatives:** small multiples of bar charts or parallel coordinates for multivariate comparison.
- Only use when: (a) you have 5–10 variables of the same unit, (b) the overall *profile shape* is the message, (c) comparing at most 2–3 groups.
- Never fill polygons when showing multiple series — the top polygon covers those beneath it. Use transparent outlines.

### Gantt Chart

- Tasks as horizontal bars on a time axis; shows duration, sequence, dependencies, and parallel workstreams.
- The standard for project planning, roadmap communication, and editorial production schedules.
- Add dependency arrows to show which tasks block others. Add a vertical "today" line for current status.
- Filter to milestone-level for executive audiences — too many tasks creates an unreadable wall.

> **Less common chart types** (violin plot, stream graph, network diagram, chord diagram, bubble map, dot map, span chart, Venn diagram, word cloud, parallel coordinates, timeline): read `references/chart-types.md` when one of these comes up.

---

## 3. The Y-Axis

- **Bar charts must start at zero.** The area of a bar encodes magnitude — truncating the axis lies.
- **Line charts don't have to start at zero.** Show the range that's meaningful for the data.
- Label the zero baseline with words when it's not obvious what zero means ("Employment as of Q3 2023", not just "0").
- When showing indexed or relative data, explain what the baseline represents: "–5% from the national average."
- Use consistent formatting throughout — if one axis label shows "–11%", all labels show "%" including tooltips.
- Extend y-axes to 100% when showing percentages that approach that threshold.
- Signal explicitly when panels in small multiples have different y-axis scales — readers assume they're the same.
- **Use a logarithmic scale** when data spans multiple orders of magnitude (e.g., population by country, revenue from $1k to $1B). A linear axis compresses smaller values into invisibility.
- **If you must truncate an axis**, mark the break with a visible jagged line (≈) so readers know the scale is interrupted — never truncate silently.

---

## 4. Color: The Most Powerful Tool

Color controls where readers look. Use it deliberately.

### Pick the right scale type

**Qualitative (hues)** — unordered categories (countries, parties, industries):
- Use distinct hues with varied lightness so they survive grayscale/colorblind printing.
- **Max 7 colors in one chart.** More than that forces readers to constantly reference the legend.
- 5–6 colors is the practical ceiling for comfort. More: merge categories, use gray, or switch chart type.

**Sequential (gradient)** — one direction of data (income, temperature, age, density):
- Light → dark reads intuitively as low → high.
- Multi-hue gradients (e.g., yellow → orange → red) show more contrast than single-hue.
- Build gradients through lightness changes, not hue alone.
- Default to this for choropleth maps when data has no meaningful midpoint.

**Diverging (two-ended gradient)** — data with a meaningful midpoint:
- Use when zero, 50%, an average, or a threshold carries meaning.
- Both extremes should be dark; midpoint bright/neutral (light gray is ideal).
- Always label the midpoint in the color key — don't make readers guess.
- Example use cases: profit/loss, election margins, temperature anomaly vs. average.

### Use fewer colors

Before adding a new color, ask: *what job is this color doing?*

- **Gray is your friend — and your most important color.** Make less important categories gray. Readers look at the most saturated color first, then slightly less saturated, then grays. Build hierarchy through saturation, not by adding more hues.
- **One highlight color** is often enough. Color the category you're talking about; gray everything else.
- **Shades of one hue** can replace multiple hues when categories are subcategories of the same thing.
- **Labels can replace color.** Direct labels eliminate the need to differentiate by color.
- **Small multiples** give each category its own panel, removing the need to distinguish by color at all.
- **Soft/desaturated palettes** can carry the same associations as bright ones, with less visual noise.

### Use color to emphasize

- The most saturated, darkest color draws the eye first on a light background.
- Don't use a different hue to de-emphasize — that implies categorical difference. Use a desaturated version of the same hue, or gray.
- Opacity can soften emphasis while keeping the hue.
- If everything is highlighted, nothing is.
- Maintain **consistent colors across related charts** — same variable = same color across an entire article or dashboard.
- **Avoid color conflicts:** if a background region is blue (e.g., a Democrat shading), don't also use blue for a data line. The same hue serving two different meanings will confuse readers — split the data or change one of the colors.
- **Use opacity + stroke width together to create data hierarchy.** For charts with primary and secondary series (e.g., raw data vs. smoothed average), reduce opacity on the secondary and increase stroke width on the primary. Readers will naturally focus on the bolder element.

### Color and cultural associations

Leverage intuitive associations; don't fight them:
- Red = danger, urgency, negative; Green = positive, environment
- Blue = safe, neutral baseline
- Avoid stereotypical pink/blue for gender data — use a different pair
- Use contextually obvious colors for political parties where conventions exist

Contrast requirements:
- Avoid complementary pairs (red/green, orange/blue) at similar brightness — they vibrate.
- Never use a bright or saturated background — it reduces text contrast and visual fatigue.
- Maintain contrast ratio ≥ 2.5:1 for large text, ≥ 4:1 for small text.

### Interpolation for maps

- **Linear (equal steps):** Good default for fairly uniform distributions. Outliers can flatten everything else.
- **Quantile (equal counts):** Best when data has extreme outliers. Shows geographic variation, but can exaggerate differences.
- **Natural breaks (Jenks):** Best balance — groups similar values, separates distinct ones.
- Always warn readers if y-axis scales or color scales differ between panels.

### Accessibility

- Always test palettes with a colorblind simulator (Viz Palette, Coblis, Color Oracle, or Datawrapper's built-in check).
- "Get it right in black and white" — if the chart is unreadable in grayscale, the lightness contrast is too low.
- Blue is the safest hue for all colorblind readers. Blue + orange is the go-to colorblind-safe pair for two-category comparisons.
- Meet WCAG contrast ratios for any text colored with a data color.
- **Non-color encodings for colorblind safety:** vary shapes (scatter plots), line dashes (line charts), patterns/textures (maps), or symbol overlays. These also improve charts for all readers.
- Max 3–4 colors for highest safety; use direct labels to eliminate color-dependency entirely.

---

## 5. Color Keys & Legends

The color key's job: readers should understand what a color means within 2 seconds.

- **Direct labels beat legends.** Label lines, bars, and regions directly whenever space allows. This eliminates eye travel entirely.
- **Place the key near the data.** In digital: never make readers scroll more than one screen height to find the key. Sticky keys that float while scrolling are excellent.
- **Repeat keys.** In a scrollytelling piece or multi-chart article, repeat the color key. Readers won't be annoyed; they will abandon a chart they can't decode.
- **Integrate colors into text.** Embed colored category names in chart titles and descriptions using HTML/CSS. This reinforces meaning without a separate legend block.
- **For quantitative scales:** label only distinct values — skip redundant intermediate labels. Add "and up" or "or more" for open-ended ranges. Consider using "less / more" instead of precise values when the specific numbers aren't the point.
- **Match key appearance to chart:** if bars have outlines or patterns, show those in the key too.
- **For categorical keys:** grid layout > horizontal list (easier to skim). Order items to match their order in the chart.
- **Legends should explain the measure**, not just the category name — "% unemployed" beats "Value."

---

## 6. Typography & Text

Text is load-bearing. It's not decoration.

### Font selection

- **Sans-serif for everything.** Clean, scannable, especially for numbers. Good free options: Roboto, Lato, Open Sans, Source Sans Pro, Noto Sans.
- **Serif** is occasionally acceptable for titles to convey editorial sophistication — never for data labels.
- **Lining figures** (uniform number height) over oldstyle figures for all data labels.
- **Tabular figures** (fixed-width digits) for any column of numbers — alignment matters.
- **Regular or medium weight** for body text; bold only for titles and key values.
- **Minimum 12px** for any text. Below that, most typefaces become unreadable.
- **Avoid thin/light weights** — they fade at small sizes or on non-retina screens.
- **Normal-width fonts only.** Never use condensed variants to save space — reduce font size instead.
- **No all-caps** except short labels (axis ticks, map region codes) — always with increased letter-spacing.
- **Verify symbol support:** ensure the font contains accented characters, currency symbols, and math operators.

### Text placement

- **Label directly.** Remove the legend and put labels next to the data elements they describe.
- **Units everywhere.** Put units in axis labels, tooltips, and annotations. Use abbreviations: "20k", "€12m", "3.4% unemployed" (not "3.4%").
- **Horizontal text only.** Rotated axis labels are hard to read. Abbreviate or flip the chart instead.
- **Left- or right-align.** Center-aligned text creates jagged edges and is harder to scan.
- **Tooltips should explain, not just report.** "3.4% unemployed in October 2023" beats "3.4%".
- **Avoid excessive decimal places.** "27%" beats "27.0%". Abbreviate large numbers. Remove thousands separators when the precision isn't needed.
- **Use plain language.** Explain as you would to a friend, not as an official data description. Reserve precise statistical terminology for secondary text or footnotes.

### Visual hierarchy

Only two prominence levels for annotations/labels:
1. **Primary:** big, bold, high-contrast (near-black) — titles, key values
2. **Secondary:** small, regular weight, gray — axis labels, source notes

Reserve the highest contrast for the thing the reader needs most. A source note should barely be noticed.

### The four text elements and their jobs

Each element in a chart has a distinct job — don't duplicate:
1. **Title** — states the main point or question ("Unemployment rose sharply in Q3", not "Unemployment rate, 2020–2024")
2. **Subtitle** — provides context the title can't fit: date range, filters applied, unit of measurement, definitions ("Seasonally adjusted, 2020–2024 · Source: BLS")
3. **Legend/color key** — explains what each color means, including the measure (not just the category label)
4. **Footnote** — minimal; data source and any essential methodological caveats only
5. **Annotations** — orient readers, explain design choices, call out outliers, add context

### Annotation style

- Annotations explain design choices, highlight outliers, add context. Use them generously.
- Keep annotations short. "US highest Q3" beats "The United States had the highest value in Q3."
- Use text outlines (background-colored stroke) when annotation text overlaps data elements.
- Avoid center alignment. Left-aligned annotation blocks feel more editorial and less cluttered.
- Distinguish between things that directly follow from the data vs. supplementary context you're adding — position them differently (subtitle vs. footnote).

---

## 7. Respecting Readers' Time

The extra time you spend making a chart understandable is time you save every reader.

- **Tell readers what to see.** Don't assume they'll find your insight — state it explicitly in the title or annotation. This also forces you to be clear about your own purpose.
- **Minimize eye travel.** Labels next to data beats a distant legend. Annotation next to the data point beats a caption.
- **Repeat key information.** Most readers don't read descriptions first — embed context directly in the chart elements. In multi-chart pieces, repeat the color key so readers never have to scroll back.
- **Make unfamiliar quantities relatable.** Compare to something the reader knows: "equivalent to the area of Germany," "about one coffee per day."
- **Add reference lines to answer "is this good or bad?"** A subtle line for the target, average, previous year, or a regulatory threshold gives readers the benchmark they need without adding text.
- **Remove everything that doesn't earn its place.** Gridlines, borders, tick marks, extra colors — every element that doesn't add meaning dilutes the message.
- **For interactive/complex charts, add alt text or an on-page text summary.** Describe the trend or insight ("Unemployment peaked at 14.7% in April 2020"), not just the chart elements. This serves screen readers and also readers who can't load images.

---

## 8. Layout & Small Multiples

### When to use small multiples

Use small multiples (same chart, one panel per category) when:
- 4+ lines overlap and become a spaghetti chart
- You want to compare trends/shapes, not exact point values
- Categories have very different magnitudes and you want to show relative shape
- You're telling a sequential story (before → during → after) — think comic strip panels

Don't use them when readers need to compare exact values at specific time points — a single chart with a shared axis is better for that.

### Small multiple design rules

- **Show all lines in background gray.** Each panel highlights one category, but all others appear as thin gray lines for context. This lets readers compare without switching panels.
- **Sort panels intentionally.** By start value, end value, range, % change, or alphabetically — the sort order creates a second narrative layer.
- **Keep text short.** Panel titles are abbreviations, not sentences.
- **Signal different scales explicitly.** If panels use independent y-axes (for different magnitudes), say so prominently: "Note: y-axis scales differ between panels."
- **Test on mobile.** Many small multiples become scroll traps on small screens. Cap the panel count if needed.
- **Smaller panels** work well with fewer data points — the eye can detect variation in position and pattern even at small resolution.
- **Limit the number of panels** to those that support the message — don't show 30 panels when 6 tell the story.

### Sequential storytelling

- Structure multiple panels like a comic strip: each panel builds on the last.
- Reorder panels so the sequence tells the story, not just alphabetical or default order.
- Use color to clarify role — one hue for one "direction" of data, another for the opposite.
- Add annotations that explain the connection between panels, not just what's in each one.

---

## 9. The One-Sentence Test

Before you finish, write your chart's message in one sentence. Then check:

- **Does the title say it?** Titles should be statements ("Unemployment rose sharply in Q3") not descriptions ("Unemployment rate, 2020–2024").
- **Does the color support it?** The most important category should be the most visually prominent.
- **Does the layout support it?** Panels, annotations, and emphasis should guide readers toward that sentence, not away from it.
- **Could you remove something?** Every element that doesn't earn its place dilutes the message. Remove it.
- **Squint test:** step back (or blur your eyes) and look at the chart. The most important element should still be obvious. If a different element jumps out first, your visual hierarchy is inverted.
- **Preattentive check:** the eye reads these attributes before conscious thought — color, size, position, and length. Whatever carries your main message should win on the most powerful attribute. Color is the strongest attention-getter; position (upper-left, center) is where eyes naturally land first; size signals importance; length encodes quantity most accurately. Misaligning these — making unimportant things big or brightly colored — is the most common emphasis error.

**When simplicity isn't the answer:** Not every chart needs to collapse to a single clear takeaway. For rich, exploratory data (long historical time series, many overlapping events, data readers will want to dig into), a "wimmelbild" approach works well — pack in all the labels, names, and event annotations and let readers explore at their own pace. The key signal: if readers are likely to ask "wait, which one is that?" repeatedly, label everything upfront rather than stripping labels in the name of simplicity.

---

## Quick Reference: Common Mistakes

| Mistake | Fix |
|---------|-----|
| Too many colors | Gray everything except 1–2 key categories |
| More than 7 colors | Merge categories or switch chart type |
| Rotated axis labels | Abbreviate labels or use a horizontal bar chart |
| Legend far from data | Direct labels, or sticky/integrated legend |
| Pie chart with 6+ slices | Bar chart, or merge into "Other" |
| Pie chart for two values | Write the percentage in text |
| Bar chart y-axis not at zero | Always start bar charts at zero |
| Line chart starting at zero unnecessarily | Show the range that matters |
| Sequential scale on categorical data | Switch to qualitative (hue-based) palette |
| Diverging scale without clear midpoint | Sequential scale, or define and label the midpoint |
| All text same size | Establish 2-level hierarchy: title vs. labels/notes |
| Precise values on color scale labels | Label only distinct classes; use "less/more" |
| Spaghetti line chart | Small multiples |
| Center-aligned labels | Left- or right-align |
| Choropleth showing absolute counts | Use rates/percentages per capita instead |
| Map with no orientation landmark | Add a river, coastline, or major landmark outside the focal area |
| Map annotations using arrows for areas | Use circles for regions, arrows only for specific points |
| Annotation colors that compete with map | Match annotation colors to the map's data palette |
| Map labels cluttering annotation callouts | Remove background labels if annotations already orient the reader |
| Two data series fighting for attention | Reduce opacity on secondary; increase stroke width on primary |
| Data color clashing with background region color | Split into separate columns or change one of the colors |
| Table as data dump | Give the table a message; sort by what matters |
| Condensed font to save space | Reduce font size instead |
| All caps for body text | Sentence case; all-caps only for short labels |
| No source cited | Always include the data source |
