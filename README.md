# 📚 RAG Knowledge Assistant

A modular **Retrieval-Augmented Generation (RAG)** application that allows users to ask questions and get answers using information retrieved from uploaded documents.

The project combines **RAG, LangChain, FastAPI, Streamlit, ChromaDB, Hugging Face embeddings, and OpenAI LLMs**.

---

## 🚀 Features

- 📄 Document-based Question Answering
- 🔍 Semantic Search using Vector Embeddings
- 🧠 Retrieval-Augmented Generation (RAG)
- 🤖 OpenAI LLM integration
- 🔀 Automatic query routing
- 📚 ChromaDB vector store
- ⚡ FastAPI backend
- 🖥️ Streamlit frontend
- 📊 RAG evaluation support
- 🧩 Modular project architecture

---

## 🧠 How It Works

```text
User Question
      ↓
Query Router
      ↓
Document Query / General Query
      ↓
Retriever
      ↓
ChromaDB Vector Store
      ↓
Relevant Document Chunks
      ↓
Prompt + Context
      ↓
OpenAI LLM
      ↓
Structured Answer
      ↓
User
Today 7:14 PM
mujje bhi ayesha redme me banana hai kaya karu

Haan 👍 Aap apne rag_project ke liye bilkul isi type ka professional README bana sakte ho. Screenshot wale README me mainly project title, badges, description, Live Demo, How It Works, Features, Tech Stack, Run instructions hote hain.

Aapke project ke according hum README banayenge.

Step 1 — README.md file open karo

Aapke project ka path:

C:\Users\lenovo\Desktop\rag_project

Is folder me ek file honi chahiye:

README.md

Agar nahi hai, PowerShell me ye command chalao:

New-Item README.md

Phir:

code README.md

Abhi sirf README.md open karo.
Mujhe screenshot bhej do ki file open ho gayi hai.

Uske baad main aapko aapke actual RAG project ke liye ready-to-copy professional README dunga, screenshot wale format jaisa.

Haan, ab samajh gaya 👍

Aapke GitHub repo me README.md already present hai. Isliye nayi file banane ki zarurat nahi hai.

Screenshot me README.md ke saamne “add all file” aur 2 months ago dikh raha hai — matlab purana README hai. Hume ise update karna hai.

Abhi sirf ye karo 👇

GitHub me README.md par click karo.

Phir mujhe uska screenshot bhejo.

Uske baad main aapke actual RAG project ke liye README ka complete content bana dunga, jisme:

📚 RAG Knowledge Assistant title
🏷️ Python / LangChain / FastAPI / Streamlit / ChromaDB badges
📝 Project description
⚙️ How It Works
🔄 RAG Pipeline
✨ Features
🏗️ Project Structure
🚀 Installation & Run
🔑 Environment Variables
🌐 Render Deployment
🖥️ Frontend + Backend
📊 Evaluation

Screenshot wale README jaisa professional format, lekin content aapke project ka hoga.

Perfect 👍 Abhi aap README.md edit screen par ho. Jo line likhi hai:

my fisr rag project

use poora delete karna hai.

Step 2 — Ye complete README paste karo

Editor ke andar Ctrl + A → Delete → neeche wala content paste karo:

# 📚 RAG Knowledge Assistant

A modular **Retrieval-Augmented Generation (RAG)** application that allows users to ask questions and get answers using information retrieved from uploaded documents.

The project combines **RAG, LangChain, FastAPI, Streamlit, ChromaDB, Hugging Face embeddings, and OpenAI LLMs**.

---

## 🚀 Features

- 📄 Document-based Question Answering
- 🔍 Semantic Search using Vector Embeddings
- 🧠 Retrieval-Augmented Generation (RAG)
- 🤖 OpenAI LLM integration
- 🔀 Automatic query routing
- 📚 ChromaDB vector store
- ⚡ FastAPI backend
- 🖥️ Streamlit frontend
- 📊 RAG evaluation support
- 🧩 Modular project architecture

---

## 🧠 How It Works

```text
User Question
      ↓
Query Router
      ↓
Document Query / General Query
      ↓
Retriever
      ↓
ChromaDB Vector Store
      ↓
Relevant Document Chunks
      ↓
Prompt + Context
      ↓
OpenAI LLM
      ↓
Structured Answer
      ↓
User
🔄 RAG Pipeline
1. Document Ingestion

Source documents are loaded from:

