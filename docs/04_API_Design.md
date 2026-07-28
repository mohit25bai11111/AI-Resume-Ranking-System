# 04. API Design Specification

## Base URL
`http://localhost:8000/api/v1`

---

## Endpoints

### 1. Health Check
* **Endpoint:** `GET /health`
* **Description:** Verifies backend service status.
* **Response (200 OK):**
```json
{
  "status": "healthy",
  "version": "0.1.0"
}
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
      "matched_skills": ["python", "fastapi", "postgresql"],
      "extracted_skills": ["python", "fastapi", "postgresql", "docker"]
    },
    {
      "rank": 2,
      "filename": "jane_smith_cv.pdf",
      "final_score": 64.0,
      "skill_match_score": 66.6,
      "semantic_score": 61.4,
      "matched_skills": ["python", "postgresql"],
      "extracted_skills": ["python", "postgresql", "java"]
    }
  ]
}
