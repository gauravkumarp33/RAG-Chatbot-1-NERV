📘 Drona AI — RAG Chatbot for Alumni Portal

Drona AI is a Retrieval-Augmented Generation (RAG) chatbot built using FastAPI, Gemini-2.5-Flash, and ChromaDB for storing vector embeddings.
It is designed specifically for a college alumni portal, where students can ask:
 * Doubts related to their alumni network
 * Queries about alumni profiles, companies, guidance, or career paths
 * Questions related to competitive exam preparation
 * Any information sourced from the provided PDF dataset
The chatbot generates accurate, context-aware responses based entirely on the PDF data that has been uploaded and indexed.

✨ Key Features
🔍 Retrieval-Augmented Generation (RAG)

 * Answers are generated from real alumni data
 * Reduces hallucinations and ensures fact-based responses
 * Perfect for academic or career-related queries

🤖 Powered by Gemini-2.5-Flash
 * Fast, efficient, and optimized for real-time chat use
 * High-quality answers based on retrieved document context

🗂 ChromaDB for Vector Storage
 * Stores embeddings of alumni data extracted from PDFs
 * Enables millisecond-speed semantic search
 * Fully cloud-based and scalable

⚡ FastAPI Backend
 * Lightweight and production-ready REST API
 * Simple endpoints for chat and document ingestion
 * CORS-enabled for frontend integration

🎓 Designed for College Alumni Systems
 * Helps students connect with alumni information
 * Assists in career guidance, placement queries, and preparation
 * Uses provided college data to ensure relevant answers

📁 Tech Stack
 * FastAPI — API Framework
 * Gemini-2.5-Flash — LLM for response generation
 * ChromaDB — Vector database
 * Sentence Transformers — Embedding generation
 * Python — Core backend

📚 How It Works

1. Admin uploads a PDF containing alumni data
2. PDF is converted into chunks and embeddings via Sentence Transformers
3. Embeddings are stored in ChromaDB (cloud)
4. Student asks a question → embedding created
5. Chroma retrieves the most relevant alumni information
6. Gemini-2.5-Flash generates a final answer using retrieved data

🔧 Installation

Clone the repository:
  git clone https://github.com/gauravkumarp33/RAG-Chatbot-1-NERV.git
  cd RAG-Chatbot-1-NERV

Install dependencies:
  pip install -r requirements.txt

Run the app:
  uvicorn main:app --host 0.0.0.0 --port 8000

📡 API Endpoint
POST /ask

Request:
    {
    "query": "Give me details about alumni working at Google"
    }

