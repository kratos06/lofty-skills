---
name: pinecone-mcp
description: Pinecone vector database
---

# pinecone-mcp

Pinecone vector database

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "pinecone-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-pinecone"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add pinecone-mcp
```

## Quick Start

After configuration, the pinecone-mcp tools will be available in Claude Code.

## Features

- pinecone
- vector
- embeddings





## Author

pinecone

## Version

1.0.0
