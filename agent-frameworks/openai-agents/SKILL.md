# OpenAI Agents SDK Skill

## Trigger
User wants: "use OpenAI's agent framework", "handoffs between agents", "OpenAI tracing", or when building agent workflows with OpenAI models.

## Key Concepts
- **Agents**: Have instructions, tools, and handoff targets
- **Handoffs**: Agent passes control to another agent
- **Run()**: Executes the agent with input
- **Tracing**: Built-in observability via OpenAI's tracing

## Pattern
```python
from agents import Agent, Runner

agent = Agent(instructions="You are a helpful assistant.")
result = Runner.run(agent, "Hello")
print(result.final_output)
```

## For multi-agent with handoffs:
```python
from agents import Agent, Runner, handoff

escalation_agent = Agent(
    name="escalation",
    instructions="Handle escalations..."
)

triage = Agent(
    name="triage",
    instructions="Route requests...",
    handoffs=[escalation_agent]
)

result = Runner.run(triage, user_input)
```

## What this adds to Hermes
- Clean agent spawning for complex tasks
- Built-in tool calling with model support
- Structured handoff chains
- Run via delegate_task with openai-agents Python

## Usage
Use via: delegate_task with acp_command='openai' or direct Python Runner
