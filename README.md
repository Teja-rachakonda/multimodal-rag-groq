# 🧠 Multimodal RAG App using GROQ + LangSmith

A powerful Retrieval-Augmented Generation (RAG) application that accepts **PDF files containing text, tables, and images** — then intelligently extracts, embeds, and answers user queries using **GROQ’s blazing-fast LLaMA3** and Hugging Face models. Includes full **LangSmith observability** support.

---

## 🚀 Features

- 📄 Upload PDFs with **text, tables, and images**
- 🧠 **RAG** pipeline for smart contextual answers
- 🖼️ Image captioning using **BLIP (Hugging Face)**
- 🔍 Embeddings using **SentenceTransformers (MPNet)**
- ⚡️ Queries answered using **GROQ LLaMA3 (Free API)**
- 🧰 Vector store: **ChromaDB**
- 📊 Full observability via **LangSmith (without LangChain)**
- 🧼 Clean project structure and modular design
- 🖥️ **Streamlit UI** — intuitive and interactive

---

## 🧩 Architecture

```text
PDF (Text + Tables + Images)
     |
     v
+-------------------------+
| Extract using pdfplumber|
+-------------------------+
     |        |         |
     v        v         v
   Text     Tables    Images
     |        |         |
     |        |         v
     |        |      Caption via BLIP
     |        |         |
     \________|_________/
              |
          Embedding (MPNet)
              |
          ChromaDB Vector Store
              |
         RAG + GROQ LLaMA3
              |
        Final Answer Output
