---
name: discord-mcp
description: Discord bot and messaging integration
---

# discord-mcp

Discord bot and messaging integration

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-discord
```

### Step 2: Get API Credentials

Get your credentials from: https://discord.com/developers/applications

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "discord": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-discord"],
      "env": {
            "DISCORD_BOT_TOKEN": "your-bot-token"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available discord commands"
```

---

## Environment Variables

- `DISCORD_BOT_TOKEN`: Required - Your bot-token

## Available Tools

- `send_message`
- `list_channels`
- `get_messages`
- `create_channel`

## Quick Start Examples

### Example 1
```
User: "Help me with discord"
```

## Documentation

See @anthropic/mcp-discord documentation for more details.



## Author

discord

## Version

1.0.0
