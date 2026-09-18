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
<img width="1312" height="1199" alt="ChatGPT Image Sep 18, 2026, 08_02_36 PM" src="https://github.com/user-attachments/assets/64667ffa-95ee-4326-88b2-052804e0755b" />
| Layer                   | Technology                            |
| ----------------------- | ------------------------------------- |
| 🐍 Programming Language | Python                                |
| 🔗 RAG Framework        | LangChain                             |
| 🧠 Embeddings           | Hugging Face — BAAI/bge-large-en-v1.5 |
| 🗄️ Vector Database     | ChromaDB                              |
| 🤖 LLM                  | OpenAI GPT-4o-mini                    |
| ⚡ Backend               | FastAPI                               |
| 🖥️ Frontend            | Streamlit                             |
| 📦 Data Validation      | Pydantic                              |
| 📊 Evaluation           | RAGAS                                 |
| 🌐 Version Control      | Git & GitHub                          |
| ☁️ Deployment           | Render                                |



