# CrewAI Agent Orchestration Skill

## Trigger
User says: "run a crew", "use CrewAI", "create an agent team", or any multi-role automation.

## Core Concept
CREW = Agents + Tasks + Process (sequential or hierarchical)

## Pattern
```python
from crewai import Agent, Task, Crew

researcher = Agent(
    role="Research Analyst",
    goal="Find the best investment opportunities",
    backstory="Expert financial analyst with 10 years experience"
)

task1 = Task(description="Research crypto markets", agent=researcher)
task2 = Task(description="Write summary", agent=writer)

crew = Crew(agents=[researcher, writer], tasks=[task1, task2], process="hierarchical")
result = crew.kickoff()
```

## Process Modes
- **Sequential**: Task 1 → Task 2 → Task 3 (ordered)
- **Hierarchical**: Manager agent delegates to worker agents

## Key Features
- Role-based agents with goals and backstories
- Built-in tools library (crewai-tools)
- Memory across tasks
- Collaborative intelligence

## Hermes Integration
Installed at /root/.hermes-bridge/venv/
Location: /root/.hermes/repo_watcher/crewAI-clone/
Use for complex multi-step automation pipelines
