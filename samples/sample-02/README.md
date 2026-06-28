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

## Use it with your Claude.ai subscription
No API key needed. Just your normal Claude.ai login.

1. Open **Claude.ai** (your subscription) in your browser.
2. Paste the **example prompt** below into the chat.
3. Claude replies with a complete `index.html`. Click **Copy**.
4. Open a plain text editor (Notepad on Windows, TextEdit on Mac), paste it in, and save
   the file as `index.html`.
5. **Double-click the file** — it opens in your browser and the dashboard appears.
6. To share it, push the file to a GitHub repo and turn on **Settings → Pages** for a free
   public link.

## The example prompt
Copy this exactly into Claude.ai:

```
Build me a single-file HTML dashboard (one index.html, no build tools) for a support team's KPIs. Load Chart.js from a CDN.

Data: an array of 8 weeks, each item { week: "YYYY-Www", closed: number, opened: number, csat: number, resolution_hours: number, escalations: number }. Put this array in a clearly-commented const near the top of the script. Make up realistic example data (closed around 40–70/week, CSAT around 4.0–4.7).

Show four KPI stat cards calculated from the data:
- Tickets Closed This Week — closed count for the most recent week.
- Avg Resolution Time — mean resolution_hours across all weeks, in hours.
- Customer Satisfaction Score — mean csat as a decimal (1–5 scale).
- Open Escalations — escalations from the latest week.

Below the cards, show a grouped bar chart titled "Weekly Ticket Volume" with closed vs opened per week.

Use a clean modern look with a purple accent (#9333EA), white cards with soft shadows, and a light background. Make it mobile-friendly.
```

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
