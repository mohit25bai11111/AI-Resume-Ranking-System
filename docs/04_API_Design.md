# 04. API Design Specification

## Base URL
`http://localhost:8000/api/v1`

---

## Endpoints

### 1. Health Check
* **Endpoint:** `GET /health`
* **Description:** Verifies that the FastAPI backend service is running and responsive.
* **Response (200 OK):**
```json
{
  "status": "healthy",
  "version": "0.1.0"
}
```

---

### 2. Rank Candidates (Core MVP Endpoint)
* **Endpoint:** `POST /rank`
* **Content-Type:** `multipart/form-data`
* **Description:** Uploads multiple candidate resume PDFs and a job description text, processes them through the NLP/AI pipeline, and returns a ranked leaderboard.
* **Form Parameters:**
  * `job_description` (string, required): Full text of the target job description.
  * `files` (array of PDF files, required): Candidate resume files to be evaluated.
* **Response (200 OK):**
```json
{
  "job_id": "job_101",
  "total_candidates": 2,
  "candidates": [
    {
      "rank": 1,
      "filename": "john_doe_resume.pdf",
      "final_score": 88.5,
      "skill_match_score": 100.0,
      "semantic_score": 77.0,
      "matched_skills": [
        "python",
        "fastapi",
        "postgresql"
      ],
      "extracted_skills": [
        "python",
        "fastapi",
        "postgresql",
        "docker"
      ]
    },
    {
      "rank": 2,
      "filename": "jane_smith_cv.pdf",
      "final_score": 64.0,
      "skill_match_score": 66.6,
      "semantic_score": 61.4,
      "matched_skills": [
        "python",
        "postgresql"
      ],
      "extracted_skills": [
        "python",
        "postgresql",
        "java"
      ]
    }
  ]
}
```
* **Error Response (400 Bad Request):**
```json
{
  "detail": "Invalid file format. Only PDF files are accepted."
}
```

---

### 3. Get All Candidate Rankings
* **Endpoint:** `GET /candidates`
* **Description:** Fetches historical candidate evaluation records and ranking data stored in the database.
* **Query Parameters:**
  * `limit` (integer, optional, default: 50): Maximum number of records to return.
  * `offset` (integer, optional, default: 0): Pagination offset.
* **Response (200 OK):**
```json
{
  "total": 1,
  "history": [
    {
      "id": 1,
      "job_title": "Backend Developer",
      "top_candidate": "john_doe_resume.pdf",
      "top_score": 88.5,
      "created_at": "2026-07-28T10:00:00Z"
    }
  ]
}
```
