---
name: fly-mcp
description: Fly.io edge deployment platform
---

# fly-mcp

Fly.io edge deployment platform

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "fly-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-fly"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add fly-mcp
```

## Quick Start

After configuration, the fly-mcp tools will be available in Claude Code.

## Features

- fly
- edge
- deployment





## Author

fly

## Version

1.0.0
