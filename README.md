# North Idaho Trail Log — PWA

A self-contained iPhone ride journal. No backend, no accounts, no internet required after setup.

## Files

| File | What it is |
|---|---|
| `index.html` | The entire app |
| `manifest.json` | PWA install config |
| `sw.js` | Service worker (offline support) |
| `icon-192.png` | Home screen icon (you supply) |
| `icon-512.png` | Home screen icon large (you supply) |

---

## How to get it on your iPhone

The app needs to be served over HTTPS to install as a PWA on iOS.
The easiest free option is **GitHub Pages** — takes about 5 minutes.

### Option 1 — GitHub Pages (recommended, free)

1. Create a free account at github.com
2. Create a new repository (e.g. `trail-log`), set it to **Public**
3. Upload all files from this folder to the repository
4. Go to Settings → Pages → Source: Deploy from branch → main → / (root)
5. GitHub gives you a URL like `https://yourusername.github.io/trail-log`
6. Open that URL in Safari on your iPhone
7. Tap the Share button → **Add to Home Screen**
8. Done — it's on your home screen like a native app

### Option 2 — Netlify Drop (even faster)

1. Go to app.netlify.com/drop in your browser
2. Drag the entire folder onto the page
3. Netlify gives you an instant HTTPS URL
4. Open it in Safari on your iPhone → Share → Add to Home Screen

---

## App icons (optional but nice)

The app works without icons but will show a generic placeholder on your home screen.
To add a proper icon:
- Create a square image (green mountain / bike theme fits well)
- Export as `icon-192.png` (192×192px) and `icon-512.png` (512×512px)
- Add them to the folder before uploading

Free tool: squoosh.app for resizing, or just use any image editor.

---

## Using the app

- **Tap a trail card** to expand details
- **Circle button** on the left marks a trail visited (stamps the date)
- **Stars** set your personal rating — tap again to clear
- **Notes area** — tap the dashed box to write, Cmd+Enter or Save button to save
- **+ button** adds a new trail
- **⇅ button** (top right) opens Export / Import

## Export / Import

- **Export** generates a `trail-log-YYYY-MM-DD.json` file and triggers the iOS share sheet
  — save to Files, email to yourself, or AirDrop to your PC as a backup
- **Import** loads a previously exported JSON file — useful for restoring a backup
  or moving to a new phone

## Data storage

All data is saved in Safari's localStorage tied to the site URL.
It persists indefinitely as long as you don't clear Safari's website data.
Regular exports are your backup strategy.
