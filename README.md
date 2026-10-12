# Diet Log & Nutrition Tracker

Personal meal, macro, and workout tracker. Dates and times use India Standard Time (IST).

## How logging works
- Add meals as rows in `data/food-log.csv`; one file holds all dates.
- Keep workouts in `data/workout-log.csv`.
- Use `data/food-database.csv` for reusable food nutrition estimates.
- `data/daily-summary.csv` is a convenience summary; the dashboard calculates totals directly from food-log rows.
- Nutrition values are estimates. Use package labels and measured portions when available.

## Dashboard / GitHub Pages
The dashboard lives in `index.html` and reads the CSV files in this repository. A GitHub Actions workflow in `.github/workflows/pages.yml` publishes the site.

After the first push, open **Settings → Pages** and ensure **Build and deployment → Source** is set to **GitHub Actions** if it is not already. Once the workflow finishes, the Pages URL will be shown under Settings → Pages.

## Current nutrition goals
Initial dashboard goals: 1,500 kcal, 100 g protein, 155 g carbs, 48 g fat, 25–30 g fibre. These are editable in the dashboard code. Treat goals as guides, not strict limits.

## CSV format
Food log columns: date, time_ist, meal, description, quantity, calories_kcal, protein_g, carbs_g, fat_g, fibre_g, sugar_g, notes.
Workout log columns: date, time_ist, workout, duration_min, details, notes.
