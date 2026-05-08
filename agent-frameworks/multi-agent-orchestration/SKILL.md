# Multi-Agent Orchestration Skill

## Trigger
User wants to: "run multiple agents", "delegate to agents", "spin up a team", "parallel research", or any task that benefits from splitting work across specialized agents.

## Core Concept
Instead of one agent doing everything, create a TEAM of specialized agents:
- Each agent has a specific ROLE
- Agents hand off work to each other
- Orchestrator coordinates the workflow

## Pattern (CrewAI-style)
```python
from crewai import Agent, Task, Crew

researcher = Agent(role="Researcher", goal="Find X", backstory="...")
coder = Agent(role="Coder", goal="Build X", backstory="...")
reviewer = Agent(role="Reviewer", goal="Review X", backstory="...")

crew = Crew(agents=[researcher, coder, reviewer], tasks=[...])
crew.kickoff()
```

## When to use
| Task type | Best pattern |
|---|---|
| Research + Report | 2-agent: researcher → writer |
| Build + Review | 3-agent: planner → coder → reviewer |
| Compare options | Parallel agents each analyze one option |
| Complex automation | 4+ agents with specific roles |

## Delegation steps
1. Break the task into distinct roles
2. Create each agent with a clear goal
3. Define handoffs between agents
4. Kickoff and monitor progress
5. Collect final output from orchestrator

## Pitfalls
- Don't over-engineer: 2-3 agents is usually enough
- Give each agent ONE clear goal — not a list
- Define output schema so agents can pass structured data
