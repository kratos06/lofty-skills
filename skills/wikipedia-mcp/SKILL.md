---
name: wikipedia-mcp
description: Wikipedia knowledge base access
---

# wikipedia-mcp

Wikipedia knowledge base access

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "wikipedia-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-wikipedia"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add wikipedia-mcp
```

## Quick Start

After configuration, the wikipedia-mcp tools will be available in Claude Code.

## Features

- wikipedia
- knowledge
- encyclopedia





## Author

wikipedia

## Version

1.0.0
