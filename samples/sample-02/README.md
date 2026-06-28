# HO12 Sample 2 — Team KPIs Dashboard

## What you'll build
A clean one-page dashboard that puts your team's key numbers — revenue, tickets, NPS,
churn, leads and pipeline — front and centre as stat cards, with a line chart showing the
revenue trend over the last three months. It's a single `index.html` file, so there's
nothing to install. This folder already contains a **working example with mock data** —
open `index.html` to see it filled in, then swap in your own figures.

## Use it with your Claude.ai subscription
No API key needed. Just your normal Claude.ai login.

1. Open **Claude.ai** (your subscription) in your browser.
2. Paste the **example prompt** below into the chat.
3. Claude replies with a complete `index.html`. Click **Copy**.
4. Open a plain text editor (Notepad on Windows, TextEdit on Mac), paste it in, and save
   the file as `index.html`.
5. **Double-click the file** — it opens in your browser and the dashboard appears.
6. To share it, drop the file into a new GitHub repo and turn on **Settings → Pages** for
   a free public link.

## The example prompt
Copy this exactly into Claude.ai:

```
Build me a single-file HTML dashboard (one index.html file, no build tools) that shows my team's KPIs to leadership. Use Chart.js loaded from a CDN. It should show:

- Six stat cards at the top: MRR ($48.2k), Tickets Resolved (312 this month), NPS Score (47), Churn Rate (2.3%), New Leads (128), Pipeline Value ($215k).
- A line chart titled "MRR — 3-month trend" with the months April, May, June and values 42000, 45500, 48200.

Use a clean modern look with a purple accent colour (#9333EA), white cards with soft shadows, and a light grey background. Put all the numbers in clearly-commented variables near the top of the script so I can easily swap them for my own data. Make it mobile-friendly.
```

## Make it your own
- Replace the six card numbers and the three monthly MRR values with your real figures.
- Pull the numbers from your spreadsheet: ask Claude how to load them from a Google Sheet
  or a published CSV link.
- Add a second chart (e.g. tickets resolved per week) by describing it to Claude.
