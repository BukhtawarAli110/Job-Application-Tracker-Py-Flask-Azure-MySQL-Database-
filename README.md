# Job Tracker Web App (Flask + Azure MySQL + Render)

A simple web application built with Flask to track job applications.  
It supports full CRUD operations and sends automated email reminders for follow-ups.

---

## 🚀 Features

- Add, edit, delete job applications
- Search and filter applications by status
- Secure login system (session-based)
- Daily email reminders (Day 3, 5, 7 follow-ups)
- Manual trigger for reminder emails
- Azure MySQL database integration

---

## 🏗️ Tech Stack

- Python 3
- Flask
- MySQL (Azure MySQL Flexible Server)
- Gunicorn (production server)
- APScheduler (background jobs)
- Render (deployment)

---

## 📁 Project Structure
.
├── app.py # Main Flask app (routes, login, CRUD)
├── db.py # Database helper
├── reminders.py # Email reminders + scheduler
├── wsgi.py # Entry point for Gunicorn
├── requirements.txt
├── Procfile
├── render.yaml
├── .env.example
├── templates/
└── static/

---

## ⚙️ Environment Variables

Create a `.env` file based on `.env.example` and fill in:

### 🔐 App Config
FLASK_SECRET_KEY=your_secret_key
APP_PASSWORD=your_login_password


### 🗄️ Database (Azure MySQL)

DB_HOST=your_host
DB_PORT=3306
DB_USER=your_user
DB_PASSWORD=your_password
DB_NAME=your_database
DB_SSL_CA=path_to_cert.pem


### 📧 Email (SMTP)

EMAIL_FROM=your_email
EMAIL_TO=your_email
SMTP_HOST=smtp.gmail.com
SMTP_PORT=587
SMTP_USER=your_email
SMTP_PASSWORD=your_app_password


### ⏰ Reminder Scheduler

REMINDER_HOUR=9
REMINDER_MINUTE=0


---

## ▶️ Run Locally

```bash
python -m venv venv
venv\Scripts\activate        # Windows
pip install -r requirements.txt
python app.py

App runs at:

http://localhost:5000

