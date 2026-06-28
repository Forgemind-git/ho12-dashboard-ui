# HO12 Sample 5 — Project Status Dashboard

## What you'll build
A one-page status dashboard that answers "where do things stand?" at a glance — stat cards
for projects On Track / At Risk / Blocked and tasks completed, a donut chart of the status
split, and a list of upcoming deadlines with colour-coded pills. It's a single `index.html`
file, so there's nothing to install. This folder already contains a **working example with
mock data** — open `index.html` to see it filled in, then swap in your own projects.

## Use it with your Claude.ai subscription
No API key needed. Just your normal Claude.ai login.

1. Open **Claude.ai** (your subscription) in your browser.
2. Paste the **example prompt** below into the chat.
3. Claude replies with a complete `index.html`. Click **Copy**.
4. Open a plain text editor (Notepad on Windows, TextEdit on Mac), paste it in, and save
   the file as `index.html`.
5. **Double-click the file** — it opens in your browser and the dashboard appears.
6. To share it with stakeholders, drop the file into a new GitHub repo and turn on
   **Settings → Pages** for a free public link.

## The example prompt
Copy this exactly into Claude.ai:

```
Build me a single-file HTML dashboard (one index.html file, no build tools) that shows my projects' status for stakeholders. Use Chart.js loaded from a CDN. It should show:

- Four stat cards at the top: On Track (7 projects), At Risk (3 projects), Blocked (2 projects), Tasks Completed (34 this week).
- A donut chart titled "Status Split" with On Track 7, At Risk 3, Blocked 2 (green, amber, red).
- A list titled "Upcoming Deadlines" with these rows, each showing a name, a date and a colour-coded status pill: "Website redesign" (Jul 3, On Track), "Mobile app launch" (Jul 9, At Risk), "Data migration" (Jul 12, Blocked), "Q3 marketing campaign" (Jul 18, On Track).

Use a clean modern look with a purple accent colour (#9333EA), white cards with soft shadows, and a light grey background. Put the project data in a clearly-commented array near the top of the script and build the deadline list from it, so I can easily swap in my own projects. Make it mobile-friendly.
```

## Make it your own
- Replace the counts and the deadline rows with your real projects and dates.
- Connect it to your task tool by asking Claude how to load the data from its CSV export.
- Add a "blocked reason" column or a second chart (e.g. tasks completed per week).
