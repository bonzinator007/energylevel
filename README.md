# Energy Tracker
 
A simple Progressive Web App (PWA) to track daily energy levels based on the Lorenzen scale (0–10). Built for people managing Post-Stroke Fatigue who want to monitor their energy throughout the day.
 
---
 
## Features
 
- **Log energy levels** on a scale from 0 (completely empty) to 10 (full energy) at any time
- **Log past entries** – add readings for earlier times or dates you forgot to record
- **Day view** – see all your individual entries for any day as a chart, navigable by date
- **Week view** – daily averages over the last 7 days as a line chart
- **Month view** – daily averages over the last 30 days as a line chart
- **Works offline** – installable on your iPhone home screen as a native-feeling app
- **Privacy first** – all data stays on your device, nothing is sent to any server
---
 
## Installation on iPhone
 
1. Open Safari and go to your GitHub Pages URL:
   `https://YOUR-USERNAME.github.io/energy-tracker`
2. Tap the **Share** button (square with arrow pointing up)
3. Tap **"Add to Home Screen"**
4. Confirm the name and tap **"Add"**
The app will appear as an icon on your home screen and opens without browser controls, just like a native app.
 
---
 
## Data Storage
 
All data is stored locally in your iPhone's browser storage (`localStorage`). This means:
 
- Your data never leaves your device
- No account or login required
- Data persists across app updates – uploading a new `index.html` does not affect your entries
- Data is tied to the installed app URL – do not rename the repository
**Important:** If you remove the app from your home screen, the stored data will be deleted. A JSON export feature is planned to allow regular backups.
 
---
 
## The Lorenzen Scale
 
The energy scale used in this app is based on the energy profile model by Heiko Lorenzen, commonly used in Post-Stroke Fatigue management:
 
| Level | Meaning |
|---|---|
| 0 | Completely empty |
| 1–2 | Very low |
| 3–4 | Low |
| 5 | Moderate |
| 6–7 | Good |
| 8–9 | Very good |
| 10 | Full energy |
 
---
 
## Updating the App
 
To update the app with a new version:
 
1. Download the new `index.html` from Claude
2. Go to your GitHub repository
3. Click on `index.html` → click the **pencil icon** (Edit)
4. Select all → delete → paste the new content
5. Click **"Commit changes"**
Changes are live after 1–2 minutes. Your data is not affected.
 
---
 
## Planned Features
 
- JSON export for data backup and sharing with doctors or therapists
---
 
## Technical Details
 
- Single-file PWA: HTML + CSS + JavaScript
- No frameworks, no backend, no dependencies except Chart.js for charts
- Data format: `{ "ts": "2026-05-15T14:32:00.000Z", "v": 7 }`
- Storage key: `et_entries_v1` in localStorage
