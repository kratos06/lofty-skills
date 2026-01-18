---
name: replicate-mcp
description: Replicate AI model hosting
---

# replicate-mcp

Replicate AI model hosting

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "replicate-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-replicate"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add replicate-mcp
```

## Quick Start

After configuration, the replicate-mcp tools will be available in Claude Code.

## Features

- replicate
- models
- ai





## Author

replicate

## Version

1.0.0
