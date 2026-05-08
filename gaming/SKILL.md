# Xbox Gaming Automation Skill

## Trigger
User says: "automate my xbox", "grind", "play game", or any gaming task

## Prerequisites
- Laptop bridge running (`start_bridge.bat`)
- Xbox on same WiFi as laptop
- VPS relay server active on port 19999

## Steps
1. Verify laptop bridge is connected (check VPS relay logs)
2. Identify the game and target action (grinding XP, farming resources, etc.)
3. Build a command plan using SmartGlass button commands
4. Execute plan via the web app or direct VPS relay
5. Monitor execution, report progress
6. If Xbox disconnects: retry discovery and reconnect

## SmartGlass Commands
- Buttons: `a`, `b`, `x`, `y`, `menu`, `home`, `ls`, `rs`
- D-pad: `navigate:up`, `navigate:down`, `navigate:left`, `navigate:right`
- Power: `power:on`, `power:off`
- Wait: `wait:3` (pause 3 seconds between commands)

## Example Plan
```json
[
  {"command": "button:a"},
  {"command": "wait:2"},
  {"command": "navigate:right"},
  {"command": "button:a"}
]
```

## Pitfalls
- Xbox must be on SAME WiFi as laptop bridge
- If Xbox goes to dashboard, plan may need to restart
- Some games block SmartGlass input — test first
