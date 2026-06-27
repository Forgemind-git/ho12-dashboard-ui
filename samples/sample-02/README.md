# Sample 02 — Team KPI Dashboard

A self-contained HTML dashboard for tracking support or engineering team performance. Shows ticket volume, resolution speed, customer satisfaction, and escalations across an 8-week window.

## What the dashboard shows

| Card | Description |
|------|-------------|
| Tickets Closed This Week | Count of tickets resolved in the most recent week in the dataset |
| Avg Resolution Time | Mean hours to close a ticket across all weeks |
| Customer Satisfaction Score | Average CSAT (1–5 scale) displayed as a decimal |
| Open Escalations | Synthetic count derived from the latest week's data |

The bar chart plots **weekly ticket volume** (closed vs opened) for the last 8 weeks so you can quickly spot backlogs.

## How to use

1. Open `index.html` directly in any modern browser — no build step, no server needed.
2. Find the `TEAM_KPI_DATA` const at the top of the script block and replace it with your own data.
3. Deploy to GitHub Pages by enabling Pages in your repo Settings → Pages.

## How to swap mock data for real data

```js
// SWAP THIS: replace with your real API call or data source
const TEAM_KPI_DATA = [ ... ];
```

Replace with a fetch:

```js
const res = await fetch('https://your-api.example.com/kpis?weeks=8');
const TEAM_KPI_DATA = await res.json();
// Expected shape: array of { week: "YYYY-Www", closed: number, opened: number, csat: number }
```

## Deploy to GitHub Pages

Push this folder to a repo and enable Pages in Settings → Pages → Branch: main / Folder: /samples/sample-02
