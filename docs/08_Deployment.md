# 08. Deployment Guide

## Local Development Setup

### 1. Prerequisites
* Python 3.10 or higher
* Node.js v18 or higher
* Git

### 2. Backend Setup
```bash
cd backend
python -m venv venv
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate

pip install -r requirements.txt
python -m spacy download en_core_web_sm
uvicorn app.main:app --reload
