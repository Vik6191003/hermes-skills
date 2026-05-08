# LangGraph Workflows Skill

## Trigger
User says: "LangGraph", "agentic workflows", "loops in agents", "retry logic", "complex flows", or when a simple linear pipeline isn't enough.

## What It Adds
LangGraph = LangChain + directed graphs. Agents can:
- **LOOP**: retry until success
- **BRANCH**: different paths based on output
- **STATE**: maintain memory across steps
- **CONDITIONS**: if X then path A else path B

## Core Pattern
```python
from langgraph.graph import StateGraph, END

workflow = StateGraph(...)
workflow.add_node("research", research_agent)
workflow.add_node("write", write_agent)
workflow.add_edge("research", "write")
workflow.add_edge("write", END)

app = workflow.compile()
```

## Example: Self-Healing Agent
```
START → research → write → success?
                                      ↓
                              YES → END
                               ↓ NO
                           retry → write
```

## Best for Hermes
- Automation pipelines that need retry logic
- Complex multi-step game grinding with checkpoints
- Any workflow where the outcome determines the next step
- Long-running tasks with error recovery

## Repo
https://github.com/langchain-ai/langgraph
Clone: /root/.hermes/repo_watcher/langgraph-clone/
