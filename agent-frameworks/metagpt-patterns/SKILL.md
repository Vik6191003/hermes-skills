# MetaGPT Patterns Skill

## Trigger
User mentions: "MetaGPT", "AI software company", "role-playing agents", or wants software to be built from a spec automatically.

## What It Is
MetaGPT simulates a software company with AI agents playing roles:
- Product Manager (PM): writes SPEC.md
- Architect: designs system architecture
- Project Manager: coordinates
- Engineer: writes code
- Tester: reviews code

## How It Works
Input: User describes what they want
Output: Working code, tests, and documentation

## Key Pattern (Software Generation)
```
User: "Build a CRUD API"
→ PM writes SPEC.md
→ Architect designs schema
→ Engineer writes code
→ Tester writes tests
→ All agents collaborate in a "company"
```

## Best for Hermes
- Complex coding projects where you'd normally hire a dev
- When you have a vague idea and need a working prototype
- Rapid prototyping of web apps, APIs, automations

## Repo
https://github.com/FoundationAgents/MetaGPT
Clone: /root/.hermes/repo_watcher/metagpt-clone/

## Note
MetaGPT is heavy — run via delegate_task when needed, not persistent.

## Limitations
- Uses many tokens per task
- Can be expensive — use sparingly
- Best for: complex greenfield projects
