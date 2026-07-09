# Diwan of Prizes — ديوان الجوائز
## Install guide / دليل التثبيت

This folder is a complete Progressive Web App (PWA). Once it is on the
internet (any free host), it can be **installed like a normal app** on
Android, iPhone, and desktop — with its own icon, full-screen view, and
offline use.

---

## Files in this package

| File | Purpose |
|---|---|
| `index.html` | The entire app (all 28 prizes + Add Prize feature) |
| `manifest.webmanifest` | Tells phones/desktops this is an installable app (name, icon, colors) |
| `sw.js` | Service worker — makes the app work offline and load instantly |
| `icons/` | App icons (home screen, splash, favicon) |
| `README.md` | This guide |

Do not rename `index.html`, `sw.js`, or `manifest.webmanifest` — the
files reference each other by these names.

---

## Step 1 — Put it online (one time, ~2 minutes, free, no coding)

Pick ONE of these:

**Option A — Netlify (easiest):**
1. Go to https://app.netlify.com/drop
2. Drag this whole folder onto the page.
3. Done. You get a link like `https://your-name.netlify.app`.

**Option B — GitHub Pages:**
1. Create a repository on github.com, upload these files.
2. Settings → Pages → deploy from the main branch.
3. Your app appears at `https://yourusername.github.io/repo-name/`.

**Option C — Cloudflare Pages, Vercel, or any web hosting** — upload the
folder as-is; no build settings needed.

> Why hosting is required: browsers only allow app installation and
> offline mode for pages served over HTTPS. That is a browser security
> rule, not a limitation of this app. (Opening `index.html` directly by
> double-click still works fine as a regular page — it just can't be
> "installed" that way.)

---

## Step 2 — Install it on each device

**Android (Chrome):** open your link → menu (⋮) → **"Install app"** or
"Add to Home screen" → the Diwan icon appears like any app.

**iPhone / iPad (Safari only):** open your link → Share button (□↑) →
**"Add to Home Screen"** → opens full-screen with the app icon.

**Windows / Mac (Chrome or Edge):** open your link → install icon (⊕ or
a small screen symbol) at the end of the address bar → **Install**.

---

## Your data

- Prizes you add are stored on each device (they do not sync between
  devices automatically).
- Use **⬇ Export my prizes** inside the app to back them up as a small
  file, and **⬆ Import** to load them on another device.
- Built-in prize data was verified against official sources in
  July 2026 — always confirm deadlines on the official award site
  before submitting.

## Updating the app later

Edit `index.html` (the prize data is in the `BUILT_IN` list near the top
of the script), change `CACHE_VERSION` in `sw.js` (e.g. `diwan-v2`), and
re-upload. Installed copies pick up the update on next launch.

