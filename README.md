# Sprite Cutter

Drop a sprite sheet / UI kit → every piece is auto-detected, cropped, and downloaded as a ZIP (with `sprites.json` coordinates).

100% static — no build step, no backend. Everything runs in the browser.

## Files
- `index.html` — the whole app (HTML + CSS + JS)
- `jszip.min.js` — JSZip 3.10.1 (bundled locally, no CDN needed)
- `vercel.json` — caching headers

## Deploy on Vercel

**Option A — Dashboard (easiest)**
1. Push this folder to a GitHub repo.
2. vercel.com → Add New → Project → import the repo.
3. Framework Preset: **Other**. Leave Build Command and Output Directory empty.
4. Deploy.

**Option B — CLI**
```bash
npm i -g vercel
cd sprite-cutter
vercel        # preview
vercel --prod # live
```

## Run locally
```bash
npx serve .
```
(or just open `index.html` — but then change `/jszip.min.js` to `./jszip.min.js`)
