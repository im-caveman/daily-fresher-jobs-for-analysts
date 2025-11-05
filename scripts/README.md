# Job Automation Scripts

This folder contains the automation that fetches LIVE analyst jobs using RapidAPI (Active Jobs DB), validates the exact application URLs, extracts Job_ID and Source, and creates a dated pull request daily at 10:00 AM IST.

Setup
1) Add your RapidAPI key as a repository secret named RAPIDAPI_KEY
2) The workflow file at .github/workflows/daily-jobs.yml runs daily
3) Outputs are written to data/YYYY-MM-DD/

Rules enforced
- Only exact application pages (no listing/search pages)
- Job_ID + Source required for every URL
- URL validated (HTTP + job keyword heuristics) before adding
- India + Remote roles prioritized; experience filtered to 0–2 and 2–5 years
