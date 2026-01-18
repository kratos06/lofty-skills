---
name: notion-mcp
description: Notion workspace integration with semantic search and page management
---

# notion-mcp

Notion workspace integration with semantic search and page management

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "notion-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-notion"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add notion-mcp
```

## Quick Start

After configuration, the notion-mcp tools will be available in Claude Code.

## Features

- notion
- workspace
- documents



## Source

GitHub: https://github.com/notion/mcp-server

## Author

Notion

## Version

1.0.0
