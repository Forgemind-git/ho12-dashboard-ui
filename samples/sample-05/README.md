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

## Use it with your Claude.ai subscription
No API key needed. Just your normal Claude.ai login.

1. Open **Claude.ai** (your subscription) in your browser.
2. Paste the **example prompt** below into the chat.
3. Claude replies with a complete `index.html`. Click **Copy**.
4. Open a plain text editor (Notepad on Windows, TextEdit on Mac), paste it in, and save
   the file as `index.html`.
5. **Double-click the file** — it opens in your browser and the dashboard appears.
6. To share it with stakeholders, push the file to a GitHub repo and turn on
   **Settings → Pages** for a free public link.

## The example prompt
Copy this exactly into Claude.ai:

```
Build me a single-file HTML dashboard (one index.html, no build tools) that shows project task status for stakeholders. Load Chart.js from a CDN.

Data: an array of projects, each item { project: string, done: number, in_progress: number, blocked: number, not_started: number }. Put this array in a clearly-commented const near the top of the script. Make up 6 realistic example projects with varied numbers.

Show four KPI stat cards calculated from the data:
- Total Tasks — sum of all tasks across every project.
- Done — total tasks in the done state.
- In Progress — total tasks in progress.
- Blocked — total blocked tasks.

Below the cards, show a horizontal stacked bar chart titled "Tasks by Status per Project" (one bar per project, segments coloured green/blue/red/grey for done/in_progress/blocked/not_started), and a summary table listing each project's totals with a simple Good/Warn/Bad health pill.

Use a clean modern look, white cards with soft shadows, and a light background. Make it mobile-friendly.
```

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
