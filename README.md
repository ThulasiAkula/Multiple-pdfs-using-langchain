# Multiple-pdfs-using-langchain
📚 Conversational PDF Assistant with LangChain + Google Gemini Pro
Have you ever wanted to chat with your PDFs instead of reading through pages of content? This project is your answer.

The Conversational PDF Assistant lets users upload multiple PDFs and then simply ask questions in natural language. It understands the document's content, finds the right answers, and responds like ChatGPT—but specifically focused on your documents.

🎯 Objective
To build an intelligent chatbot-like tool that allows users to:

Upload one or more PDF documents.

Ask questions based on the document content.

Get accurate, context-aware answers from the uploaded documents using LLMs.

🧠 How It Works – Step by Step
1. 📄 PDF Text Extraction
Tool Used: PyPDF2

Each uploaded PDF is processed, and raw text is extracted.

This text forms the knowledge base for answering questions.

2. 🔍 Embedding and Vector Storage
Tools Used: FAISS (Facebook AI Similarity Search) and ChromaDB

The text is split into manageable chunks and converted into embeddings (numerical vectors that capture semantic meaning).

These embeddings are indexed for fast similarity search, so the system can later retrieve relevant content efficiently when a user asks a question.

3. 🤖 Connecting the LLM (Google Gemini Pro)
Frameworks Used: LangChain, langchain_google_genai

The assistant uses Google Gemini Pro via LangChain to:

Receive user queries

Find relevant chunks from stored embeddings

Answer based on those chunks

The model does contextual Q&A using a technique known as Retrieval-Augmented Generation (RAG).

4. 🖥️ Front-End and Deployment
UI Library: Streamlit

Simple and intuitive interface to:

Upload multiple PDFs

View document upload status

Ask questions in plain English

Environment Management: python-dotenv securely manages API keys and credentials.

✅ Final Outcome
You get a working Conversational PDF Assistant that allows users to:

Upload documents

Ask questions in natural language

Get fast and context-aware answers—no need to search manually or scan pages

Perfect for use-cases like:

Students studying large reports

Professionals reviewing legal documents

Researchers interacting with technical papers

