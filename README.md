# 🤖 AI Resume Parser & Ranking System

> **An AI-powered Applicant Screening System that parses resumes, extracts candidate information, compares resumes with job descriptions, and ranks candidates using Natural Language Processing (NLP) and Machine Learning.**

---

## 📖 Project Overview

Recruiters often spend hours manually reviewing hundreds of resumes for a single job opening. This project automates the initial screening process by using AI to analyze resumes, extract relevant information, compare them against a job description, and rank candidates based on their suitability.

The system aims to reduce recruitment time while providing a fair and data-driven candidate ranking.

---

## 🎯 Problem Statement

Traditional recruitment involves:

- ❌ Manual resume screening
- ❌ Time-consuming candidate shortlisting
- ❌ Human bias during evaluation
- ❌ Difficulty comparing hundreds of resumes

Our solution provides an intelligent AI-based ranking system that automates these tasks.

---

# ✨ Features

### 📄 Resume Management
- Upload multiple PDF/DOCX resumes
- Secure resume storage
- Resume preview

### 🧠 AI Resume Parser
- Extract candidate name
- Extract email & phone number
- Detect technical skills
- Extract education details
- Extract work experience
- Identify certifications

### 💼 Job Description Analysis
- Upload or paste Job Description
- Keyword extraction
- Skill extraction

### 🤖 AI Ranking Engine
- Resume similarity scoring
- Skill matching
- Experience matching
- Education comparison
- Final ranking score

### 📊 Dashboard
- Candidate list
- Ranking score
- Resume details
- Search & Filter
- Download results

---

# 🏗️ System Architecture

```text
                    React Frontend
                           │
                           │ REST API
                           ▼
                    FastAPI Backend
        ┌──────────────┼──────────────┐
        │              │              │
        ▼              ▼              ▼
 Resume Parser    AI Ranking      Database
        │              │
        └───────► NLP Engine ◄────────┘
```

---

# 🛠️ Tech Stack

| Category | Technology |
|-----------|------------|
| Frontend | React + Vite |
| Backend | FastAPI |
| Language | Python |
| Database | PostgreSQL |
| AI/NLP | spaCy |
| ML | Sentence Transformers |
| Styling | Tailwind CSS |
| Version Control | Git & GitHub |

---

# 📂 Project Structure

```text
AI-Resume-Ranking-System/
│
├── backend/              # FastAPI Backend
│
├── frontend/             # React Frontend
│
├── datasets/             # Sample resumes & datasets
│
├── docs/                 # Project documentation
│
├── screenshots/          # UI screenshots
│
├── README.md
└── .gitignore
```

---

# 🔄 Project Workflow

```text
Candidate Uploads Resume
            │
            ▼
Resume Parser extracts information
            │
            ▼
Job Description Analysis
            │
            ▼
AI compares Resume & Job Description
            │
            ▼
Similarity Score Generated
            │
            ▼
Candidates Ranked
            │
            ▼
Results Displayed on Dashboard
```

---

# 📅 Development Timeline

| Week | Milestone |
|------|-----------|
| ✅ Week 1 | Repository Setup & Planning |
| 🔄 Week 2 | Backend + Frontend Setup |
| ⏳ Week 3 | Resume Parsing |
| ⏳ Week 4 | AI Ranking Engine |
| ⏳ Week 5 | Dashboard & Database |
| ⏳ Week 6 | Testing & Deployment |

---

# 👥 Team Members

| Member | Name | Responsibility |
|--------------|------------|---------------|
| 👨‍💻 Member 1 |  **Mohit Pillai**          | Project Lead & Backend |
| 🎨 Member 2 |           |Frontend Development |
| 📄 Member 3 |           |Resume Parser |
| 🧠 Member 4 |           |AI Ranking Engine |
| 🗄️ Member 5 |           |Database |
| 🧪 Member 6 |  **Chitransh goyal**       |Testing & Documentation |

---

# 🚀 Future Enhancements

- 🔐 User Authentication
- ☁️ Cloud Deployment
- 📧 Email Notifications
- 📈 Analytics Dashboard
- 🤖 AI Interview Question Generator
- 🏢 HR Admin Panel

---

# 📸 Screenshots

Screenshots will be added as development progresses.

---

# 📜 License

This project is developed for academic purposes as part of the **AIML Second-Year Project Exhibition**.

---

# ⭐ Project Status

🚧 **Currently Under Development**

Version: **v0.1.0**

---

## 💡 Goal

> **"Build an intelligent AI-powered recruitment assistant that helps recruiters identify the best candidates quickly, accurately, and fairly."**
