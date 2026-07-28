# 05. Database Design & Schema

## Entity Relationship Summary
* A **Job** can have many **Rankings**.
* A **Candidate** can be evaluated across multiple **Rankings**.

---

## Tables Specification

### Table: `jobs`
| Column Name | Data Type | Constraints | Description |
| :--- | :--- | :--- | :--- |
| `id` | INTEGER | PRIMARY KEY, AUTOINCREMENT | Unique job ID |
| `title` | VARCHAR(255) | NOT NULL | Job title |
| `description_text` | TEXT | NOT NULL | Full JD text |
| `created_at` | TIMESTAMP | DEFAULT CURRENT_TIMESTAMP | Record creation time |

---

### Table: `candidates`
| Column Name | Data Type | Constraints | Description |
| :--- | :--- | :--- | :--- |
| `id` | INTEGER | PRIMARY KEY, AUTOINCREMENT | Unique candidate ID |
| `filename` | VARCHAR(255) | NOT NULL | Original PDF file name |
| `raw_text` | TEXT | NOT NULL | Extracted raw text from PDF |
| `extracted_skills` | JSONB / TEXT | NULLABLE | Parsed array of skills |
| `created_at` | TIMESTAMP | DEFAULT CURRENT_TIMESTAMP | Upload timestamp |

---

### Table: `rankings`
| Column Name | Data Type | Constraints | Description |
| :--- | :--- | :--- | :--- |
| `id` | INTEGER | PRIMARY KEY, AUTOINCREMENT | Unique ranking ID |
| `job_id` | INTEGER | FOREIGN KEY (`jobs.id`) | Target job reference |
| `candidate_id` | INTEGER | FOREIGN KEY (`candidates.id`) | Candidate reference |
| `skill_score` | FLOAT | NOT NULL | Skill overlap percentage |
| `semantic_score` | FLOAT | NOT NULL | Vector similarity score |
| `final_score` | FLOAT | NOT NULL | Weighted final score |
| `ranked_at` | TIMESTAMP | DEFAULT CURRENT_TIMESTAMP | Evaluation timestamp |
