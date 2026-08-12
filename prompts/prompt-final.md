# Dashboard Build Prompt — Superstore Executive Performance Dashboard

## Role
You are a senior BI developer and data storyteller. Build an executive-level, interactive sales & profitability dashboard for the **CEO and CFO** of a retail superstore business.

## Source Data
File: `superstore_data.xlsx` — one flat table, 9,994 rows (2018-01-03 to 2021-12-30).

| Column | Type | Notes |
|---|---|---|
| Row ID, Order ID | ID | Order ID repeats — one order can have multiple line items |
| Order Date, Ship Date | Date | Use Order Date for all time trends |
| Ship Mode | Category | Standard/Second/First Class, Same Day |
| Customer ID, Customer Name | ID/Text | 793 unique customers |
| Segment | Category | Consumer, Corporate, Home Office |
| Country/Region, City, State, Postal Code, Region | Geography | 49 states, 531 cities, 4 US regions (South/West/Central/East) |
| Product ID, Category, Sub-Category | Category | 3 Categories, 17 Sub-Categories |
| Sales | Measure | Revenue for that line item |
| Quantity | Measure | Units sold |
| Discount | Measure | 0–1 (e.g. 0.2 = 20%) |
| Profit | Measure | Can be negative — ~1,870 line items are loss-making |

## Audience & Purpose
CEO and CFO — they need to answer three questions in under 60 seconds: **Are we growing? Are we profitable? Where's the risk/opportunity?** Assume no time to hunt through raw data. No jargon, no clutter — every visual must justify its place on the page.

## Design Principles
- **Simplicity first**: one dashboard page (with tabs/pages if needed for drill-down), clean grid layout, consistent color palette (2–3 brand colors + one alert color reserved only for losses/negative trends).
- **Executive hierarchy**: KPI summary cards at the very top, trends next, breakdowns and detail below.
- **Self-explanatory**: every chart has a clear title stating the takeaway, not just the metric name (e.g. "Profit Margin Is Shrinking in Furniture" beats "Profit Margin by Category").
- **Consistent formatting**: currency in $, one decimal for %, thousands separators, consistent date granularity.
- **Insight callouts**: add 3–5 short text annotations/cards surfacing what the data says (best/worst region, loss-making sub-category, top customer concentration, discount-profit relationship), not just charts with no narrative.

## Required KPI Cards (top row)
1. Total Sales
2. Total Profit
3. Profit Margin %
4. Total Orders
5. Average Order Value
6. YoY Sales Growth %

## Required Visuals (minimum 10 — build all of these)
1. **Sales & Profit Trend Over Time** — dual-axis or combo line/bar chart, monthly, 2018–2021, to show growth trajectory and where profit diverges from sales.
2. **Sales by Category & Sub-Category** — treemap or bar chart, drillable from Category into Sub-Category.
3. **Profit by Category & Sub-Category** — bar chart, sorted ascending, so loss-making sub-categories (e.g. Tables, Bookcases, Supplies typically) are immediately visible.
4. **Sales by Region** — map (if tool supports geo) or bar chart across South/West/Central/East.
5. **Profit Margin % by Region** — bar chart, highlighting the region with the weakest margin, not just weakest sales.
6. **Sales by Customer Segment** — donut/pie chart (Consumer/Corporate/Home Office).
7. **Discount vs. Profit Relationship** — scatter plot (Discount % on X, Profit on Y), to visually prove/disprove that high discounts destroy margin.
8. **Top 10 Customers by Sales** — horizontal bar chart, with a callout on revenue concentration risk (e.g. "Top 10 customers = X% of sales").
9. **Sales by Ship Mode** — bar or donut chart, to inform logistics cost conversations.
10. **Loss-Making Orders Analysis** — table or bar chart isolating line items with negative profit, broken down by Category/Sub-Category, with a KPI card showing count and $ of losses.
11. **Sales by State/City (Top 10)** — bar chart or map, for geographic expansion/investment decisions.
12. **Monthly Order Volume vs. Average Discount** — combo chart to show whether heavier discounting periods correlate with volume spikes (seasonality).

*(That's 12 — gives you two to trim if the tool/space demands exactly 10.)*

## Interactivity Requirements
- **Global filters/slicers** (affecting every visual): Date range, Region, Category, Segment, Ship Mode.
- **Cross-filtering**: clicking any chart element (e.g. a region on the map) filters all other visuals.
- **Drill-down**: Category → Sub-Category → Product on relevant charts.
- **Tooltips**: every visual shows Sales, Profit, Margin %, and Quantity on hover — not just the single plotted metric.
- **Toggle**: a Sales/Profit metric switch on the trend and regional charts so the CEO/CFO can flip perspective without needing two separate charts.

## Insights the Dashboard Must Make Obvious (without reading raw numbers)
- Overall business is profitable (~10% margin) but profitability is inconsistent across categories/sub-categories — some products are sold at a loss.
- Whether high discounting is correlated with the loss-making transactions.
- Which region drives the most sales vs. which region is most/least efficient (margin).
- Revenue concentration — how dependent the business is on top customers.
- Growth trend — is the business accelerating, flat, or decelerating year over year.

## Deliverable Format
- Specify the output as a single-page interactive dashboard (state your tool: Power BI / Tableau / Excel / HTML dashboard).
- Use a consistent 12-column grid layout: KPI row → trend row → category/region row → detail/table row.
- Include a short "Executive Summary" text box (3–4 bullet points) pinned at the top or side, auto-summarizing the top-line story.
