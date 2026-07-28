# System Architecture

## Overview Workflow

```text
[ Candidate Resume (PDF) ] ──► [ React UI ] ──► [ FastAPI Backend ]
                                                       │
                                  ┌────────────────────┴────────────────────┐
                                  ▼                                         ▼
                        [ Text & Skill Parser ]                 [ AI Ranking Engine ]
                          (pdfplumber / spaCy)                (Sentence Transformers)
                                  │                                         │
                                  └────────────────────┬────────────────────┘
                                                       ▼
                                            [ PostgreSQL Database ]
                                                       │
                                                       ▼
                                            [ Dashboard UI Results ]
