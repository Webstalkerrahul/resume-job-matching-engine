<div align="center">

# 🤖 Resume ↔ Job Matching Engine  
### AI-Powered Semantic Job Recommendation System

![Python](https://img.shields.io/badge/Python-3.9+-blue)
![NLP](https://img.shields.io/badge/NLP-SentenceBERT-green)
![FAISS](https://img.shields.io/badge/Vector_Search-FAISS-orange)
![FastAPI](https://img.shields.io/badge/Backend-FastAPI-teal)
![Streamlit](https://img.shields.io/badge/Frontend-Streamlit-red)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

</div>

---

## ✨ What is this?

An **end-to-end AI system** that matches resumes to the most relevant job descriptions using **semantic understanding**, not just keywords.

It uses:

- 🧠 Sentence-BERT for embeddings  
- ⚡ FAISS for fast similarity search  
- 🚀 FastAPI for backend  
- 🎨 Streamlit for UI  

---

## 🎯 Why this project is unique

❌ Traditional systems → keyword matching  
✅ This system → **meaning-based matching**

It understands that:

> “Data Scientist with NLP experience”  
≈  
> “Machine learning engineer working on text analytics”

---

## 🧠 Architecture

┌──────────────┐
│ Resume Text  │
└──────┬───────┘
↓
┌──────────────┐
│ Preprocessing│
└──────┬───────┘
↓
┌────────────────────┐
│ Sentence-BERT Model│
└──────┬─────────────┘
↓
┌──────────────┐
│ FAISS Index │◄── Job Embeddings
└──────┬───────┘
↓
┌──────────────┐
│ Ranking Engine│
└──────┬───────┘
↓
┌──────────────┐
│ FastAPI API │
└──────┬───────┘
↓
┌──────────────┐
│ Streamlit UI │
└──────────────┘


## 🛠 Tech Stack

| Layer | Technology |
|-------|------------|
| Language | Python |
| NLP | SentenceTransformers (SBERT) |
| Vector Search | FAISS |
| Backend | FastAPI |
| Frontend | Streamlit |
| Data | Kaggle |
| Deployment | Docker (optional) |

---

## 📂 Project Structure

resume-job-matching-engine/
│
├── data/
│ ├── raw/
│ └── processed/
│
├── models/
│
├── src/
│ ├── preprocessing.py
│ ├── embedding.py
│ ├── faiss_index.py
│ ├── matcher.py
│ └── build_system.py
│
├── backend/
│ └── api.py
│
├── frontend/
│ └── app.py
│
├── requirements.txt
├── README.md
└── .gitignore

---

## 📊 Datasets

📌 From Kaggle:

- Resume Dataset  
- Job Descriptions Dataset  

> Datasets are not included due to license and size.

---

## ⚙️ Installation Guide

### 1️⃣ Clone repository

```bash
git clone https://github.com/yourusername/resume-job-matching-engine.git
```

```bash
cd resume-job-matching-engine
```

2️⃣ Create a virtual environment
```python
python -m venv venv
```
or 
```bash
uv sync
```

activate virtual environment
```bash
.venv\Scripts\activate
```

3️⃣ Install dependencies
```bash
pip install -r requirements.txt
```

4️⃣ Add datasets
data/raw/resumes.csv
data/raw/jobs.csv

5️⃣ Build FAISS index (one time)
```bash
python src/build_system.py
```

6️⃣ Run backend
``` bash
uvicorn backend.api:app --reload
```
📍 API: http://127.0.0.1:8000
📍 Docs: http://127.0.0.1:8000/docs

7️⃣ Run frontend
```bash
streamlit run frontend/app.py
```

Results:
✔ Data Scientist – Google
✔ NLP Engineer – Amazon
✔ ML Engineer – Microsoft
📈 Resume Value
This project demonstrates:

✔ NLP in production

✔ Vector databases

✔ API engineering

✔ Full ML pipeline

✔ System design

✔ Real-world problem solving
