---
name: chroma-mcp
description: ChromaDB embeddings database
---

# chroma-mcp

ChromaDB embeddings database

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-chroma
```

### Step 2: Get API Credentials

Configure the required credentials below.

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "chroma": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-chroma"],
      "env": {
            "CHROMA_HOST": "localhost",
            "CHROMA_PORT": "8000"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available chroma commands"
```

---

## Environment Variables

- `CHROMA_HOST`: localhost
- `CHROMA_PORT`: 8000

## Available Tools

- `add`
- `query`
- `delete`
- `get_collection`

## Quick Start Examples

### Example 1
```
User: "Help me with chroma"
```

## Documentation

See @anthropic/mcp-chroma documentation for more details.



## Author

chroma

## Version

1.0.0
