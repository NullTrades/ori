# dreaminwithori — 2026 plan PWA

Personal life tracker built as a Progressive Web App. Installable on iPhone from Safari.

## Stack
- Single `index.html` — no build step, no dependencies
- GitHub Pages hosting (free)
- Service worker for offline access

---

## GitHub Pages Setup (do this once)

1. Go to github.com → New repository
2. Name it: `dreaminwithori` (or anything you want)
3. Set to **Public**
4. Create the repo

Then in Cursor terminal:
```bash
git init
git remote add origin https://github.com/NullTrades/ori.git
git add .
git commit -m "init: dreaminwithori PWA"
git branch -M main
git push -u origin main
```

5. Go to repo Settings → Pages → Source: **Deploy from branch** → branch: `main` → folder: `/ (root)` → Save

Your app will be live at: `https://nulltrades.github.io/ori/`

---

## Install on iPhone

1. Open Safari on iPhone
2. Go to your GitHub Pages URL
3. Tap the Share button (box with arrow)
4. Tap "Add to Home Screen"
5. Tap Add — it's now a full-screen app on your home screen

---

## Update Workflow

**How to update the app after changes in Claude chat:**

1. Open Cursor
2. Make sure you're in this project folder
3. Claude Code will edit `index.html` directly
4. Then run:

```bash
git add .
git commit -m "update: [what changed]"
git push
```

GitHub Pages auto-deploys in ~30–60 seconds. Refresh on iPhone to see changes.

---

## What can be updated by telling Claude in chat

- Any debt number (Visa balance, Affirm payments)
- Progress percentages on any goal
- Checklist items (vlog steps, quarterly milestones)
- New goals, trips, career changes
- Igbo phase progress
- Anything in your Notion plan

Just say something like:
> "Visa is now $800, I paid $173"
> "I finished the comeback vlog, it's published"
> "Add Miami trip to Life tab"

Claude reads Notion, updates the code, you push, done.

---

## File Structure

```
dreaminwithori/
├── index.html      ← the entire app (edit this)
├── manifest.json   ← PWA config
├── sw.js           ← service worker (offline)
├── icon-192.png    ← app icon (add your own)
├── icon-512.png    ← app icon (add your own)
└── README.md
```

## Adding App Icons

Create a square image (your face, logo, etc.) and export at:
- 192×192px → `icon-192.png`
- 512×512px → `icon-512.png`

Drop both in the project folder and push.
