# HO12 Sample 1 — Habit Tracker Dashboard

## What you'll build
A single-page dashboard that shows your weekly progress across a few habits — streak,
workouts, steps, sleep and spending — as big stat cards plus a bar chart. Everything lives
in one `index.html` file that opens straight in a browser, so there's nothing to install.
This folder already contains a **working example with mock data** — open `index.html` and
you'll see the cards and chart filled in. Use it as-is, then swap in your own numbers.

## Use it with your Claude.ai subscription
No API key needed. Just your normal Claude.ai login.

1. Open **Claude.ai** (your subscription) in your browser.
2. Paste the **example prompt** below into the chat.
3. Claude replies with a complete `index.html`. Click **Copy**.
4. Open a plain text editor (Notepad on Windows, TextEdit on Mac), paste it in, and save
   the file as `index.html`.
5. **Double-click the file** — it opens in your browser and the dashboard appears.
6. To put it online for free, drop the file into a new GitHub repo and turn on
   **Settings → Pages**. You'll get a public link to share.

## The example prompt
Copy this exactly into Claude.ai:

```
Build me a single-file HTML dashboard (one index.html file, no build tools) that tracks my personal habits. Use Chart.js loaded from a CDN. It should show:

- Five stat cards at the top: Habit Streak (12 days), Workouts This Week (4), Steps Average (8,450/day), Sleep Average (7.2 hours), Spending vs Budget (82%).
- A bar chart titled "Weekly Progress" showing habits completed for Week 1–4 with these values: 18, 22, 19, 25.

Use a clean modern look with a purple accent colour (#9333EA), white cards with soft shadows, and a light grey background. Put all the numbers in clearly-commented variables near the top of the script so I can easily swap them for my own data. Make it mobile-friendly.
```

## Make it your own
- Replace the five card numbers and the four weekly values with your real habit data.
- Ask Claude to add a second chart (e.g. a line chart of sleep hours over the month).
- Change the accent colour, or add or remove a card — just tell Claude what you want.
