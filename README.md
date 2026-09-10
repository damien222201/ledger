# Ledger — Spending & Debt Tracker

A single self-contained HTML page for logging daily spending and
tracking debt — no backend, no build step, no database. Everything is
stored in the browser's `localStorage`, so it works entirely client-side
and is perfect for hosting free on GitHub Pages.

## Features

- **Log an expense** — amount + reason, timestamped to a date
- **Daily Ledger** — browse any day, see every entry and the day's total
- **Monthly Summary** — total spent this month, entry count, average per
  entry, and a day-by-day bar breakdown
- **Debt Book** — a separate slot for tracking money you owe and money
  owed to you, each with a reason, running outstanding totals, and a
  "mark settled" toggle (settled entries stay visible but struck through)
- **Always-visible status strip** — today's total, this month's total,
  and your net debt position, at the top of every tab
- **Export to CSV** — download everything (expenses + debts) as one file
- **Clear all data** — a reset button, with a confirmation prompt

## Design

Styled as an actual bookkeeper's ledger rather than a generic finance
dashboard: ruled paper background, a folder-tab strip to switch between
Daily / Monthly / Debt Book, and monospace type for every number and
date so entries read like typewritten ledger rows. Fraunces (serif) is
used for headings; IBM Plex Mono for everything else.

## How to host on GitHub Pages

1. Push this repo to GitHub.
2. Go to **Settings → Pages**.
3. Under "Build and deployment", set **Source** to `Deploy from a
   branch`, branch `main`, folder `/ (root)`.
4. Your tracker will be live at
   `https://<your-username>.github.io/<repo-name>/`

## A note on data

All entries are stored in **your browser's localStorage only** — nothing
is sent to a server, and nothing syncs across devices or browsers.
Clearing your browser data (or using a different browser/device) starts
you with an empty ledger. Use the **Export CSV** button regularly if you
want a backup.

## Project structure

```
spending-tracker/
└── index.html   # everything — markup, styles, and logic in one file
```

## Skills demonstrated

Vanilla JavaScript • localStorage persistence • Responsive CSS •
Data visualization (bar breakdown) • CSV export • No-backend architecture
