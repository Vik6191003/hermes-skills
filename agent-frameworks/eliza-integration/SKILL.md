# ElizaOS (Eliza) Integration Skill

## Trigger
User wants: "Eliza", "Discord bot", "Telegram agent", "character AI", or wants to run a persistent agent on messaging platforms.

## What ElizaOS Is
Open-source autonomous agent framework — like OpenClaw but with built-in platform integrations for Discord, Telegram, Twitter, Slack.

## Key Features
- Character/config-based agents
- Multi-platform deployment
- Memory and long-term context
- Plugin system
- Voice and image support

## Repo
https://github.com/elizaOS/eliza
Clone: /root/.hermes/repo_watcher/eliza-clone/

## How Hermes Could Use It
Eliza could run as a SECONDARY agent on your Telegram — handles character-based interactions while Hermes handles automation/research.

## For Alexander's Use Case
Could create a "Gaming Assistant" character on Telegram that:
- Responds in a specific voice/personality
- Handles casual game questions
- Hands off complex tasks to Hermes

## Setup (if needed later)
node.js 18+ required
git clone https://github.com/elizaOS/eliza
npm install
node --experimental-specifier-resolution=node packages/core/dist/node/index.js
