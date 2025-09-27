# -AI-Agent-with-External-Tool-Access
# 📄 PDF Summarization and RAG Q&A with LangChain and Gemini

This project provides a robust solution for loading data from a PDF, segmenting the content, and using the Gemini model to answer questions or generate a summary based *only* on the information contained in the document (Retrieval Augmented Generation - RAG).

---

## ✨ Features

* **PDF Document Loading:** Efficiently loads content from a local PDF file using `PyPDFLoader`.
* **Intelligent Text Splitting:** Uses a Recursive Character Text Splitter to preserve document structure and create optimized chunks for the model.
* **Vectorization & Embedding:** Converts text chunks into numerical vectors using Google's `GoogleGenerativeAIEmbeddings` for semantic search.
* **Vector Store Creation:** Stores and indexes the text vectors using a vector database (e.g., ChromaDB or in-memory) for fast retrieval.
* **RAG Chain:** Implements a complete RAG workflow using LangChain to retrieve relevant document chunks before generating a final answer with the **Gemini 2.5 Flash** model.

---

## ⚙️ How to Run

### 1. Prerequisites

Before running the script, ensure you have:

* **Python 3.10+** installed.
* A **PDF file** that you want to analyze (e.g., `report.pdf`).
* A **Gemini API Key**.

### 2. Setup

#### A. Install Dependencies

Install the necessary Python libraries.

```bash
pip install -U \
  langchain-google-genai \
  langchain-community \
  langchain-core \
  pypdf \
  chromadb
``` 
### 3.Update the script
# summary.py (Example line)
# Ensure you use a raw string (r"...") for Windows paths
pdf_path = r"C:\Users\bhatt\Downloads\report.pdf" # <-- Use your verified, correct path
loader = PyPDFLoader(pdf_path)

### 4. Execute

python summary.py
