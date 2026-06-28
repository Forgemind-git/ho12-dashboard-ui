# HO12 Sample 4 — Open Data Explorer Dashboard

## What you'll build
A one-page dashboard that turns a public dataset into something readable — headline stat
cards, two charts (a bar chart and a line chart) and a small data table. The example uses a
city bike-share dataset (rides and trip lengths per month), but you can point it at any
open data you're curious about. It's a single `index.html` file, so there's nothing to
install. This folder already contains a **working example with mock data** — open
`index.html` to see it filled in, then swap in your own dataset.

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
Build me a single-file HTML dashboard (one index.html file, no build tools) that visualises a city bike-share open dataset. Use Chart.js loaded from a CDN. It should show:

- Four stat cards at the top: Total Rides (198k Jan–Apr), Avg Trip Length (15 minutes), Busiest Month (April), Active Stations (240).
- A bar chart titled "Rides Per Month (thousands)" for Jan, Feb, Mar, Apr with values 42, 38, 51, 67.
- A line chart titled "Average Trip Length (minutes)" for the same four months with values 14, 13, 16, 18.
- A data table with columns Month, Rides (000s), Avg Trip (min), Active Stations, with one row per month (active stations: 228, 230, 236, 240).

Use a clean modern look with a purple accent colour (#9333EA), white cards with soft shadows, and a light grey background. Put all the data in a clearly-commented array near the top of the script and build the table rows from it, so I can easily swap in my own dataset. Make it mobile-friendly.
```

## Make it your own
- Find a dataset that interests you (your city's open-data portal, sports stats, app
  reviews) and replace the months and numbers with its columns.
- Tell Claude the column names from your CSV and ask it to match the cards and table.
- Add a third chart or a filter dropdown by describing what you want to Claude.
