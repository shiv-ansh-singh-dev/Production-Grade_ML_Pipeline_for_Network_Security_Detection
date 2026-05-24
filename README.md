# Production-Grade_ML_Pipeline_for_Network_Security_Detection

Production-grade end-to-end MLOps pipeline for phishing and network anomaly detection using MongoDB, Scikit-learn, Docker, AWS, and GitHub Actions.

---

## Overview

This project implements a modular machine learning pipeline for detecting phishing and malicious network activity. The system automates:

- Data ingestion from MongoDB Atlas
- Data validation and drift detection
- Feature transformation and preprocessing
- Model training and evaluation
- Dockerized deployment
- CI/CD automation using GitHub Actions
- AWS EC2 + ECR cloud deployment

The architecture is built using an artifact-driven modular pipeline design suitable for scalable MLOps workflows.

---

## Tech Stack

- Python
- Scikit-learn
- MongoDB Atlas
- Evidently AI
- Pandas & NumPy
- Docker
- AWS EC2
- AWS ECR
- GitHub Actions

---

## Pipeline Architecture

```text
MongoDB Atlas
      │
      ▼
Data Ingestion
      │
      ▼
Data Validation
      │
      ▼
Data Transformation
      │
      ▼
Model Training
      │
      ▼
Model Evaluation
      │
      ▼
Model Deployment
      │
      ▼
AWS EC2 Deployment
```

---

## Project Structure

```bash
networksecurity/
│
├── components/
├── pipeline/
├── configuration/
├── entity/
├── utils/
├── app.py
├── train_pipeline.py
├── Dockerfile
├── requirements.txt
└── README.md
```

---

## Features

- Modular ML pipeline architecture
- Automated data validation & drift detection
- KNN Imputer + RobustScaler preprocessing
- SMOTETomek imbalance handling
- Automated model selection
- Dockerized deployment
- CI/CD pipeline using GitHub Actions
- AWS cloud deployment

---

## Local Setup

### Clone Repository

```bash
git clone https://github.com/your-username/networksecurity.git
cd networksecurity
```

### Create Environment

```bash
python -m venv venv
source venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Configure Environment Variables

Create `.env` file:

```env
MONGO_DB_URL=your_mongodb_connection_string
```

---

## Run Pipeline

### Training Pipeline

```bash
python train_pipeline.py
```

### Run Application

```bash
python app.py
```

---

## Docker Setup

### Build Docker Image

```bash
docker build -t networksecurity .
```

### Run Container

```bash
docker run -p 5000:5000 networksecurity
```

---

## AWS Deployment

### GitHub Secrets

```env
AWS_ACCESS_KEY_ID=

AWS_SECRET_ACCESS_KEY=

AWS_REGION=us-east-1

AWS_ECR_LOGIN_URI=788614365622.dkr.ecr.us-east-1.amazonaws.com

ECR_REPOSITORY_NAME=networkssecurity
```

---

## EC2 Docker Setup

```bash
sudo apt-get update -y

curl -fsSL https://get.docker.com -o get-docker.sh

sudo sh get-docker.sh

sudo usermod -aG docker ubuntu

newgrp docker
```

---

## CI/CD Workflow

1. Push code to GitHub
2. GitHub Actions builds Docker image
3. Image pushed to AWS ECR
4. EC2 pulls latest image
5. Container redeployed automatically

---

## Author

Shivansh Singh

- GitHub: https://github.com/shiv-ansh-singh-dev
- LinkedIn: https://linkedin.com/in/shivansh-singh112
