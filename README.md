# 🎓 EduSage — Admission & Enrollment Portal

> **A modern admissions operations workspace that brings applicant review, application tracking, decisions, events, and enrollment analytics together in one place.**

---

## ✨ What is EduSage?

**EduSage** is a full-stack admission and enrollment portal designed to make the admissions journey easier to understand and manage.

Instead of spreading applicant information, documents, decisions, activities, and analytics across different places, EduSage brings them together into a single workspace.

### 🚀 The journey at a glance

**📊 Dashboard → 👥 Applicants → 🧾 Applicant 360° → ✅ Checklist → 🤖 Review Signal → 👤 Human Decision → 📝 Audit Timeline → 📈 Analytics**

The result is a clear, structured workflow from **application review to admission decision**.

---

## 🌟 Key Features

### 📊 Admissions Dashboard

Get an instant overview of the current admissions cycle.

* 👥 Total applicants
* 📩 Submitted applications
* 🔍 Applications under review
* 🎓 Admitted applicants
* 📈 Application pipeline
* ⚡ Action queue
* 🕒 Recent applicant activity

---

### 👥 Applicant Directory

A centralized workspace for discovering and reviewing applicants.

* 🔎 Searchable applicant records
* 🎓 Program information
* 📣 Applicant source
* 📊 Application score
* 📋 Checklist progress
* 🏷️ Application status
* ➡️ Direct access to applicant details

---

### 🧑‍💻 Applicant 360°

A complete view of an applicant's application journey.

View:

* 👤 Applicant profile
* 🆔 Application number
* 💳 Fee status
* 📚 Academic/application score
* 📑 Document checklist
* 🕒 Activity history
* 📝 Audit timeline

Everything needed for a review is brought together in one place.

---

### 🤖 Review & Decisions

EduSage combines automated assistance with a human-controlled decision workflow.

**Review → Assess → Decide → Record**

Features include:

* 🤖 AI-assisted review signal
* 👤 Human reviewer workflow
* ✅ Admit
* ❌ Deny
* ⏳ Waitlist
* 🔍 Review
* 📝 Decision audit event

> **Important:** The AI-assisted signal supports the review process; the final admission action is explicitly made through the reviewer workflow.

---

### 📅 Events

Keep track of admissions-related events and participation information.

* 📅 Event information
* 👥 Registration details
* 🎯 Capacity information

---

### 📈 Analytics

Turn application data into an easy-to-understand overview.

Explore:

* 📊 Status distribution
* 🎓 Program distribution
* 📣 Applicant sources
* 📅 Monthly application trends
* 🎯 Admission trends

---

# 🛠️ Technology Stack

| Layer        | Technology           |
| ------------ | -------------------- |
| 🎨 Frontend  | **React + Vite**     |
| ✨ UI Icons   | **Lucide React**     |
| ⚙️ Backend   | **Python + FastAPI** |
| 🗄️ Database | **SQLite**           |
| 🔗 ORM       | **SQLAlchemy**       |
| 🌐 API       | **REST**             |

---

# 🗂️ Project Structure

```text
EduSage_Assessment_Final/
│
├── 📄 README.md
│
├── ⚙️ backend/
│   ├── database.py
│   ├── edusage.db
│   ├── main.py
│   ├── models.py
│   ├── requirements.txt
│   └── seed.py
│
└── 🎨 frontend/
    ├── index.html
    ├── package.json
    └── src/
        ├── main.jsx
        └── style.css
```

---

# 🚀 Run EduSage Locally

## 1️⃣ Start the Backend

Open a terminal:

```bash
cd backend
```

Create a virtual environment:

```bash
python -m venv venv
```

### Windows

```bash
venv\Scripts\activate
```

### macOS / Linux

```bash
source venv/bin/activate
```

Install the backend dependencies:

```bash
pip install -r requirements.txt
```

Seed the demonstration database:

```bash
python seed.py
```

Start FastAPI:

```bash
uvicorn main:app --reload --port 8000
```

### ⚙️ Backend

```text
http://localhost:8000
```

### 📚 API Documentation

```text
http://localhost:8000/docs
```

---

## 2️⃣ Start the Frontend

Open a **second terminal**:

```bash
cd frontend
```

Install dependencies:

