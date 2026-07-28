# 02. System Requirements

## Functional Requirements (FR)

### FR1: Resume Management
* The system shall allow users to upload single or multiple PDF resumes.
* The system shall extract raw text content while preserving spatial reading order.

### FR2: Skill & Metadata Extraction
* The system shall extract candidate contact information (email, phone number).
* The system shall match candidate skills against a predefined technology dictionary using regex and `spaCy`.

### FR3: Job Description Analysis
* The system shall allow recruiters to input a text-based Job Description (JD).
* The system shall extract key skills required from the JD.

### FR4: Candidate Ranking
* The system shall calculate a **Skill Match Score** based on Jaccard similarity.
* The system shall calculate a **Semantic Similarity Score** using Sentence Transformer embeddings.
* The system shall aggregate scores into a final ranking (0–100%).

### FR5: Recruiter Dashboard
* The system shall display candidate rankings in descending order of match percentage.
* The system shall display matched vs. missing skills for each candidate.

---

## Non-Functional Requirements (NFR)

* **Performance:** Processing and ranking up to 10 resumes must complete in under 5 seconds.
* **Usability:** The user interface must be clean, intuitive, and require minimal technical setup for recruiters.
* **Scalability:** The database schema must support scaling from local SQLite to production PostgreSQL seamlessly.
* **Accuracy:** Entity parsing accuracy for standard technical skills should exceed 85%.

---

## MVP Scope Boundaries
* **In-Scope:** PDF parsing, skill extraction, JD comparison, candidate ranking leaderboard.
* **Out-of-Scope (Future Phase):** Multi-tenant authentication, email notifications, dynamic interview question generation.
