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
