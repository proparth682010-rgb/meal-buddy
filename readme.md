# Chore & Meal Buddy

A simulated Alexa+ experience for the family kitchen, built for the Amazon Developer Hackathon (Alexa+ track, simulated-experience path).

Talk or type to an assistant to manage a shopping list, chores and reminders, and a weekly dinner plan. Each request is turned into an MCP-style tool call (`tools/call` with a tool name and arguments), the same pattern Alexa+ uses to reach an MCP server. The tool calls are shown live on the page.

## Run it
1. Download or clone this repo.
2. Open `index.html` in Chrome, Edge or Safari. No install or build step.
3. Type a request, tap a suggestion, or press **Speak** (voice input needs a browser with speech recognition; replies are spoken aloud).

## Try saying
- "Add milk to my shopping list"
- "Remind me to take out the trash"
- "Dinner on Friday is pasta"
- "What's for dinner?"
- "Suggest dinner"
- "Show my shopping list"
- "Remove milk"
- "I finished take out the trash"
- "Clear my shopping list"

## How it works
- `understand()` matches what you say to a tool and its arguments.
- `tools` holds the tools: `add_item`, `remove_item`, `get_list`, `clear_list`, `set_dinner`, `get_dinner`, `suggest_dinner`.
- Results update the on-screen "fridge door" and are saved in the browser's localStorage.
- Voice uses the browser's built-in Web Speech API.

## Hackathon notes
- Track: Alexa+ (simulated experience). Mini challenge: Open Source (MIT license).
- Everything here was created during the hackathon window.
- Simulation only. Not affiliated with Amazon.

## Next steps
Replace the local tools with a real self-hosted MCP server (Streamable HTTP) so a real Alexa+ agent could call them.