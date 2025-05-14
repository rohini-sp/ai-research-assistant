# 🧠 AI Research Assistant with RAG Pipeline

This project is an AI-powered research assistant that processes academic PDFs and answers natural language queries using a Retrieval-Augmented Generation (RAG) pipeline. It leverages FAISS for semantic search and BART for summarization, enabling fast, contextual answers from technical documents.

---

## 🔍 Features

-  **PDF Ingestion**: Parses and chunks academic papers into semantically meaningful segments.
-  **Semantic Search**: Uses sentence embeddings and FAISS to retrieve the most relevant sections based on user queries.
-  **Contextual Summarization**: Generates concise answers using the `facebook/bart-large-cnn` model.
-  **Multi-document Support**: Retrieves and summarizes content across multiple PDFs.
-  **Modular Design**: Easily extendable to support evaluation (RAGAS), translation, or other LLMs.

---

## 💻 Tech Stack

| Component           | Purpose                                   |
|---------------------|-------------------------------------------|
| FAISS               | Vector similarity search                  |
| sentence-transformers | Embedding model (`all-MiniLM-L6-v2`)    |
| transformers        | Summarization model (`bart-large-cnn`)    |
| PyMuPDF             | PDF text extraction                       |

---

## 🚀 How It Works

1. **Upload PDFs**  
   Extracts and chunks text from academic documents.

2. **Ask a Question**  
   Accepts a natural language query from the user.

3. **Retrieve Relevant Chunks**  
   Uses FAISS to identify top-k relevant sections.

4. **Generate Summary Answer**  
   Concatenates retrieved context and summarizes using BART.

---

## 📈 Planned Extensions

-  Integrate RAGAS for automated answer evaluation.
-  Improve chunking and ranking heuristics.
-  Enable multilingual question answering.

---

## 🛠️  Setup

```bash
pip install faiss-cpu transformers sentence-transformers datasets pymupdf

