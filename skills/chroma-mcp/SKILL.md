---
name: chroma-mcp
description: ChromaDB embeddings database
---

# chroma-mcp

ChromaDB embeddings database

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "chroma-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-chroma"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add chroma-mcp
```

## Quick Start

After configuration, the chroma-mcp tools will be available in Claude Code.

## Features

- chroma
- embeddings
- vector





## Author

chroma

## Version

1.0.0
