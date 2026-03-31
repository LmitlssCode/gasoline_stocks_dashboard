# Gasoline Fundamentals — EIA WPSR Dashboard

A real-time interactive dashboard for tracking U.S. gasoline market fundamentals using data from the **U.S. Energy Information Administration (EIA) Weekly Petroleum Status Report (WPSR)**.

## Overview

This single-page web application provides a comprehensive view of the U.S. gasoline market, covering RBOB, CBOB, and total gasoline across all PADD regions. It fetches live weekly data directly from the EIA API v2 and presents it through interactive charts and summary tables.

## Features

### Data Categories

- **Ending Stocks** — RBOB, CBOB, and Total Gasoline inventory levels (Thousand Barrels)
- **Trade** — RBOB/CBOB imports, total motor gasoline imports/exports, crude oil imports/exports, and net import flows (Thousand Bbl/Day)
- **Production** — Reformulated, conventional, and finished motor gasoline production (Thousand Bbl/Day)
- **Refinery/Blender Inputs** — RBOB and CBOB blender inputs, crude oil inputs, and refinery utilization rates (Thousand Bbl/Day / %)
- **Product Supplied (Demand)** — Finished motor gasoline demand and fuel ethanol inputs (Thousand Bbl/Day)

### Regional Coverage (PADD Regions)

- U.S. Total
- PADD 1 — East Coast
- PADD 2 — Midwest
- PADD 3 — Gulf Coast (USGC)
- PADD 4 — Rockies
- PADD 5 — West Coast

### Dashboard Components

- **Key Metrics** — At-a-glance cards showing latest U.S. RBOB stocks, CBOB stocks, and motor gasoline demand with week-over-week changes
- **USGC Sentiment Indicator** — Automated bullish/bearish/neutral assessment for PADD 3 based on stocks, production, imports, and demand trends
- **Interactive Charts** — Time-series charts with current year, prior year, and 5-year seasonal average overlays
- **Summary Tables** — Weekly data with week-over-week and year-over-year changes
- **Date Range Controls** — Filter by 1Y, 3Y, 5Y, 10Y, all data, or custom date ranges
- **Debug Panel** — Built-in diagnostics for API call status and data validation

## Data Source

All data is sourced from the [EIA API v2](https://www.eia.gov/opendata/):

- `petroleum/sum/sndw` — Ending stocks
- `petroleum/move/wkly` — Trade and import/export flows
- `petroleum/pnp/wprodrb` — Refinery and blender production
- `petroleum/pnp/wiup` — Refinery inputs and utilization
- `petroleum/cons/wpsup` — Product supplied (demand)

## Usage

Open `gasoline_dashboard_Finalv1.html` in a web browser. The dashboard will automatically fetch the latest data from the EIA API and render all charts and tables. No build step or server is required.

### Requirements

- A modern web browser (Chrome, Firefox, Edge, Safari)
- Internet connection (for live EIA API data)

## Tech Stack

- **HTML/CSS/JavaScript** — Single-file, no build tooling
- **Chart.js 4.4.1** — Charting library (loaded via CDN)
- **Google Fonts** — JetBrains Mono and Outfit typefaces

## File Structure

| File | Description |
|------|-------------|
| `gasoline_dashboard_Finalv1.html` | Latest stable version of the dashboard |
| `gasoline_dashboard_0.html` – `gasoline_dashboard_7.html` | Earlier development iterations |
| `gasoline_dashboard.html` | Initial version |

## License

This project uses publicly available data from the U.S. Energy Information Administration.
