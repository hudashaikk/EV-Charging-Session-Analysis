# EV Charging Session Analysis Website

## Features
- Three separate demo logins and one shared dataset
- Flask login/logout with hashed passwords
- SQLite storage
- Pandas summary metrics
- Plotly charts
- CSV upload with required-column and numeric validation
- 150 illustrative sample charging sessions

## Setup (Windows / VS Code)
1. Install Python 3.10 or newer.
2. Open this folder in VS Code.
3. In the terminal, create a virtual environment:
   `python -m venv .venv`
4. Activate it:
   PowerShell: `.\.venv\Scripts\Activate.ps1`
   Command Prompt: `.venv\Scripts\activate.bat`
5. Install dependencies:
   `python -m pip install -r requirements.txt`
6. Start the app:
   `python app.py`
7. Open http://127.0.0.1:5000 in your browser.

If `python` is not recognized, use `py` in the commands instead.

## Demo accounts
- member1 / EVmember1!
- member2 / EVmember2!
- member3 / EVmember3!

These are demo credentials only. Change them and replace `SECRET_KEY` before deployment.

## CSV format
Required headers:
`session_id,session_date,vehicle_id,station_id,station_name,energy_kwh,duration_minutes,cost_inr,status`

Date example: `2026-03-12 14:30`
Energy is in kWh, duration is in minutes, and cost is in INR.

## Notes
- The sample records are synthetic and intended for demonstration, not real-world reporting.
- The first run creates `ev_charging.db` and inserts the sample dataset.
- Uploaded rows are appended to the same shared dataset. Duplicate session IDs are skipped.
- This is a student demo. Before public deployment, add CSRF protection, rate limiting, production secret management, and stronger upload controls; do not use the Flask development server in production.
