# 📊 Executive Sales Dashboard (Vibe-coded)

An interactive, single-page sales analytics dashboard built for executive stakeholders (CEO/CFO level), powered by a retail Superstore dataset.

> ✨ **Vibe coded.** This project was built end-to-end through conversational prompting with Claude — from exploring the raw dataset to designing the visuals to debugging the deployment. No hand-written boilerplate; the entire dashboard was generated, reviewed, and iterated on through AI-assisted development. The two prompts used to produce it are included in this repo (see [`/prompts`](./prompts)) so the process is fully transparent and reproducible.

🔗 **Live demo:** [sartaj1995.github.io/sales-dashboard-t1](https://sartaj1995.github.io/sales-dashboard-t1/)

---

## Overview

This dashboard turns a raw retail transactions file into a decision-ready view of the business — built specifically for a non-technical executive audience who needs the story, not the spreadsheet.

It's a single, self-contained HTML file: no backend, no build step, no server. Open it in a browser, or host it for free on GitHub Pages.

## Key Insights Surfaced

The dashboard is built around a handful of insights pulled directly from the data, not assumed in advance:

- 📉 A significant share of order line items are loss-making (negative profit)
- 🪑 **Furniture** — specifically **Tables** and **Bookcases** — are the primary drivers of losses
- 🗺️ The **South** and **Central** regions consistently show the weakest margins
- 🏷️ Heavy discounting correlates strongly with profit losses
- 📅 2021 saw a slight sales contraction compared to 2020

## Features

- Executive-friendly KPI summary (sales, profit, margin, order volume)
- Interactive charts (region, category, discount vs. profit, year-over-year trend)
- Clean, presentation-ready visual design suitable for a boardroom
- Fully self-contained — no dependencies beyond CDN-hosted charting libraries
- Works offline once loaded; no data leaves the browser

## Data Source

`superstore_data.xlsx` — a retail Superstore transactions dataset covering:
- ~9,994 order line items
- 2018–2021
- Sales, profit, discount, geography, customer segment, and product category fields

## Tech Stack

- HTML / CSS / JavaScript (single self-contained file)
- CDN-hosted charting library (no local install required)
- Hosted via GitHub Pages

## Repo Structure

```
├── index.html              # The full dashboard (self-contained)
├── prompts/
│   ├── 1_meta_prompt.md    # The prompt used to construct the final build prompt
│   └── 2_final_prompt.md   # The final prompt used to generate the dashboard
└── README.md
```

## Running Locally

No installation needed:

```bash
git clone https://github.com/sartaj1995/sales-dashboard-t1.git
cd sales-dashboard-t1
open index.html   # or just double-click the file
```

## Roadmap

- [ ] Add a geographic choropleth map for regional performance
- [ ] Incorporate stakeholder feedback rounds after initial share-out

## Why This Repo Exists

Beyond the dashboard itself, this repo is a small case study in **AI-assisted product building** — going from a raw dataset to a polished, boardroom-ready tool through structured prompting, iteration, and debugging, all documented in the included prompt files.

---

*Built with Claude.*