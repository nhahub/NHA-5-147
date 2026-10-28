# AI Interview Coach 🎯

An AI-powered interview preparation platform that helps candidates prepare for job interviews, practice answering questions, and receive structured feedback to improve their interview performance.

## 📌 Overview

**AI Interview Coach** is a web application designed to make interview preparation more personalized, structured, and accessible. Users can upload their CVs, build candidate profiles, practice role-specific interview questions, and review evaluations that highlight their strengths and areas for improvement.

The project combines a React-based frontend with a FastAPI backend, database persistence, and an intelligent evaluation pipeline to support the interview preparation workflow.

## ✨ Key Features

- **CV Upload and Analysis:** Upload a CV to support personalized interview preparation.
- **Candidate Profiles:** Organize relevant skills, experience, and professional information.
- **Personalized Interviews:** Practice interview questions based on the candidate's profile and target role.
- **Answer Evaluation:** Receive structured feedback and performance scores.
- **Evidence-Based Feedback:** Review the concepts and evidence associated with answer evaluations.
- **Improvement Plans:** Identify skill gaps and get guidance on what to improve.
- **Interview History:** Review previous sessions and track performance over time.
- **Question Bank:** Use a structured collection of interview questions and competency data.
- **Authentication:** Access user-specific application features.
- **Responsive Interface:** Navigate the platform through a modern React interface.

## 🛠️ Technology Stack

| Component | Technologies |
|---|---|
| Frontend | React, Vite, JavaScript, CSS |
| Backend | Python, FastAPI |
| Database | PostgreSQL |
| Database Migrations | Alembic |
| Data Validation | Pydantic |
| Testing | Pytest |
| API Documentation | OpenAPI / Swagger UI |
| Containerization | Docker |

## 🏗️ System Architecture

The application follows a frontend–backend architecture.

1. **Frontend:** Provides the user interface for CV uploads, profile management, interview sessions, and evaluation results.
2. **Backend API:** Handles requests, authentication, interview workflows, and application logic.
3. **Intelligence and Evaluation Layer:** Supports question selection, answer scoring, competency analysis, and personalized improvement recommendations.
4. **Database:** Stores application data, interview sessions, answers, evaluations, and related records.
5. **Testing Layer:** Validates API endpoints, application logic, database behavior, and evaluation workflows.

## 📂 Repository Structure

```text
NHA-5-147/
├── AI_Interview_Coach/
│   ├── backend/
│   │   ├── app/
│   │   │   ├── api/              # API routes and dependencies
│   │   │   ├── core/             # Configuration and security
│   │   │   ├── db/               # Database setup
│   │   │   ├── intelligence/     # Interview intelligence logic
│   │   │   ├── llm/              # Language model integrations
│   │   │   ├── models/           # Database models
│   │   │   ├── scoring/          # Answer evaluation and scoring
│   │   │   ├── schemas/          # Request and response schemas
│   │   │   └── services/         # Application services
│   │   ├── alembic/              # Database migrations
│   │   ├── tests/                # Backend tests
│   │   └── requirements.txt
│   ├── src/
│   │   ├── components/           # Reusable UI components
│   │   ├── context/              # Application state
│   │   ├── hooks/                # Custom React hooks
│   │   ├── pages/                # Application pages
│   │   ├── services/             # Frontend API integration
│   │   └── styles/               # Styling and themes
│   ├── public/
│   ├── package.json
│   ├── Dockerfile
│   ├── API_SPECIFICATION.md
│   └── README.md
├── All_Project_Documents/
│   └── Project documentation and final deliverables
├── erd.pgerd
├── erd.pgerd.png
├── project_handbook.docx
├── project_handbook.pdf
└── README.md
```

## 🚀 Getting Started

### Prerequisites

Install the following before running the application:

- Python 3.11 or another Python version supported by the backend dependencies
- Node.js and npm
- PostgreSQL
- Git

### 1. Clone the Repository

```bash
git clone https://github.com/nhahub/NHA-5-147.git
cd NHA-5-147/AI_Interview_Coach
```

### 2. Set Up the Backend

Open a terminal in the backend directory:

```bash
cd backend
python -m venv .venv
```

Activate the virtual environment.

**Windows PowerShell:**

```powershell
.\.venv\Scripts\Activate.ps1
```

**macOS / Linux:**

```bash
source .venv/bin/activate
```

Install the dependencies:

```bash
pip install -r requirements.txt
```

Create your local environment file from the provided template:

```powershell
Copy-Item .env.example .env
```

On macOS or Linux:

```bash
cp .env.example .env
```

Configure the environment variables in `.env`, including the database connection and any required authentication or AI-provider settings. Create the PostgreSQL database and user before running migrations.

Apply the database migrations:

```bash
alembic upgrade head
```

Start the backend server:

```bash
uvicorn app.main:app --reload
```

The backend will typically be available at:

- API: `http://127.0.0.1:8000`
- Swagger UI: `http://127.0.0.1:8000/docs`
- Health check: `http://127.0.0.1:8000/health`

### 3. Set Up the Frontend

Open a **second terminal** and navigate to the frontend project:

```bash
cd NHA-5-147/AI_Interview_Coach
npm install
```

Create a local environment file if required by the frontend configuration, then configure the backend API URL according to the project's environment settings.

Start the development server:

```bash
npm run dev
```

Open the local URL displayed in your terminal by Vite.

> **Note:** Environment variable names and provider-specific configuration may vary. Refer to `AI_Interview_Coach/README.md`, `AI_Interview_Coach/API_SPECIFICATION.md`, and the `.env.example` files for the exact project configuration.

## 🧪 Running Tests

From the backend directory, activate the virtual environment and run:

```bash
pytest
```

Some tests require a configured PostgreSQL test database and appropriate environment variables. Configure these before running the complete database-dependent test suite.

## 📚 Documentation

The repository includes supporting materials for understanding the system and its development:

- **[Project Proposal](All_Project_Documents/AI_Capstone_Project_Proposal_Team147.docx)** — project objectives and proposed solution.
- **[Project Handbook (PDF)](project_handbook.pdf)** — project overview and supporting documentation.
- **[Entity Relationship Diagram](erd.pgerd.png)** — visual representation of the database structure.
- **[API Specification](AI_Interview_Coach/API_SPECIFICATION.md)** — API endpoints and expected request/response behavior.
- **[Detailed Project Documents](All_Project_Documents/)** — planning, requirements, system design, implementation, testing, and final deliverables.

## 🔐 Security Notes

- Never commit your actual `.env` files, API keys, database passwords, access tokens, or other secrets.
- Use `.env.example` as a template for local configuration.
- Use strong credentials and appropriate environment-specific settings.
- Keep production secrets outside version control.

## 👥 Team

**DEPI — AWS Machine Learning Track**  
**Graduation Project — Team 147**

Developed as a collaborative project focused on applying software engineering, machine learning, and cloud-oriented development to a practical interview preparation problem.

## 🎯 Project Goal

Our goal is to help candidates prepare more effectively for interviews by combining structured practice, personalized feedback, and actionable improvement guidance in one platform.

---

*Built with Python, React, and a focus on smarter interview preparation.*
