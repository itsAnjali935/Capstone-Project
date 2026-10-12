
# SmartCity.AI – Bhopal Civic Issue Management System

SmartCity.AI is a software-based civic issue management platform designed to help citizens report local problems and help administrators manage, prioritize, and track complaints in Bhopal.

## Features

- **Citizen Portal:** Register, log in, submit civic complaints, and track complaint status.
- **Complaint Classification:** Uses machine learning to predict the category of a complaint.
- **Priority Assessment:** Applies rule-based logic to identify complaints that require urgent attention.
- **Admin Dashboard:** Allows administrators to review and manage complaints.
- **Department Management:** Supports organizing civic issues for the relevant departments.
- **Complaint Tracking:** Helps users follow the progress of submitted complaints.
- **Duplicate Detection:** Checks for potentially duplicate complaints.
- **REST API:** Provides backend endpoints for frontend communication.

## Technology Stack

- **Frontend:** React, Vite, Tailwind CSS
- **Backend:** Python, FastAPI
- **Database:** SQLAlchemy with the configured database
- **Machine Learning:** TF-IDF and Naive Bayes for complaint classification
- **Priority Engine:** Rule-based priority assessment
- **Containerization:** Docker and Docker Compose

## Project Structure

```text
Capstone-Project/
├── backend/
│   ├── app/
│   ├── tests/
│   ├── Dockerfile
│   └── requirements.txt
├── database/
│   ├── schema.sql
│   └── seed.py
├── frontend/
│   ├── src/
│   ├── package.json
│   └── Dockerfile
├── ml/
│   ├── data/
│   ├── models/
│   └── train_models.py
├── .gitignore
├── docker-compose.yml
└── README.md
```

## Getting Started

### Prerequisites

Install the following tools:

- Python 3.10 or a compatible version supported by the project dependencies
- Node.js and npm
- Git

Docker Desktop is optional if you prefer running the services manually.

### 1. Clone the repository

```bash
git clone https://github.com/itsAnjali935/Capstone-Project.git
cd Capstone-Project
```

### 2. Start the backend

Open a terminal in the project root:

```bash
cd backend
python -m venv venv
```

Activate the virtual environment on Windows:

```powershell
.\venv\Scripts\Activate.ps1
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Configure the required environment variables and database settings according to the backend configuration.

Start the API:

```bash
uvicorn app.main:app --reload
```

When the server starts, open `http://127.0.0.1:8000/docs` to explore the API, if Swagger documentation is enabled.

### 3. Start the frontend

Open a second terminal at the project root:

```bash
cd frontend
npm install
npm run dev
```

Open the local URL printed by Vite in the terminal.

### 4. Run with Docker (optional)

From the project root, run:

```bash
docker compose up --build
```

Follow the service URLs and configuration defined in `docker-compose.yml`.

## Machine Learning

The project uses a TF-IDF and Naive Bayes pipeline to classify civic complaints into categories. Complaint priority is determined separately by a rule-based priority engine.

The classifier can be trained using the project's training script:

```bash
python ml/train_models.py
```

Run this command from the project root with the required Python dependencies installed.

## Security Notes

- Do not commit `.env` files, API keys, database passwords, or other secrets.
- Configure administrator accounts and credentials locally.
- Do not use demo credentials in production.
- Keep environment-specific configuration out of public source control.

## Project Purpose

This capstone project demonstrates how web development, machine learning, and rule-based decision logic can be combined to support civic complaint reporting and management.

---

**Project:** SmartCity.AI – Bhopal Civic Issue Management System  
**Type:** Academic Capstone Project
























































