---
name: weaviate-mcp
description: Weaviate vector search engine
---

# weaviate-mcp

Weaviate vector search engine

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "weaviate-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-weaviate"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add weaviate-mcp
```

## Quick Start

After configuration, the weaviate-mcp tools will be available in Claude Code.

## Features

- weaviate
- vector
- search





## Author

weaviate

## Version

1.0.0
