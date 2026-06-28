# Sample 03 — Content Performance Dashboard

A self-contained HTML dashboard for content creators and marketing teams. Tracks views, engagement, follower growth, and top-performing content over the last 30 days using a dual-axis line chart.

## What the dashboard shows

| Card | Description |
|------|-------------|
| Total Views This Month | Sum of all daily views in the current calendar month |
| Avg Engagement Rate | Mean engagement rate (%) across all 30 days |
| Top Performing Piece | The date with the highest single-day view count |
| New Followers | Sum of daily follower gains across the 30-day window |

The dual-axis chart overlays **daily views** (left axis, bars) and **engagement rate %** (right axis, line) to surface the relationship between reach and audience response.

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
Build me a single-file HTML dashboard (one index.html, no build tools) for content performance. Load Chart.js from a CDN.

Data: an array of 30 days, each item { date: "YYYY-MM-DD", views: number, engagement_rate: number, shares: number, new_followers: number }. Put this array in a clearly-commented const near the top of the script. Make up realistic example data (views around 900–3000/day, engagement 3–7%).

Show four KPI stat cards calculated from the data:
- Total Views This Month — sum of views for the current calendar month.
- Avg Engagement Rate — mean engagement_rate over the 30 days, as a %.
- Top Performing Day — the date with the highest single-day views.
- New Followers — sum of new_followers across the period.

Below the cards, show a dual-axis chart titled "Daily Views & Engagement Rate — Last 30 Days" with views as bars (left axis) and engagement_rate as a line (right axis).

Use a clean modern look with a purple accent (#9333EA), white cards with soft shadows, and a light background. Make it mobile-friendly.
```

## How to use

1. Open `index.html` in any modern browser — no build step required.
2. The `CONTENT_DATA` const at the top of the script holds mock data. Swap it for your API.
3. Host on GitHub Pages: push to a repo and enable Pages in Settings.

## How to swap mock data for real data

```js
// SWAP THIS: replace with your real API call or data source
const CONTENT_DATA = [ ... ];
```

Replace with:

```js
const res = await fetch('https://your-api.example.com/content?days=30');
const CONTENT_DATA = await res.json();
// Expected shape: array of { date: "YYYY-MM-DD", views: number, engagement_rate: number, shares: number, new_followers: number }
```

## Deploy to GitHub Pages

Push this folder to a repo and enable Pages in Settings → Pages → Branch: main / Folder: /samples/sample-03
