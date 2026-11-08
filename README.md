# PROJECT 2028 — UNSTOPPABLE (Offline PWA)

## What's included
- Manual backlog creation: any subject, chapter, lecture count, duration, priority, notes and target date.
- Editable backlog items and one-tap lecture completion / undo.
- Automatic remaining lecture, remaining-hour, daily-target and deadline-health calculations.
- Daily mission suggestions recalculated from your data.
- 360° subject and overall progress dashboards.
- Existing `project2028_v1` browser data key retained; the new backlog system is added alongside earlier records.
- Local JSON export/import.
- Offline PWA app shell and Android install support.
- Animated black-and-gold interface with a battery-friendly particle toggle and reduced-motion option.

## Run locally
Open `index.html` in a modern browser for basic use. Browser install/offline caching requires HTTPS or localhost.

## Publish free with GitHub Pages
1. Create a GitHub repository named `project-2028-unstoppable`.
2. Upload **all files and folders** in this package to the repository root (not inside another nested folder).
3. Open repository **Settings → Pages**.
4. Under Build and deployment choose **Deploy from a branch**.
5. Choose branch `main`, folder `/ (root)`, then Save.
6. Wait for GitHub Pages to publish the site. Open the Pages URL once while online.

## Install on Android tablet
1. Open the published HTTPS URL in Chrome.
2. Open the browser menu (⋮) and choose **Install app** or **Add to Home screen**.
3. Confirm installation. Launch it from the tablet home screen.
4. Open it once while online so the service worker can cache the app shell. Then test offline by switching off Wi-Fi.
5. Keep the JSON backup from Settings somewhere safe. Browser storage is local to the device and can be cleared by Android/browser storage cleanup.

## Important data note
This version stores backlog data in the browser's local storage on this device. It does not provide cloud sync or multi-device syncing. Export backups regularly, especially before clearing browser data or reinstalling the browser.

## Daily target calculation
For each unfinished backlog item:
- Remaining lectures = total lectures − completed lectures.
- Available days = max(1, calendar days from today through the target date, inclusive).
- Daily target = ceiling(remaining lectures ÷ available days).
- Remaining hours = remaining lectures × average lecture duration ÷ 60.

The app proposes a daily mission from the closest deadlines first. It does not force a schedule; you can edit backlog and deadlines at any time.
