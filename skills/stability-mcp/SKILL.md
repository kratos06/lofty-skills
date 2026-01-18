---
name: stability-mcp
description: Stability AI image generation
---

# stability-mcp

Stability AI image generation

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "stability-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-stability"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add stability-mcp
```

## Quick Start

After configuration, the stability-mcp tools will be available in Claude Code.

## Features

- stability
- images
- generation





## Author

stability

## Version

1.0.0
