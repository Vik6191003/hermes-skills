---
name: mcp-servers
description: Model Context Protocol servers for universal AI tool integration
triggers:
  - "connect to slack"
  - "use github tools"
  - "browse the web"
  - "search the web"
---

# Model Context Protocol (MCP) Integration

## Available MCP Servers
These servers let me connect to external tools through the MCP standard:

| Server | What it connects to |
|---|---|
| `@modelcontextprotocol/server-slack` | Slack workspace |
| `@modelcontextprotocol/server-github` | GitHub repos, issues, PRs |
| `@modelcontextprotocol/server-filesystem` | Local filesystem |
| `@modelcontextprotocol/server-memory` | Persistent memory |
| `@modelcontextprotocol/server-brave-search` | Web search |
| `@modelcontextprotocol/server-puppeteer` | Browser automation |
| `@modelcontextprotocol/server-everything` | All-of-them aggregator |

## How to Start an MCP Server
```bash
# Start a specific server
npx @modelcontextprotocol/server-github

# Or use the installed package
node /root/.npm-global/lib/node_modules/@modelcontextprotocol/server-github/dist/index.js
```

## Available Tools
- GitHub: repos, issues, PRs, files, search
- Slack: channels, messages, files, users
- Search: web search via Brave
- Browser: visit pages, scrape, fill forms
- Memory: persistent key-value store
