# ☕ Coffee & Wifi

Web app to discover cafes suitable for remote work, with ratings for coffee quality, wifi strength and power socket availability.

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Flask](https://img.shields.io/badge/Flask-2.3-black?logo=flask)
![Bootstrap](https://img.shields.io/badge/Bootstrap-5-purple?logo=bootstrap)

## Features

- Browse all registered cafes in a sortable table
- Add new cafes via a validated web form
- Emoji-based rating system for coffee ☕, wifi 💪 and power 🔌
- Data persisted in a CSV file

## Knowledge Applied

### Backend
- **Flask** — routing with `@app.route`, template rendering, form handling (`GET`/`POST`)
- **Flask-WTF + WTForms** — form creation, server-side validation, CSRF protection
- **python-dotenv** — loading environment variables from `.env` to keep secrets out of source code
- **CSV module** — reading and appending records to a flat-file database

### Frontend
- **Jinja2 templating** — template inheritance with `{% extends %}` and `{% block %}`, dynamic data rendering with loops and conditionals
- **Bootstrap 5 (Flask-Bootstrap)** — responsive layout, styled tables, `render_form` macro for automatic form rendering

### Project Practices
- **Environment variable management** — `SECRET_KEY` stored in `.env`, never committed to version control
- **`.gitignore`** — excluding `.env`, virtual environment, IDE files and Python cache
- **Separation of concerns** — logic in `main.py`, presentation in templates, styles in `static/css/`

## Project Structure

```
coffee-and-wifi/
├── main.py             # Flask app and routes
├── cafe-data.csv       # Cafe data (flat-file database)
├── requirements.txt    # Python dependencies
├── .env                # Secret keys (not committed)
├── .gitignore
├── static/
│   └── css/
│       └── styles.css
└── templates/
    ├── base.html
    ├── index.html
    ├── cafes.html
    └── add.html
```

## Getting Started

```bash
# Install dependencies
pip install -r requirements.txt

# Create your .env file
echo "SECRET_KEY=your_secret_key_here" > .env

# Run the app
python main.py
```

Then open `http://127.0.0.1:5000` in your browser.
