# 01. Project Overview

## Project Title
**AI Resume Parser & Ranking System**

## Executive Summary
The AI Resume Parser & Ranking System is an intelligent recruitment tool designed to automate candidate screening. By extracting structured metadata from unstructured PDF resumes and evaluating candidates against specific Job Descriptions (JDs) using NLP and machine learning, the system provides an objective, data-driven candidate leaderboard.

## Problem Statement
* **High Volume of Applicants:** Recruiters receive hundreds of resumes for a single opening, creating a massive manual bottleneck.
* **Human Bias & Inconsistency:** Manual shortlisting can introduce subjective bias and variable evaluation criteria.
* **Keyword Matching Limitations:** Traditional keyword search fails to understand semantic context (e.g., missing that "ML" and "Machine Learning" represent the same domain).

## Proposed Solution
An automated pipeline that parses PDF resumes, categorizes candidate skills, computes semantic alignment against job requirements, and ranks applicants transparently on an interactive dashboard.

## Key Features
1. **Multi-Resume Upload:** Batch upload PDF files.
2. **Text & Skill Extraction:** Automated parsing using `pdfplumber` and `spaCy`.
3. **Semantic Similarity Scoring:** Context-aware scoring using Sentence Transformers (`all-MiniLM-L6-v2`).
4. **Weighted Ranking Engine:** Combined skill overlap and semantic matching.
5. **Interactive Dashboard:** Recruiter leaderboard with detailed candidate breakdowns.

## Project Scope
* **Target Audience:** Recruiters, HR Teams, and Hiring Managers.
* **Context:** AIML Second-Year Project Exhibition.
