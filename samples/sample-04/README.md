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
Build me a single-file HTML dashboard (one index.html, no build tools) that turns a city open dataset (311-style incidents) into clear visuals. Load Chart.js from a CDN.

Data: an array of incident records, each item { date: "YYYY-MM-DD", type: string, response_time_min: number, resolved: boolean }. Put this array in a clearly-commented const near the top of the script. Make up ~35 realistic example records across types like "Road Damage", "Noise Complaint", "Illegal Parking", "Graffiti", "Water Leak".

Show four KPI stat cards calculated from the data:
- Total Incidents This Month — count of records in the current calendar month.
- Most Common Type — the type that appears most often.
- Avg Response Time — mean response_time_min across all records.
- Open vs Resolved — count of unresolved vs total.

Below the cards, show a doughnut chart titled "Incidents by Category" breaking records down by type.

Use a clean modern look with a purple accent (#9333EA), white cards with soft shadows, and a light background. Make it mobile-friendly.
```

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
