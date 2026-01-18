---
name: telegram-mcp
description: Telegram Bot API integration
---

# telegram-mcp

Telegram Bot API integration

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "telegram-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-telegram"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add telegram-mcp
```

## Quick Start

After configuration, the telegram-mcp tools will be available in Claude Code.

## Features

- telegram
- bot
- messaging





## Author

telegram

## Version

1.0.0
