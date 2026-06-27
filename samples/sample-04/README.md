# Sample 04 — City Open Data Explorer

A self-contained HTML dashboard that turns city incident or public-service data into clear visual summaries. Built to show how open civic datasets — 311 calls, permit applications, road closures — can be displayed without a backend.

## What the dashboard shows

| Card | Description |
|------|-------------|
| Total Incidents This Month | Count of all records in the current calendar month |
| Most Common Type | The incident category that appears most frequently |
| Avg Response Time | Mean response time in minutes across all records |
| Open vs Resolved | Count of unresolved incidents vs. total |

The doughnut chart breaks incidents down **by category** so patterns are immediately visible.

## How to use

1. Open `index.html` in any modern browser — no build step, no server needed.
2. Replace the `INCIDENT_DATA` const at the top of the script block with your own data or API.
3. Host on GitHub Pages by enabling Pages in your repo Settings.

## How to swap mock data for real data

```js
// SWAP THIS: replace with your real API call or data source
const INCIDENT_DATA = [ ... ];
```

Replace with a fetch:

```js
const res = await fetch('https://data.cityofexample.gov/resource/incidents.json?$limit=500');
const INCIDENT_DATA = await res.json();
// Expected shape: array of { date: "YYYY-MM-DD", type: string, response_time_min: number, resolved: boolean }
```

Many city open-data portals use Socrata, which returns JSON at URLs like the one above.

## Deploy to GitHub Pages

Push this folder to a repo and enable Pages in Settings → Pages → Branch: main / Folder: /samples/sample-04
