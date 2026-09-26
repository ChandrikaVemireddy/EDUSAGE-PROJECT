EduSage --- Admission & Enrollment Portal

A full-stack admissions operations workspace for applicant review,
application tracking, decisions, events, and enrollment analytics.

Project Overview

EduSage is a demonstration admission and enrollment portal built as a
full-stack web application. It brings applicant information, application
status, document checklist progress, review decisions, audit activity,
events, and analytics into one workspace.

The current implementation focuses on a demonstrable end-to-end
admissions workflow:

Dashboard → Applicant Directory → Applicant 360° → Checklist →
AI-assisted review signal → Human Decision → Audit Timeline → Analytics
/ Events

Key Features

Admissions Dashboard

Applicant totals

Submitted applications

Applications under review

Admitted applicants

Application pipeline

Action queue

Recent applicant activity

Applicant Directory

Searchable applicant records

Program, source, score, checklist, and status information

Applicant detail navigation

Applicant 360°

Applicant profile

Application number and fee status

Academic/application score information

Document checklist

Activity and audit timeline

Review & Decisions

Reviewer workflow

AI-assisted review signal

Human decision actions

Admit / Deny / Waitlist / Review status handling

Decision audit event

Events

Admissions event information

Registration/capacity information

Analytics

Status distribution

Program distribution

Applicant source information

Monthly application/admission trend

Technology Stack

Layer      Technology

Frontend   React + Vite
UI Icons   Lucide React
Backend    Python + FastAPI
Database   SQLite
ORM        SQLAlchemy
API        REST

Project Structure

EduSage_Assessment_Final/
├── README.md
├── backend/
│   ├── database.py
│   ├── edusage.db
│   ├── main.py
│   ├── models.py
│   ├── requirements.txt
│   └── seed.py
└── frontend/
    ├── index.html
    ├── package.json
    └── src/
        ├── main.jsx
        └── style.css

Running the Project Locally

1. Start the Backend

cd backend

python -m venv venv

Windows:

venv\Scripts\activate

macOS/Linux:

source venv/bin/activate

Install dependencies:

pip install -r requirements.txt

Seed the demonstration database:

python seed.py

Start FastAPI:

uvicorn main:app --reload --port 8000

Backend:

http://localhost:8000

API documentation:

http://localhost:8000/docs

2. Start the Frontend

Open a second terminal:

cd frontend
npm install
npm run dev

Frontend:

http://localhost:5173

Demonstration Flow

The recommended demo flow is:

Open the Overview dashboard.

Review the admissions pipeline and action queue.

Open Applicants.

Select an applicant to open the Applicant 360° view.

Review checklist completion and application information.

Review the AI-assisted signal.

Submit a human admission decision.

Observe the updated status and audit activity.

Open Events.

Open Analytics to review application trends and distributions.

API Endpoints

The FastAPI backend currently exposes:

GET  /api/health
GET  /api/dashboard
GET  /api/applicants
GET  /api/applicants/{applicant_id}
POST /api/applicants/{applicant_id}/decision
GET  /api/events
GET  /api/analytics

FastAPI's interactive API documentation is available at:

http://localhost:8000/docs

Important Design Principle

EduSage separates automated assistance from the final admission action.
The application provides an AI-assisted review signal, while the actual
decision is explicitly made through the reviewer workflow and recorded
in the audit timeline.

Current Scope

This repository is an assessment/MVP implementation focused on the
strongest demonstrable admissions workflow.

The architecture can be extended for future integrations such as:

Student Information Systems (SIS)

Transcript providers

Payment systems

Communication services

Additional identity/authentication providers

Production-grade deployment infrastructure

Demo Simulation

A separate visual simulation is provided alongside this repository to
demonstrate the intended user journey without requiring a viewer to
install the application first.

Recommended file: EduSage_Simulation.mp4

Project Status

Status: Functional assessment/MVP demonstration

Primary workflow: Applicant review and admission decision

Database: Seeded SQLite demonstration data

Built for demonstration and evaluation

EduSage is designed to make the admissions workflow easier to understand
by bringing applicant operations, review, decisions, events, and
analytics into one interface.
