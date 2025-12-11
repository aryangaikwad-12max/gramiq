# GramIQ — Farm Finance Report Generator

Simple FastAPI backend that accepts farm finance data via a web form and generates a downloadable PDF report with charts, tables, and a clean header (GramIQ logo).

## Repository structure
gramiq-report/
├─ app.py
├─ templates/report.html
├─ requirements.txt
├─ README.md
└─ sample_data/example_submission.json


## Setup (local / Ubuntu)
1. Clone the repo:
```bash
git clone <your-repo-url>
cd gramiq-report

## Create virtual environment and install Python deps
python3 -m venv .venv
source .venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt

## Install system dependency for PDF
sudo apt update
sudo apt install -y wkhtmltopdf

Running in Google Colab
##Install dependencies in a Colab cell
##Upload app.py, templates/report.html, and gramiq_logo.png to workspace; start uvicorn and ngrok as documented in the repo.

Libraries used

FastAPI — API framework
Uvicorn — ASGI server
Jinja2 — HTML templating
Matplotlib — charts generation
pdfkit + wkhtmltopdf — HTML → PDF conversion
python-multipart — form parsing
pydantic — validation
pyngrok — (optional) expose local server in Colab

Files of interest
app.py — backend logic, models, charting, PDF generation
templates/report.html — Jinja2 report template
requirements.txt — Python dependencies
sample_data/example_submission.json — sample payload for testing
