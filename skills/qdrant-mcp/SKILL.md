---
name: qdrant-mcp
description: Qdrant vector database for semantic search and AI memory
---

# qdrant-mcp

Qdrant vector database for semantic search and AI memory

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-qdrant
```

### Step 2: Get API Credentials

Configure the required credentials below.

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "qdrant": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-qdrant"],
      "env": {
            "QDRANT_URL": "http://localhost:6333",
            "QDRANT_API_KEY": "your-api-key"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available qdrant commands"
```

---

## Environment Variables

- `QDRANT_URL`: http://localhost:6333
- `QDRANT_API_KEY`: Required - Your api-key

## Available Tools

- `upsert`
- `search`
- `delete`
- `get_collection`

## Quick Start Examples

### Example 1
```
User: "Help me with qdrant"
```

## Documentation

See @anthropic/mcp-qdrant documentation for more details.

## Source

GitHub: https://github.com/qdrant/mcp-server-qdrant

## Author

Qdrant

## Version

1.0.0
