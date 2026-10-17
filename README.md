# EarthLens — Environmental Citizen Science

EarthLens is a Flask-based academic web application where community members can submit and explore observations about environmental concerns.

## Features
- Premium responsive landing page and community dashboard
- Community reports for pollution, waste, water, green spaces, and wildlife
- Search reports by title, location, or description
- Filter reports by category and status
- Account registration and sign-in with hashed passwords
- Report submission and report-owner status updates
- SQLite database created automatically on first run

## Project structure
```text
EarthLens/
├── app.py
├── database.py
├── requirements.txt
├── README.md
├── .gitignore
├── templates/
│   ├── base.html
│   ├── index.html
│   ├── reports.html
│   ├── new_report.html
│   ├── login.html
│   └── register.html
└── static/
    ├── css/style.css
    └── js/main.js
```

## Run locally
1. Install Python 3.10 or newer.
2. Open this folder in VS Code.
3. Open Terminal and run:
   ```bash
   pip install -r requirements.txt
   python app.py
   ```
4. Visit `http://127.0.0.1:5000`.

The SQLite database `earthlens.db` is generated automatically.

## Demo notes
The seeded community reports are sample observations for presentation, not verified scientific measurements. The sample community account is only used as the report owner for seeded entries; it is not a sign-in account.

## Before public deployment
Set a strong `SECRET_KEY` environment variable, turn off Flask debug mode, add CSRF protection and rate limiting, and review privacy/security requirements. Do not collect sensitive personal information. This is an academic demo, not an emergency reporting service.
