# Sample 01 — Personal Habit Tracker Dashboard

A self-contained HTML dashboard that visualises daily habit completion data. Displays a 30-day line chart and four KPI stat cards to help you understand your consistency at a glance.

## What the dashboard shows

| Card | Description |
|------|-------------|
| Current Streak | Consecutive days with at least one habit completed up to today |
| Days Completed This Month | Days in the current month where all habits were completed |
| Completion Rate % | Percentage of total possible habit completions achieved over the last 30 days |
| Best Streak | Longest consecutive run of fully-completed days in the dataset |

The line chart plots **daily completed habits** against **total habits** over the last 30 days.

## How to use

1. Open `index.html` directly in any modern browser — no build step, no server needed.
2. The mock data is a `const` near the top of the `<script>` block, clearly marked with a comment.
3. To host on GitHub Pages: push this folder to a GitHub repo, go to Settings → Pages, set the source branch/folder to where index.html lives.

## How to swap mock data for real data

Find this block near the top of the script section:

```js
// SWAP THIS: replace with your real API call or data source
const HABIT_DATA = [ ... ];
```

Replace it with a fetch call:

```js
const res = await fetch('https://your-api.example.com/habits?days=30');
const HABIT_DATA = await res.json();
// Expected shape: array of { date: "YYYY-MM-DD", completed_habits: number, total_habits: number }
```

## Deploy to GitHub Pages

Push this folder to a repo, enable Pages in Settings → Pages → Branch: main / Folder: /samples/sample-01
