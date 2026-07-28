# 07. Testing Strategy & Cases

## Test Matrix

### 1. Resume Parsing Unit Tests (`pdfplumber` + `spaCy`)
* **TC-PARSER-01:** Verify text extraction from standard single-column PDF resumes.
* **TC-PARSER-02:** Verify skill extraction accuracy using sample resumes containing standard technology names (e.g., Python, React, Docker).
* **TC-PARSER-03:** Verify parser stability when handling empty or corrupted PDF files.

### 2. AI Scoring Unit Tests (`Sentence Transformers`)
* **TC-AI-01:** High relevance check—Verify that a Python Developer resume scores above 80% against a Python Developer JD.
* **TC-AI-02:** Low relevance check—Verify that a Graphic Designer resume scores below 40% against a Senior Backend Engineer JD.

### 3. Integration Tests (API Endpoints)
* **TC-API-01:** Test `POST /api/v1/rank` with valid PDF uploads and verify structured JSON response layout.