```bash
npm install
```

Start the development server:

```bash
npm run dev
```

### 🎨 Frontend

```text
http://localhost:5173
```

---

# 🎬 Demonstration Flow

Want to understand EduSage quickly?

Follow this workflow:

```text
📊 Overview
     ↓
👥 Applicants
     ↓
🧑 Applicant 360°
     ↓
📋 Checklist
     ↓
🤖 AI-Assisted Review Signal
     ↓
👤 Human Decision
     ↓
📝 Audit Activity
     ↓
📅 Events
     ↓
📈 Analytics
```

### Suggested demo walkthrough

1. 📊 Open the **Overview** dashboard.
2. 📈 Review the admissions pipeline and action queue.
3. 👥 Open **Applicants**.
4. 🧑 Select an applicant.
5. 📋 Review application information and checklist progress.
6. 🤖 Examine the AI-assisted review signal.
7. 👤 Submit a human admission decision.
8. 📝 Observe the updated status and audit activity.
9. 📅 Explore **Events**.
10. 📈 Finish with **Analytics**.

---

# 🔌 API Endpoints

The FastAPI backend exposes the following endpoints:

| Method | Endpoint                                  | Purpose             |
| ------ | ----------------------------------------- | ------------------- |
| `GET`  | `/api/health`                             | Health check        |
| `GET`  | `/api/dashboard`                          | Dashboard data      |
| `GET`  | `/api/applicants`                         | Applicant directory |
| `GET`  | `/api/applicants/{applicant_id}`          | Applicant details   |
| `POST` | `/api/applicants/{applicant_id}/decision` | Submit decision     |
| `GET`  | `/api/events`                             | Admissions events   |
| `GET`  | `/api/analytics`                          | Analytics data      |

Interactive API documentation:

```text
http://localhost:8000/docs
```

---

# 🧠 Design Principle

EduSage is designed around a simple principle:

> **Automation can assist the review process, but the final admission action remains a human decision.**

The application provides an **AI-assisted review signal**, while the actual decision is explicitly made through the reviewer workflow and recorded in the audit timeline.

This keeps the workflow transparent and makes the decision process easier to follow.

---

# 📦 Current Scope

EduSage is currently presented as a **functional assessment/MVP demonstration** focused on the core admissions workflow.

The architecture can be extended in future iterations with integrations such as:

* 🏫 Student Information Systems (SIS)
* 📚 Transcript providers
* 💳 Payment systems
* 💬 Communication services
* 🔐 Additional identity/authentication providers
* ☁️ Production-grade deployment infrastructure

---

# 🎥 Demo Simulation

A separate visual simulation is provided alongside the source project.

The simulation demonstrates the main EduSage journey without requiring viewers to install the application first.

### 🎬 Simulation

**`EduSage_Simulation.mp4`**

The video demonstrates:

**Dashboard → Applicants → Applicant 360° → Review → Decision → Analytics**

> The simulation video is intentionally kept **separate from the project ZIP**.

---

# 📌 Project Status

| Area                  | Status          |
| --------------------- | --------------- |
| 🎨 Frontend           | ✅ Functional    |
| ⚙️ Backend            | ✅ Functional    |
| 🗄️ Database          | ✅ Seeded SQLite |
| 👥 Applicant workflow | ✅ Implemented   |
| 🤖 Review signal      | ✅ Demonstrated  |
| 👤 Decision workflow  | ✅ Implemented   |
| 📝 Audit activity     | ✅ Demonstrated  |
| 📅 Events             | ✅ Implemented   |
| 📈 Analytics          | ✅ Demonstrated  |
| 🎬 Simulation         | ✅ Provided      |

### 🏁 Status

**Functional Assessment / MVP Demonstration**

**Primary Workflow:** Applicant Review & Admission Decision

**Database:** Seeded SQLite Demonstration Data

---

# 💡 Why EduSage?

EduSage brings the important parts of the admissions workflow into **one clear operational workspace**.

Instead of viewing admissions as disconnected steps, the platform connects:

**Applicants + Applications + Documents + Review + Decisions + Events + Analytics**

into a single journey.

---

## 🎓 EduSage

### *From application to decision — one connected admissions workspace.*

---

**Built for demonstration, evaluation, and future expansion.**
