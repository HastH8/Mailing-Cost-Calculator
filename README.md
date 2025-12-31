# Mailing Cost Calculator (Flask)

Flask web app for calculating mailing costs by weight, converting currency, and saving user history. Includes user authentication, profile management, and an admin dashboard.

## Features
- Weight-based mailing cost calculator with detailed breakdown
- Currency conversion (base TRY) via exchangerate-api.com
- User registration/login with history tracking
- Export calculation history to CSV
- Profile edit + password update
- Admin dashboard with user management and stats

## Tech Stack
- Python, Flask
- Flask-Login, Flask-SQLAlchemy, Flask-Migrate
- SQLite
- Requests, Pillow

## Setup
1. Create a virtual environment:
   ```bash
   python -m venv .venv
   source .venv/bin/activate
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Run
```bash
python app.py
```
Open `http://localhost:8080` in your browser.

The app creates `app.db` automatically on first run.

## Admin Access
1. Register a user in the UI.
2. Grant admin privileges:
   ```bash
   flask --app app grant-admin <username>
   ```

## Project Structure
- `app.py` - Flask app, models, routes, and CLI commands
- `templates/` - HTML templates
- `static/` - CSS, JS, images, uploads

## Notes
- Currency conversion relies on a public API and requires network access.
- Profile pictures are stored under `static/profile_pics/`.
