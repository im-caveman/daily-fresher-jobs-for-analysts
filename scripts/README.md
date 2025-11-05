# Automation Script for Daily Job Updates

This repository includes an automation script that validates job application URLs, extracts Job_ID and Source fields, and prepares daily CSVs and pull requests.

## Files
- `scripts/job_automation_script.py`

## Highlights
- Validates each URL via HTTP status and lightweight content checks
- Detects ATS sources (Greenhouse, Workday, Lever, Amazon ATS, Microsoft ATS, Google ATS, Deloitte ATS, Razorpay/Greenhouse)
- Distinguishes job listing pages from application pages
- Adds `Job_ID`, `Source`, `Is_Application_Page`, `URL_Valid`, `Validation_Message` columns
- Prepares files for GitHub PRs dated by the run date
