# Putting Daniel DJ on GitHub Pages (free)

This folder is the whole website. Once it's hosted over HTTPS your phone can "install" it like an app:
it gets a home-screen icon, opens full screen, keeps the screen awake while music plays, and opens even when offline.
(The double-click file `daniel-dj.html` keeps working on its own; it just can't install.)

## One-time setup (about 5 minutes)
1. Sign in at https://github.com (or make a free account).
2. Click **New repository**, name it e.g. `daniel-dj`, choose **Public**, then click **Create repository**.
3. On the new repo page click **uploading an existing file** and drag in everything in this folder:
   `index.html`, `manifest.webmanifest`, `sw.js`, `icon-192.png`, `icon-512.png`, `icon-maskable-512.png`.
   (You don't need to upload HOSTING.md.) Click **Commit changes**.
4. Open **Settings → Pages**. Under "Build and deployment" pick **Deploy from a branch**, branch **main**, folder **/ (root)**, then click **Save**.
5. Wait a minute. Your site will be live at `https://<your-username>.github.io/daniel-dj/`.

## Install it on your phone
- **iPhone (Safari):** open the link, tap **Share → Add to Home Screen**.
- **Android (Chrome):** open the link, tap **⋮ → Install app** (or "Add to Home screen").

## Updating later
1. Regenerate `index.html`: in `/workspace/dj-app` run `./build_site.sh` (it copies `daniel-dj.html` to `site/index.html`).
2. In `sw.js`, change `daniel-dj-v6` to a new name (e.g. `daniel-dj-v7`) so phones fetch the new version.
3. Upload the changed files to the repo again (**Add file → Upload files**). Pages updates within a minute or two.

## Notes
- Your music never leaves your device. The site only serves the app; songs are opened from your phone or computer.
- Public repos are visible to anyone with the link, but they only contain the app code.
- On iPhone, the first tap anywhere unlocks audio (an iOS rule), and the app asks iOS to keep playing even with the silent switch on (iOS 17+ where supported).
