# The Tab

A simple shared-expense tracker for hangouts with friends. Standalone PWA — no backend, no login, data lives on the device.

## Files
- `index.html` — the app
- `manifest.json` — PWA manifest (name, icons, colors)
- `service-worker.js` — makes it work offline once loaded
- `icons/` — app icons generated from your artwork, in the sizes PWABuilder and Android expect

## Put it on GitHub Pages
1. Create a new GitHub repo (e.g. `the-tab`).
2. Upload all the files in this folder, keeping the folder structure (`icons/` stays a subfolder).
3. In the repo, go to **Settings > Pages**, set source to the `main` branch, root folder, and save.
4. GitHub gives you a URL like `https://yourusername.github.io/the-tab/`. Open it once to confirm the app loads.

## Turn it into an installable Android app with PWABuilder
1. Go to [pwabuilder.com](https://www.pwabuilder.com).
2. Paste in your GitHub Pages URL and hit **Start**.
3. PWABuilder will scan the manifest and icons (already set up here) and score your PWA — it should pass with the icons included.
4. Click **Package for stores > Android**, download the package.
5. That gives you a signed `.apk` or `.aab` you can install directly on an Android phone (enable "install unknown apps" for your browser/file manager) or upload to the Play Store.

## Note on data
Each phone that installs this keeps its own local copy of the ledger (via browser storage) — it does not sync between friends automatically. Everyone would need to enter their own view of shared expenses, or one person keeps the "source of truth" copy.
