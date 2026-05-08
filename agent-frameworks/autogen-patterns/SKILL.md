# Microsoft AutoGen Patterns Skill

## Trigger
User wants: "AutoGen", "Microsoft agent framework", "conversational agents", "human-in-the-loop", or coding automation.

## Core Patterns

### Pattern 1: Two-Agent Chat
```python
import autogen

math_agent = autogen.AssistantAgent("MathAgent", llm_config=...)
user_proxy = autogen.UserProxyAgent("user", human_input_mode="NEVER")

user_proxy.initiate_chat(math_agent, message="Solve 2+2")
```

### Pattern 2: Group Chat (3+ agents)
```python
from autogen.agentchat.groupchat import GroupChat
from autogen.agentchat import GroupChatManager

group = GroupChat(agents=[math_agent, coder_agent, reviewer_agent], messages=[], max_round=5)
manager = GroupChatManager(groupchat=group, llm_config=llm_config)
```

### Pattern 3: Human-in-the-Loop
```python
user_proxy = autogen.UserProxyAgent("user", human_input_mode="TERMINATE")
# Agent stops and asks human when needed
```

## Best for
- Coding agents that execute code
- Multi-agent code review
- Interactive problem-solving with human approval

## Hermes Integration
AutoGen is installed at /root/.hermes-bridge/venv/
Use via delegate_task or execute_code Python
