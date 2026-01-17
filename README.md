Resume ↔ Job Matching Engine

AI-Powered Semantic Job Recommendation System

📌 Overview

This project is an end-to-end AI-powered resume to job matching system that uses Natural Language Processing (NLP) and semantic similarity to recommend the most relevant job postings for a given resume.

Unlike traditional keyword matching, this system understands context and meaning using Sentence-BERT embeddings and performs fast similarity search using FAISS.

🚀 Features

Resume text matching using semantic similarity

NLP embeddings with Sentence-BERT

Fast vector similarity search using FAISS

Job ranking based on relevance

REST API using FastAPI

Interactive web UI using Streamlit

Scalable architecture

Easily extendable for PDF upload & filters

🧠 System Architecture
Resume Text
     |
Text Preprocessing
     |
Sentence-BERT Embeddings
     |
FAISS Vector Index
     |
Top-K Job Matches
     |
FastAPI Backend
     |
Streamlit Frontend UI

🛠 Tech Stack
Category	Tools
Language	Python
NLP	SentenceTransformers (SBERT)
Vector Search	FAISS
Backend	FastAPI
Frontend	Streamlit
Data	Kaggle datasets
Deployment Ready	Docker (optional)
📂 Project Structure
resume-job-matching-engine/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── models/
│
├── notebooks/
│
├── src/
│   ├── preprocessing.py
│   ├── embedding.py
│   ├── faiss_index.py
│   ├── matcher.py
│   └── build_system.py
│
├── backend/
│   └── api.py
│
├── frontend/
│   └── app.py
│
├── requirements.txt
├── README.md
└── .gitignore

📊 Datasets Used

Resume Dataset – Kaggle

Job Descriptions Dataset – Kaggle

(Datasets are not included in this repository due to size and license constraints.)

⚙️ Installation & Setup
1️⃣ Clone Repository
git clone https://github.com/yourusername/resume-job-matching-engine.git
cd resume-job-matching-engine

2️⃣ Create Virtual Environment
python -m venv venv
venv\Scripts\activate

3️⃣ Install Dependencies
pip install -r requirements.txt

4️⃣ Add Datasets

Place datasets in:

data/raw/resumes.csv
data/raw/jobs.csv


Ensure job description column name matches the one used in build_system.py.

5️⃣ Build Vector Index (One-time)
python src/build_system.py


This generates:

models/index.faiss
data/processed/jobs.csv

6️⃣ Start Backend API
uvicorn backend.api:app --reload


API will run at:

http://127.0.0.1:8000


Swagger UI:

http://127.0.0.1:8000/docs

7️⃣ Start Frontend UI

Open a new terminal:

streamlit run frontend/app.py

🖥 UI Preview

Users can:

Paste resume text

Click Find Matching Jobs

View ranked job results with similarity scores

📈 Resume Impact

This project demonstrates:

Applied NLP in real-world recruitment systems

Vector similarity search at scale

API development

ML system design

Full-stack data science deployment

🧪 Sample Resume Bullet Points

Built an AI-powered resume-to-job matching engine using Sentence-BERT and FAISS achieving semantic job recommendations.
Designed full ML pipeline including text preprocessing, embedding generation, vector indexing, REST API (FastAPI), and interactive UI (Streamlit).
Implemented scalable semantic search over thousands of job descriptions.

🔮 Future Improvements

PDF resume upload support

Skill extraction using spaCy

Location & salary filtering

Cosine similarity scoring

User authentication

Docker deployment

Cloud hosting (Render / AWS / HuggingFace Spaces)

⚠️ Notes

Large datasets are excluded from version control.

Ensure correct dataset column names before building the system.

📜 License

MIT License

👤 Author

Your Name
LinkedIn: your-link
GitHub: your-username