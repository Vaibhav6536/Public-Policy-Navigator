# Public Policy Navigation using AI — OCR + Ollama Chat

![App Screenshot](./assets/Screenshot%202025-09-30%20131525.png)


A Streamlit-based AI application that helps users extract, analyze, and understand public policy PDFs using OCR, text chunking, retrieval, and local LLMs powered by Ollama.

---

## 🚀 Overview

**Public Policy Navigation using AI** allows you to:

- Upload PDF files  
- Convert PDF → images → text using **Tesseract OCR**
- Split the extracted text into **overlapping chunks**
- Retrieve best-matching text sections intelligently  
- Ask questions about the document using **Local LLMs via Ollama**

This project is ideal for policy researchers, students, analysts, and citizens who want fast insights from long PDF documents.

---

## 🌟 Features

### 🔍 PDF Upload + OCR
Uses **Tesseract OCR** + **Poppler (pdf2image)** to extract accurate text from scanned pages.

### ✂️ Adaptive Chunking
Text is split into overlapping character chunks:
- Default chunk size: `1200`
- Overlap: `200`

### 🤖 Local LLM Chat with Ollama
- Works with any Ollama model (LLaMA, Mistral, Llama3 etc.)
- Runs fully offline on your machine
- Communicates using Ollama REST API: `http://localhost:11434`

### 🔎 Dual Retrieval Modes
1. **TF-IDF + Cosine Similarity** (using scikit-learn)  
2. **Word-Overlap Scoring** (no external libraries needed)

### 💬 Streamlit Chat UI
- Clean, modern interface  
- Conversation stored in session  
- Retrieved chunks + user query → AI answer  

### 📥 JSON Export
Export complete OCR output and chunks for reuse.

---

## 🛠️ Tech Stack

| Component | Technology |
|----------|------------|
| OCR | Tesseract OCR |
| PDF → Image | Poppler / pdf2image |
| LLM | Ollama (local) |
| UI | Streamlit |
| Retrieval | TF-IDF / Naive word overlap |
| Language | Python 3.10+ |

---

## 🔧 Installation Guide (Windows)

### 1️⃣ Clone Repository
```bash
git clone https://github.com/Vaibhav6536/Public-Policy-Navigator
cd Public-Policy-Navigator
