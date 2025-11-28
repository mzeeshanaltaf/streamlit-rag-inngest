# Ask PDF

A production-grade Retrieval-Augmented Generation (RAG) application that allows users to upload PDFs, ask questions, and get AI-powered answers based on the document content. Built with FastAPI, Streamlit, OpenAI, Inngest and Qdrant vector database.

## 🌟 Features

- 📄 PDF document ingestion and processing
- 🔍 Semantic search using vector embeddings
- 🤖 AI-powered question answering using OpenAI GPT
- 🎯 Production-ready architecture with event-driven design
- 📊 User-friendly Streamlit interface
- 🔄 Asynchronous processing using Inngest
- 📦 Vector storage with Qdrant

## 🏗️ Architecture

The application follows a modern, event-driven architecture:

1. **Frontend (Streamlit)**
   - Handles PDF uploads
   - Provides question-answering interface
   - Displays results with source citations

2. **Backend (FastAPI + Inngest)**
   - Processes PDF ingestion events
   - Manages question-answering workflow
   - Coordinates with vector database

3. **Vector Database (Qdrant)**
   - Stores document embeddings
   - Enables semantic search
   - Manages document chunks

# System Requirements
You must have Python 3.10 or later installed.

# Installation
1. Clone this repository
2. Install `uv`, if not already installed, by running following command from terminal:

   `pip install uv`
3. Create a virtual environment by running:

   `uv init`

4. Install the necessary python packages:

   `uv sync`
5. Run the FastAPI server with following command from terminal:

   `uv run uvicorn main:app`

6. Run the Inngest Dev Server using following command from terminal:

    `npx inngest-cli@latest dev -u http://127.0.0.1:8000/api/inngest`

7. Run Streamlit application using following command from terminal:

    `uv run streamlit run .\streamlit_app.py`