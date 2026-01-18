---
name: intercom-mcp
description: Intercom customer conversations and messaging platform
---

# intercom-mcp

Intercom customer conversations and messaging platform

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "intercom-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-intercom"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add intercom-mcp
```

## Quick Start

After configuration, the intercom-mcp tools will be available in Claude Code.

## Features

- intercom
- messaging
- customer-support



## Source

GitHub: https://github.com/intercom/mcp-server

## Author

Intercom

## Version

1.0.0
