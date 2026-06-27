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
