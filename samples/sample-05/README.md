# Sample 05 — Project Status Dashboard

A self-contained HTML dashboard for engineering leads and project managers. Shows task status distribution across multiple projects with a horizontal stacked bar chart, making it easy to compare throughput at a glance.

## What the dashboard shows

| Card | Description |
|------|-------------|
| Total Tasks | Sum of all tasks across every project |
| Done | Tasks in the "done" state |
| In Progress | Tasks currently being worked on |
| Blocked | Tasks blocked and needing attention |

The horizontal stacked bar chart shows **tasks per status per project** so you can instantly see which projects are healthy and which are stalled.

## How to use

1. Open `index.html` in any modern browser — no build step, no server needed.
2. Replace the `PROJECT_DATA` const at the top of the script block with your own data or API response.
3. Host on GitHub Pages by enabling Pages in your repo Settings.

## How to swap mock data for real data

```js
// SWAP THIS: replace with your real API call or data source
const PROJECT_DATA = [ ... ];
```

Replace with a fetch:

```js
const res = await fetch('https://your-api.example.com/projects/status-summary');
const PROJECT_DATA = await res.json();
// Expected shape: array of { project: string, done: number, in_progress: number, blocked: number, not_started: number }
```

## Deploy to GitHub Pages

Push this folder to a repo and enable Pages in Settings → Pages → Branch: main / Folder: /samples/sample-05
