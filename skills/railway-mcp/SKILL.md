---
name: railway-mcp
description: Railway deployment platform
---

# railway-mcp

Railway deployment platform

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "railway-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-railway"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add railway-mcp
```

## Quick Start

After configuration, the railway-mcp tools will be available in Claude Code.

## Features

- railway
- deployment
- hosting





## Author

railway

## Version

1.0.0
