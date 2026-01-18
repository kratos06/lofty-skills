---
name: discord-mcp
description: Discord bot and messaging integration
---

# discord-mcp

Discord bot and messaging integration

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "discord-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-discord"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add discord-mcp
```

## Quick Start

After configuration, the discord-mcp tools will be available in Claude Code.

## Features

- discord
- bot
- messaging





## Author

discord

## Version

1.0.0
