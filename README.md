# OTA Driver Training Planner — Prototype v0.1

A responsive, static, offline-capable planning estimator for a **single exact vehicle model**, intended for GitHub Pages.

## Deploy on GitHub Pages
1. Create a repository (for example `ota-driver-training-planner`).
2. Upload **the files inside this folder** to the repository root (`index.html` must be at root).
3. Open **Settings → Pages → Build and deployment**.
4. Choose **Deploy from a branch**, select **main** and **/(root)**, then Save.
5. Visit the Pages URL displayed by GitHub after deployment.

## What is implemented
- Aggregate inputs for beginner/intermediate/advanced students, matching vehicles, qualified NCOs, LI/LEs, control lanes, and expected failure rate.
- Editable duration assumptions, optional specialized equipment and simulator time.
- A rough phase duration estimator and **illustrative** overlap between Phase II and Phase III.
- Calendar rows with Army-style administrative columns.
- Offline U.S. federal holiday calculation, including observed dates, plus manually entered non-training days.
- CSV export compatible with Excel. **This is not a native `.xlsx` export.**
- Responsive interface and service-worker offline caching after initial online visit.

## Limitations — important
This is an **initial planning prototype, not a validated duty-compliant optimizer**. It does not allocate individual students, vehicles, or examiners hour by hour, or enforce rolling 24-hour driver-duty caps, 8-hour rest, darkness/sunrise/sunset windows, 1200–1300 lunch, PT, or 90-day permit expiry. The Gantt overlap is illustrative; simultaneous activities can exceed shared vehicle capacity and require review. It uses coarse capacity estimates and may overestimate or underestimate actual calendar duration. Phase III starts on projected readiness, not actual team-leader referrals. No personal data should be entered. Verify Army requirements with current authoritative publications before operational use.

## Privacy and saving
No backend, account, or browser-plan persistence. Inputs are held in memory until the page is refreshed. Use CSV export to save the proposed calendar. There is no CSV import in v0.1.

## Files
- `index.html`: app interface
- `styles.css`: responsive styling
- `app.js`: calculations, holidays, Gantt, calendar and export
- `manifest.webmanifest` / `sw.js`: installability and offline caching
