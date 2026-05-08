---
name: claude-code
description: Spawn Anthropic Claude Code CLI as a coding sub-agent for complex tasks
triggers:
  - "build this"
  - "write code"
  - "implement"
  - "create a file"
  - "write tests"
---

# Claude Code CLI Integration

## Commands
```bash
claude --help                    # Show all commands
claude -p "<prompt>"            # Run single prompt (non-interactive)
claude --print "<prompt>"       # Print only, no follow-up
```

## How I Use It
When you ask me to build/write/debug code, I spawn Claude Code as a sub-agent:

```bash
claude -p "You are working on the Hermes AI Agent system for Alexander Barnes. [TASK]"
```

## Environment Context
Claude Code already has hermes-context.md loaded from ~/.claude/skills/

## Key Flags
- `--no-input`     : Run without prompting for confirmation
- `--dangerously-skip-permissions` : Skip permission prompts
- `--out <file>`   : Write output to file
