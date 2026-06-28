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

## Use it with your Claude.ai subscription
No API key needed. Just your normal Claude.ai login.

1. Open **Claude.ai** (your subscription) in your browser.
2. Paste the **example prompt** below into the chat.
3. Claude replies with a complete `index.html`. Click **Copy**.
4. Open a plain text editor (Notepad on Windows, TextEdit on Mac), paste it in, and save
   the file as `index.html`.
5. **Double-click the file** — it opens in your browser and the dashboard appears.
6. To put it online for free, push the file to a GitHub repo and turn on
   **Settings → Pages**. You'll get a public link to share.

## The example prompt
Copy this exactly into Claude.ai:

```
Build me a single-file HTML dashboard (one index.html, no build tools) that visualises my daily habit tracking. Load Chart.js from a CDN.

Data: an array of 30 days, each item { date: "YYYY-MM-DD", completed_habits: number, total_habits: number }. Put this array in a clearly-commented const near the top of the script so I can swap it for my own data. Make up realistic example data where I usually complete 4–5 of 5 habits.

Show four KPI stat cards calculated from the data:
- Current Streak — consecutive days (up to the latest) with at least one habit completed.
- Days Completed This Month — days this calendar month where all habits were completed.
- Completion Rate % — total completed ÷ total possible over the 30 days.
- Best Streak — longest run of fully-completed days.

Below the cards, show a line chart titled "Daily Habits — Last 30 Days" plotting completed_habits vs total_habits per day.

Use a clean modern look with a purple accent (#9333EA), white cards with soft shadows, and a light background. Make it mobile-friendly.
```

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
