# Alex · Health & Fitness Dashboard

Public single-page dashboard for **Alex McNab-Lundbäck** — body composition (Withings), fitness & paces (Strava), strength marks, meal plan, and upcoming training.

## Maintained by Sarah

**Sarah** (Health & Fitness assistant) owns this site. Update live numbers and plans in `data.json` — the UI in `index.html` reads that file and needs no redesign for routine data changes.

## Files

| File | Purpose |
|------|---------|
| `index.html` | Dark, mobile-first dashboard (vanilla HTML/CSS/JS) |
| `data.json` | All live stats, meals, and training |
| `README.md` | This note |

## Energy logs

Add end-of-day entries to `energy.dailyLogs` using this shape: `{ "date": "YYYY-MM-DD", "intakeKcal": number, "burnKcal": number, "deficitKcal": number, "mealsNote": "", "source": "garmin+self" }`. `deficitKcal` is `burnKcal - intakeKcal` (positive means a deficit); rolling averages are calculated in the dashboard from the latest seven logs.

## Local preview

Open `index.html` via a simple static server (fetch needs HTTP):

```bash
python3 -m http.server 8080
```

Then visit `http://localhost:8080`.

## GitHub Pages

Published from the `main` branch root. Public data only — not medical advice.
