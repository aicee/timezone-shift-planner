# Shift — Schedule Converter

A timezone-aware work schedule tracker built for Hostinger support teams.
Converts Lithuanian time (LT) to any target timezone (default: Manila PH +8).

## Features
- Week & Month calendar views
- Auto-splits Live Chat blocks when Break/Training/etc. is added inside
- Diagonal transition cells at :30 boundaries
- Categories: Live Chat, Break, Training, 1-on-1, Meeting, P2P Session, PPP
- Multi-day selection for batch adding shifts
- Midnight overflow handled across week boundaries
- Data persists in browser localStorage

## Deploy to Vercel (easiest)

1. Install Vercel CLI (requires Node.js):
   npm install -g vercel

2. From this folder, run:
   vercel

3. Follow the prompts — it will give you a live URL instantly.

## Deploy via Vercel Dashboard (no CLI)

1. Push this folder to a GitHub repo
2. Go to https://vercel.com → New Project
3. Import your GitHub repo
4. Click Deploy — done! (~30 seconds)

## Share with colleagues

Option A — Just share the HTML file:
  Send `index.html` directly. They open it in any browser.
  Each person gets their own localStorage (separate data).

Option B — Host on Vercel (shared URL, but still separate data per browser):
  Everyone uses the same URL, but localStorage is per-browser.

Option C — If you want SHARED data across colleagues:
  That would need a backend (not included). For now each person
  maintains their own schedule independently.

## Local use (no deployment needed)

Just open index.html in your browser. Works offline.
Data saves automatically to your browser's localStorage.

## Customize

- Change default timezone: edit the `<select id="tz-target">` default value
- Add more event types: search for "p2p" in the file and follow the pattern