data/raw/

The documents are then divided into smaller chunks.

2. Embedding

Each document chunk is converted into a vector embedding using a Hugging Face embedding model.

3. Vector Store

The embeddings are stored in ChromaDB for semantic similarity search.

4. Retrieval

When the user asks a document-related question, the system retrieves the most relevant chunks from ChromaDB.

5. Generation

The retrieved context is passed to the LLM along with the user's question.

The LLM generates the final answer based on the retrieved information.

🏗️ Project Structure
rag_project/
│
├── backend/
│   ├── main.py
│   └── __init__.py
│
├── data/
│   └── raw/
│       └── documents
│
├── evaluation/
│   ├── evaluate.py
│   ├── testset.json
│   └── __init__.py
│
├── frontend/
│   ├── app.py
│   └── __init__.py
│
├── generation/
│   ├── llm.py
│   ├── parser.py
│   └── prompt.py
│
├── ingestion/
│   ├── loader.py
│   ├── splitter.py
│   ├── embed_store.py
│   └── run_ingestion.py
│
├── retrieval/
│   ├── retriever.py
│   └── __init__.py
│
├── routing/
│   ├── query_router.py
│   └── __init__.py
│
├── vectorstore/
│
├── .env.example
├── .gitignore
├── requirement.txt
└── README.md
🛠️ Tech Stack
Technology	Purpose
Python	Core programming language
LangChain	RAG orchestration
FastAPI	Backend API
Streamlit	Frontend UI
ChromaDB	Vector database
Hugging Face	Embedding model
OpenAI	LLM generation
Pydantic	Structured output
RAGAS	RAG evaluation
Git & GitHub	Version control
Render	Deployment
⚙️ Installation

Clone the repository:

git clone https://github.com/Ajaysakle721/rag_project.git

Go to the project directory:

cd rag_project

Create a virtual environment:

python -m venv venv-rag

Activate the environment on Windows:

venv-rag\Scripts\activate

Install dependencies:

pip install -r requirement.txt
🔑 Environment Variables

Create a .env file in the project root.

OPENAI_API_KEY=your_openai_api_key

CHAT_MODEL=gpt-4o-mini

DATA_DIR=data/raw

CHROMA_PERSIST_DIR=vectorstore/chroma_db

CHUNK_SIZE=1000

CHUNK_OVERLAP=150

Never upload your real API key to GitHub.

📥 Run Document Ingestion

Before running the backend, create the vector database:

python -m ingestion.run_ingestion

This process:

Documents
   ↓
Loading
   ↓
Chunking
   ↓
Embedding
   ↓
ChromaDB
⚡ Run Backend

Start the FastAPI server:

uvicorn backend.main:app --reload

Backend will run at:

http://127.0.0.1:8000

API documentation:

http://127.0.0.1:8000/docs
🖥️ Run Frontend

Open another terminal and activate the virtual environment.

Then run:

streamlit run frontend/app.py

The Streamlit application will open in your browser.

🔌 API
Health Check
GET /

Response:

{
  "status": "ok"
}
Ask Question
POST /ask

Example:

{
  "question": "What is Retrieval Augmented Generation?"
}
☁️ Deployment

The application can be deployed using Render.

Backend
FastAPI
    ↓
Render Web Service

Start command:

uvicorn backend.main:app --host 0.0.0.0 --port $PORT
Frontend
Streamlit
    ↓
Render Web Service

The Streamlit frontend communicates with the deployed FastAPI backend.

📊 Evaluation

The project includes an evaluation module using RAGAS.

Evaluation data is maintained in:

evaluation/testset.json

Evaluation script:

evaluation/evaluate.py
🎯 Project Objective

The main objective of this project is to build a modular RAG system that can:

Understand user queries
Route queries appropriately
Retrieve relevant document information
Generate context-aware answers
Provide a simple chat interface
Evaluate RAG performance
👨‍💻 Author

Ajay Sakle

GitHub: Ajaysakle721

⭐ Future Improvements
Support multiple document formats
Improve retrieval accuracy
Add conversation memory
Add authentication
Add advanced RAG evaluation
Deploy using scalable vector databases
Improve UI/UX

### Abhi kya karna hai

**Sirf content paste karo.**  
Uske baad neeche **“Commit changes…”** button par click karna hai.

⚠️ **Commit button abhi mat dabana** — pehle screenshot bhejo ki README paste ho gaya hai.
