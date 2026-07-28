# 06. Weekly Progress Tracker

## Project Timeline & Milestones

| Week | Development Phase | Key Deliverables & Goals | Status |
| :---: | :--- | :--- | :---: |
| **Week 1** | Project Initiation | Scope definition, stack finalization, & initial repo setup | ✅ Completed |
| **Week 2** | Design & Architecture | Documentation suite creation, architecture diagrams, & task allocation | ✅ Completed |
| **Week 3** | Environment & Core PoC | FastAPI/React boilerplates, PDF parsing with `pdfplumber`, & spaCy matcher | 🔄 In Progress |
| **Week 4** | AI Scoring & UI Dev | Sentence Transformers (`all-MiniLM-L6-v2`) & React Dashboard UI | ⏳ Scheduled |
| **Week 5** | Database & API Integration | Database ORM integration & End-to-End API linking | ⏳ Scheduled |
| **Week 6** | Testing & Presentation | Edge case testing, demo video, slide deck, & final report | ⏳ Scheduled |

---

## Detailed Weekly Progress Logs

### Week 1: Project Initiation & Setup
* **Focus:** Defining scope and initializing codebase repository.
* **Key Accomplishments:**
  * Finalized project concept: AI Resume Parser & Ranking System.
  * Selected stack: React (Vite + Tailwind CSS), FastAPI, PostgreSQL, spaCy, Sentence Transformers.
  * Initialized GitHub repository with base folder structure (`/backend`, `/frontend`, `/docs`, `/datasets`).
* **Status:** ✅ Completed

---

### Week 2: System Architecture & Documentation
* **Focus:** Comprehensive system design and documentation suite setup.
* **Key Accomplishments:**
  * Created full 10-file documentation suite inside `/docs/`.
  * Designed clear architecture diagrams and defined system workflow.
  * Formalized team role assignments across all 6 members.
  * Defined core REST API endpoints and relational database schema.
* **Status:** ✅ Completed

---

### Week 3: Backend Boilerplate & Parsing Engine PoC
* **Focus:** Dev environment configuration and text extraction PoCs.
* **Target Tasks:**
  * Set up FastAPI backend boilerplate and virtual environment dependencies.
  * Set up Vite React frontend with Tailwind CSS styling.
  * Implement `pdfplumber` script to extract clean text from candidate PDF resumes.
  * Configure `spaCy` entity matcher for candidate skill extraction.
* **Status:** 🔄 In Progress

---

### Week 4: Semantic AI Model & Frontend Dashboard
* **Focus:** Vector embedding scoring and recruiter UI dashboard.
* **Target Tasks:**
  * Integrate `SentenceTransformer('all-MiniLM-L6-v2')` model.
  * Compute cosine similarity between JD embeddings and resume embeddings.
  * Build React component for resume drag-and-drop upload.
  * Build Recruiter Leaderboard view with matched skill badges.
* **Status:** ⏳ Scheduled

---

### Week 5: Database Integration & End-to-End Flow
* **Focus:** Persisting evaluation results and connecting API endpoints.
* **Target Tasks:**
  * Configure SQLAlchemy models for candidates, jobs, and rankings.
  * Connect `POST /api/v1/rank` endpoint to Frontend interface via Axios.
  * Verify end-to-end execution: Upload PDF ➔ Parse Text ➔ AI Score ➔ Store DB ➔ Render UI.
* **Status:** ⏳ Scheduled

---

### Week 6: Testing, Refinement, & Exhibition Prep
* **Focus:** Quality assurance, system performance, and presentation assets.
* **Target Tasks:**
  * Perform edge-case testing (handling irregular PDF layouts and missing skills).
  * Build project exhibition slide deck (`09_Presentation.md`).
  * Record a backup product demo video and finalize report (`10_Final_Report.md`).
* **Status:** ⏳ Scheduled
