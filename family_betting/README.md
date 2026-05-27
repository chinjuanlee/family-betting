# 🎲 FamilyBets

A Polymarket-style prediction market app built for family use. Place bets on family events, track odds in real-time, and settle up when the truth comes out.

## Live Markets

| # | Market | Category |
|---|--------|----------|
| 1 | Who gets married first — Chin or Sofia? | Family |
| 2 | Will Nicholas be incarcerated? | Drama |

## Features

- **Real-time sync** — all bets shared instantly across devices via Firebase Realtime Database
- **Parimutuel payouts** — winners split the losers' pool proportionally to their stake
- **Odds tracker** — probability updates live as each bet comes in
- **Charts tab** — odds over time, volume by market, family P&L, bet distribution, bet count per person
- **Admin panel** (PIN-gated) — create new markets, resolve outcomes, reset all data
- **Leaderboard** — ranked by balance with P&L per person

## Getting Started

Open `index.html` in any browser — no install or build step needed. All data lives in Firebase so everyone shares the same state.

Each family member starts with **$1,000** in play money.

## Tech Stack

- Vanilla HTML/CSS/JS — single file, no framework
- [Firebase Realtime Database](https://firebase.google.com/products/realtime-database) — real-time shared state
- [Chart.js](https://www.chartjs.org/) — charts and analytics

## Admin

Go to the **Admin** tab and enter the PIN (`1234` by default) to:
- Create new prediction markets (Yes/No or custom two-option)
- Resolve a market and distribute payouts
- Reset all data back to $1,000 per person

To change the PIN, update `ADMIN_PIN` in `index.html`.

## Hosting

The app is a static HTML file — host it anywhere:

**GitHub Pages:** Repo → Settings → Pages → Deploy from `main` / `/family_betting`

**Local network:** Run `python3 -m http.server 8080` in this folder and open `http://<your-ip>:8080` on any device on the same WiFi.
