# Breast Cancer Detection Web App

This project is a Flask-based machine learning web application for breast cancer classification. It lets users:

- enter 30 tumor feature values manually
- paste a CSV row of 30 values
- use a basic image workflow (currently scaffolded for future CNN integration)

The app loads trained models from the `saved_models/` folder and predicts whether the input is malignant or benign.

## Project structure

- `app.py` – Flask app and prediction logic
- `templates/` – HTML pages
- `static/` – CSS and JavaScript files
- `saved_models/` – trained model files and scaler
- `src/` – supporting preprocessing/evaluation scripts
- `notebooks/` – training notebooks

## Requirements

Python 3.10+

```bash
pip install -r requirements.txt
```

## Run locally

```bash
python app.py
```

Then open:

```text
http://localhost:5000
```

## Deployment notes

This app is ready to be deployed behind a WSGI server or any host that supports Python web apps. For example, the included `wsgi.py` entrypoint works with Gunicorn:

```bash
gunicorn wsgi:app
```

## GitHub push

To publish this repository on GitHub, run:

```bash
git init
git add .
git commit -m "Initial project commit"
git branch -M main
git remote add origin https://github.com/rayen-feb/machine_learning_breast_cancer_detection.git
git push -u origin main
```
