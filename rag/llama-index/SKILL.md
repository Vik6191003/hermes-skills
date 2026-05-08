---
name: llama-index
description: RAG framework for document ingestion, retrieval, and question answering
triggers:
  - "build RAG"
  - "ingest documents"
  - "search knowledge base"
  - "answer from documents"
---

# LlamaIndex — RAG Framework

## What It Does
LlamaIndex connects documents to LLMs for accurate, context-grounded answers.

## Installation
```bash
pip install llama-index
```

## Key Capabilities
- Document loading (PDF, CSV, txt, Word, HTML)
- Text chunking and embedding
- Vector storage (Qdrant, Milvus, Faiss, PGVector)
- Retrieval and query engines
- Full RAG pipelines

## Usage
```python
from llama_index import VectorStoreIndex, SimpleDirectoryReader

documents = SimpleDirectoryReader("./data").load_data()
index = VectorStoreIndex.from_documents(documents)
query_engine = index.as_query_engine()
response = query_engine.query("What is this about?")
```

## Resources
Local: /root/.hermes/repo_watcher/llama_index/