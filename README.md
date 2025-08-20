# Habit & Workout Tracker — PWA Bundle

This folder is ready to host as a **Progressive Web App** (installable, offline).

## Files
- `index.html` — the app (includes dynamic manifest + iOS icon + SW registration)
- `sw.js` — service worker for offline caching
- `README.md` — you are here

> Icons are generated at runtime, so no extra image files are needed.

## Deploy
1. Upload these files to any **HTTPS** static host (GitHub Pages, Netlify, Vercel, etc.).  
2. Visit the URL once while online to warm the cache.

### Install on phone
- **Android / Chrome**: open the site → ⋮ menu → **Install app**.
- **iOS / Safari**: Share → **Add to Home Screen**.

## Update the app
- After changing code, bump the cache name in `sw.js` (e.g., `hwt-cache-v2`) and redeploy.
- Users may need to refresh once to pick up updates.

## Data & backups
- Data is stored in `localStorage` per device/browser.
- Use **Export** in the UI to back up JSON; **Import** to restore or merge.

## Notes
- Service workers don't run from `file://`. Use a local server (e.g., `npx serve .`) or host online.
