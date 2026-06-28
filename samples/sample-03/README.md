# HO12 Sample 3 — Content Performance Dashboard

## What you'll build
A one-page dashboard for creators that shows which of your posts are actually working —
average views, engagement rate, follower growth, best format and posting cadence as stat
cards, plus a bar chart of views for your recent posts. It's a single `index.html` file,
so there's nothing to install. This folder already contains a **working example with mock
data** — open `index.html` to see it filled in, then swap in your own numbers.

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
Build me a single-file HTML dashboard (one index.html file, no build tools) that shows my social content performance. Use Chart.js loaded from a CDN. It should show:

- Five stat cards at the top: Views Per Post (2,103 average), Engagement Rate (4.8%), Follower Growth (+312 this month), Best Format (Reels), Publishing Cadence (3 posts/week).
- A bar chart titled "Views Per Post" with these four posts: "Tips Reel" (1240), "Behind-the-scenes" (3580), "Q&A Live" (920), "Carousel" (2670).

Use a clean modern look with a purple accent colour (#9333EA), white cards with soft shadows, and a light grey background. Put all the numbers in clearly-commented variables near the top of the script so I can easily swap them for my own data. Make it mobile-friendly.
```

## Make it your own
- Replace the card numbers and the four post titles/views with your own from Instagram,
  TikTok or YouTube analytics.
- Add more posts to the chart, or switch it to a line chart of views over time.
- Ask Claude to colour the best-performing bar differently so it stands out.
