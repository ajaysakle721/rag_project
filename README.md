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

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| 🐍 Python | Core programming language |
| 🔗 LangChain | RAG orchestration and prompt management |
| ⚡ FastAPI | Backend REST API |
| 🖥️ Streamlit | Frontend chat interface |
| 🗄️ ChromaDB | Vector database for document embeddings |
| 🤗 Hugging Face | Text embedding model |
| 🤖 OpenAI | LLM-based answer generation |
| 📦 Pydantic | Data validation and structured output |
| 📊 RAGAS | RAG evaluation |
| 🌐 Git & GitHub | Version control and source management |
| ☁️ Render | Cloud deployment |

 📁 Project Structure
rag-project/
├── data/raw/                 # source documents
├── ingestion/                 # load -> split -> embed -> persist (offline, run once)
├── retrieval/                 # wraps the persisted vector store as a retriever
├── routing/                   # classifies queries: general vs document
├── generation/                 # prompts, LLM config, structured output parser
├── backend/                   # FastAPI — POST /ask, wires everything together
├── frontend/                  # Streamlit chat UI (HTTP calls only, no LangChain)
├── evaluation/                 # RAGAS test set + scoring script
├── scripts/scaffold_project.py
├── setup.ps1                  # one-command Windows environment setup
├── requirements.txt
└── .env.example
