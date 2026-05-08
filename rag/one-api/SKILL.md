---
name: one-api
description: LLM API gateway — unified API for 200+ model providers
triggers:
  - "unified API"
  - "manage API keys"
  - "multi-provider gateway"
---

# OneAPI — LLM API Gateway

## What It Does
Single API endpoint for all LLM providers:
- OpenAI, Claude, Gemini, DeepSeek, Groq, etc.
- Manage keys, load balance, track usage

## How to Deploy
```bash
docker run -d -p 3000:3000 --name one-api \
  -v /root/one-api/data:/data \
  justsong/one-api
```

## Usage
1. Add API keys for each provider
2. Use the unified API endpoint
3. All requests route to the right provider

## Resources
Local: /root/.hermes/repo_watcher/one-api/