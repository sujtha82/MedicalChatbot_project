Hybrid Medical Claims RAG Project
This project is a Retrieval-Augmented Generation (RAG)-based system designed to process and answer questions from medical claims documents using LangChain, ChromaDB, and Sentence Transformers.
It combines document chunking, semantic embeddings, and a conversational interface powered by Gradio. This project follows industry best practices for AI system design, including modular architecture, environment isolation, reproducibility, and observability-ready components.

Overview Large Language Models (LLMs) are prone to hallucinations, especially in sensitive domains like healthcare. This project mitigates that risk by implementing Retrieval-Augmented Generation (RAG), where responses are grounded in a curated medical claims knowledge base. The system retrieves relevant documents using vector similarity search and injects them into the LLM prompt to generate context-aware, evidence-backed answers.

Features
PDF and text document ingestion (via PyMuPDF)
Intelligent text chunking using RecursiveCharacterTextSplitter and TokenTextSplitter
Embedding generation using sentence-transformers
Vector storage using ChromaDB or FAISS
Query answering pipeline using LangChain retrievers
Interactive Gradio-based web UI
Support for BM25 ranking and hybrid retrieval
Architecture Client / UI | | HTTP API | Backend (Python API Layer) | | RAG Orchestration | Retriever → Vector Database | | Medical Claims Knowledge Base

Key Features
Retrieval-Augmented Generation (RAG) Semantic search over medical claims data Context-grounded LLM responses Modular and extensible backend design Environment-based configuration Ready for monitoring and scaling

Installation git clone https://github.com/sujtha82/MedicalChatbot_project.git cd GenAI_RAG_medicalClaims_project python -m venv venv source venv/bin/activate # macOS/Linux venv\Scripts\activate # Windows

pip install -r requirements.txt

Running the Application python app/api.py The API will be available at: http://localhost:8000

Configuration Environment variables are managed via .env: OPENAI_API_KEY=your_api_key VECTOR_DB_TYPE=pymilvus EMBEDDING_MODEL=sentence-transformers/all-MiniLM-L6-v2

This project is for my own educational purposes.
