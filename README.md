# KRYVA

A simple market application built with Flask, allowing users to register, login, and trade items.

## Project Structure

```text
FlaskMarket/
├── flaskenv/             # Virtual environment
├── instance/            # Instance folder (contains SQLite database)
├── market/               # Main application package
│   ├── static/           # Static assets (CSS, JS, Images)
│   │   └── css/          # CSS files (e.g., kryva.css)
│   ├── templates/        # HTML templates (Jinja2)
│   │   ├── includes/     # Partial templates and modals
│   │   ├── base.html     # Base layout
│   │   ├── home.html     # Homepage
│   │   ├── login.html    # Login page
│   │   ├── market.html   # Market dashboard
│   │   └── register.html # Registration page
│   ├── __init__.py       # App initialization and configuration
│   ├── forms.py          # WTForms for user input
│   ├── models.py         # SQLAlchemy database models
│   └── routes.py         # URL routing and view functions
└── run.py                # Entry point to run the application
```

## Core Components

- **`run.py`**: The main entry point. It imports the `app` instance from the `market` package and runs the development server.
- **`market/__init__.py`**: Initializes the Flask application, configures the database (SQLAlchemy), password hashing (Bcrypt), and login management (LoginManager).
- **`market/models.py`**: Defines the database schema, including `User` and `Item` models.
- **`market/routes.py`**: Handles all the URL routing and business logic for each page (home, login, register, market).
- **`market/forms.py`**: Contains the form classes for user registration, login, and other interactions, using Flask-WTF.

## Getting Started

1. **Install Dependencies**:
   Ensure you have the necessary packages installed (Flask, Flask-SQLAlchemy, Flask-Bcrypt, Flask-Login, Flask-WTF).
   ```bash
   pip install flask flask-sqlalchemy flask-bcrypt flask-login flask-wtf email-validator
   ```

2. **Run the Application**:
   Execute the `run.py` script.
   ```bash
   python run.py
   ```
   The app will be available at `http://127.0.0.1:5000/`.

## Author
Kritan Lamichhane
