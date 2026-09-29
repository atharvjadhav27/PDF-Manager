# Django PDF Manager System - Dockerized Application

## Project Overview

The Django PDF Manager System is a web-based application developed using Django and SQLite. It allows users to upload, view, download, and manage PDF documents through a user-friendly interface.

This project has been containerized using Docker to ensure consistent deployment and execution across different environments.

---

## Technologies Used

- Python 3.11
- Django
- SQLite
- HTML
- CSS
- Docker

---

## Project Structure

DJANGO-PDF-MANAGER/

├── pdf_app/

├── PDF_Manager/

├── manage.py

├── db.sqlite3

├── requirements.txt

├── Dockerfile

└── .dockerignore

---

## Dockerfile

```dockerfile
FROM python:3.11

WORKDIR /app

COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

COPY . .

EXPOSE 8000

CMD ["python","manage.py","runserver","0.0.0.0:8000"]
