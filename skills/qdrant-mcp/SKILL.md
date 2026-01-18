---
name: qdrant-mcp
description: Qdrant vector database for semantic search and AI memory
---

# qdrant-mcp

Qdrant vector database for semantic search and AI memory

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "qdrant-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-qdrant"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add qdrant-mcp
```

## Quick Start

After configuration, the qdrant-mcp tools will be available in Claude Code.

## Features

- qdrant
- vector
- embeddings
- ai



## Source

GitHub: https://github.com/qdrant/mcp-server-qdrant

## Author

Qdrant

## Version

1.0.0
