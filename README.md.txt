# AI RAG Telegram Chatbot

An AI-powered Telegram chatbot built with **n8n**, **Ollama**, **Qdrant**, and **Llama 3.2**.

The chatbot answers user questions by retrieving relevant information from company documents using Retrieval-Augmented Generation (RAG).

---

## Features

- AI-powered question answering
- Telegram Bot integration
- Local LLM using Ollama (Llama 3.2)
- Vector search with Qdrant
- Conversation memory
- Document ingestion workflow
- Fully self-hosted (no cloud LLM required)

---

## Technologies

- n8n
- Ollama
- Llama 3.2
- Qdrant
- Telegram Bot API

---

## Project Structure

```text
AI-RAG-Telegram-Chatbot
│
├── workflows
│   ├── 01-document-ingestion.json
│   └── 02-telegram-chatbot.json
│
├── documents
│   └── company_policy.pdf
│
├── screenshots
│
└── README.md
```

---

## Workflow Overview

### Workflow 1 – Document Ingestion

This workflow:

- Reads the PDF document
- Splits the document into text chunks
- Generates embeddings
- Stores vectors in Qdrant

### Workflow 2 – Telegram AI Chatbot

This workflow:

- Receives user messages from Telegram
- Searches relevant information in Qdrant
- Uses Ollama (Llama 3.2) to generate answers
- Sends responses back to Telegram
- Maintains conversation memory

---

## Architecture

```text
PDF
   │
   ▼
Document Ingestion
   │
   ▼
Qdrant Vector Database
   ▲
   │
Telegram Trigger
   │
AI Agent
   │
Memory
   │
Ollama (Llama 3.2)
   │
Telegram Bot
```

---

## Screenshots

Screenshots of the workflows and chatbot interaction are available in the `screenshots` folder.