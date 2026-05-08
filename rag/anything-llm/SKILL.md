---
name: anything-llm
description: All-in-one AI knowledge base platform — documents to answers, fully offline
triggers:
  - "set up knowledge base"
  - "chat with documents"
  - "private AI assistant"
---

# AnythingLLM — All-in-One AI Knowledge Base

## What It Does
One install = full RAG chatbot. Connect any LLM, any vector DB, any documents.
Runs 100% offline. Privacy-first.

## How to Run
```bash
cd /root/.hermes/repo_watcher/anything-llm
docker compose up
```

## Features
- Multi-document ingestion (PDF, DOCX, TXT, Markdown)
- Works with: GPT-4, Claude, Llama, Groq, any LLM
- Vector stores: Qdrant, Milvus, Faiss, PGVector
- Workspace management
- Chat with citations
- API access

## Resources
Local: /root/.hermes/repo_watcher/anything-llm/