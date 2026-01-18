---
name: telegram-mcp
description: Telegram Bot API integration
---

# telegram-mcp

Telegram Bot API integration

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-telegram
```

### Step 2: Get API Credentials

Get your credentials from: https://t.me/BotFather

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "telegram": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-telegram"],
      "env": {
            "TELEGRAM_BOT_TOKEN": "your-bot-token"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available telegram commands"
```

---

## Environment Variables

- `TELEGRAM_BOT_TOKEN`: Required - Your bot-token

## Available Tools

- `send_message`
- `get_updates`
- `send_photo`
- `send_document`

## Quick Start Examples

### Example 1
```
User: "Help me with telegram"
```

## Documentation

See @anthropic/mcp-telegram documentation for more details.



## Author

telegram

## Version

1.0.0
