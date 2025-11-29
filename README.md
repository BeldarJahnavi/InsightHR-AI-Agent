#  InsightHR — AI-Powered Knowledge Base Agent  
### Retrieval-Augmented Generation (RAG) HR Assistant  
Developed by **Beldar Jahnavi**

InsightHR is an AI-powered Knowledge Base Agent that answers HR-related questions using internal documents such as HR Policies, SOPs, and FAQs.  
It is built using a fully open-source RAG pipeline including SentenceTransformer embeddings, FAISS vector search, and the Phi-2 local language model.  
This system runs completely offline inside Google Colab—no API keys required.

---

##  Table of Contents
- Overview  
- Features  
- Architecture  
- Tech Stack  
- How It Works  
- How to Run  
- Folder Structure  
- Example Queries  
- Future Improvements  
- Author  

---

##  Overview

Employees often struggle to quickly find accurate HR information from documents like policies, SOPs, and FAQs.  
**InsightHR** solves this by enabling natural-language querying over internal documents, retrieving relevant chunks, and generating accurate answers.

This agent is highly efficient, free, and uses entirely open-source tools.

---

##  Features

✔ 100% free – no API keys needed  
✔ Accurate HR policy question answering  
✔ Transparent source citation  
✔ Fast semantic search with FAISS  
✔ Local LLM (Phi-2) for answer generation  
✔ Modular and extendable RAG pipeline  
✔ Simple to run in Google Colab  

---

##  Architecture

![Architecture Diagram](InsightHR_Architecture.png)

The system consists of three major layers:

### 🔹 1. User Layer  
- User / Employee  
- Google Colab Input Interface

### 🔹 2. RAG Logic Layer  
- Query Handler  
- Retriever (FAISS Top-k Search)  
- Context Builder  
- Local LLM (Phi-2)

### 🔹 3. Knowledge Base Layer  
- HR Policy Document  
- SOP Document  
- FAQ Document  
- Document Chunker  
- Embedding Model (MiniLM)  
- FAISS Vector Store  

---

##  Tech Stack

| Component | Technology |
|----------|-----------|
| Language | Python |
| Environment | Google Colab |
| Embeddings | SentenceTransformer MiniLM |
| Vector DB | FAISS |
| LLM | Phi-2 (HuggingFace Transformers) |
| Libraries | transformers, sentence-transformers, faiss-cpu |

---

##  How InsightHR Works

1. Load HR/SOP/FAQ documents  
2. Chunk documents into 300–350 character segments  
3. Convert chunks into embeddings using MiniLM  
4. Store embeddings in FAISS for fast search  
5. When user asks a question:  
   - Query is embedded  
   - FAISS returns top-k similar chunks  
6. Retrieved chunks are merged into a context  
7. Phi-2 LLM generates a final answer  
8. Sources are displayed for transparency  

---

##  How to Run (Google Colab)

1. Open **main.ipynb**  
2. Click **Runtime → Run all**  
3. Wait for all modules and models to load  
4. Type your question in the input prompt  
5. The system will return the answer + source chunks  

### Example query:

---

##  Example Queries

- “What is the annual leave policy?”  
- “How do I request a laptop?”  
- “What are the onboarding steps?”  
- “Where can I check my leave balance?”  

---

##  Future Improvements

- Add a GUI (Streamlit or Gradio)  
- Support PDF/Docx ingestion  
- Use larger LLMs like LLaMA-3 or Gemma-2  
- Deploy as a web API or chatbot  
- Add role-based access control  

---

##  Author

**Beldar Jahnavi**  
AI Agent Development Challenge Participant  
2025  

---

##  Acknowledgment
This project uses free and open-source technologies including  
Phi-2, SentenceTransformers, FAISS, and Google Colab.


