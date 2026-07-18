# End-to-end-Youtube-Sentiment

# 🧠✨ End-to-End Live YouTube Viewer Sentiment MLOps Pipeline

An end-to-end, production-grade MLOps system designed to eliminate tutorial guesswork. Using a custom Chrome Extension, this tool fetches live YouTube comments via the YouTube Data API, routes them through a containerized Flask backend powered by an optimized LightGBM model, and injects a real-time analytics dashboard (pie charts, trend graphs, and word clouds) directly onto the YouTube watch page.

---

## 🚀 Features & Workflow
1. **Chrome Extension UI:** Injects an interactive data visualization dashboard natively into the YouTube watch page interface.
2. **Real-Time Data Ingestion:** Fetches live comment streams dynamically using the YouTube Data API v3.
3. **Robust Text Engineering:** Balances highly skewed comment datasets using SMOTE and extracts semantic features via TF-IDF Vectorization.
4. **Centralized MLOps Tracking:** Integrated with an AWS-hosted MLflow server and Amazon S3 for comprehensive tracking of artifacts, hyperparameters, and evaluation metrics.
5. **Modular DVC Automation:** Managed as a reproducible 5-stage Data Version Control pipeline spanning ingestion to model registration.
6. **Automated GitOps CI/CD:** Utilizes GitHub Actions to build Docker containers, push them to AWS ECR, and automatically deploy updates to an AWS EC2 instance.

---

## 🛠️ Tech Stack
* **Frontend:** Chrome Extension API, JavaScript, Data Visualization Libraries
* **Backend:** Python 3.11, Flask
* **Machine Learning & MLOps:** LightGBM, Scikit-Learn, SMOTE, NLTK, MLflow, DVC
* **Cloud & DevOps:** Docker, AWS EC2, AWS ECR, Amazon S3, GitHub Actions

---

## ⚙️ Project Architecture & Pipeline Stages

The core engine is driven by a highly modular, 5-stage DVC pipeline managed via `dvc.yaml` and `params.yaml`:

1. **Data Ingestion:** Interacts with the YouTube API to pull raw comment feeds.
2. **Data Preprocessing:** Cleans, tokenizes, and processes natural language text using NLTK.
3. **Feature Engineering:** Converts text to numeric representations via TF-IDF and applies SMOTE to balance sentiment classes.
4. **Model Training:** Optimizes hyperparameters and trains a high-performance LightGBM Classifier.
5. **Evaluation & Registration:** Evaluates metrics, exports local performance plots, and registers production-ready models to MLflow.

---
~ Made By Rhythm 
