---
name: weaviate-mcp
description: Weaviate vector search engine
---

# weaviate-mcp

Weaviate vector search engine

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-weaviate
```

### Step 2: Get API Credentials

Configure the required credentials below.

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "weaviate": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-weaviate"],
      "env": {
            "WEAVIATE_URL": "http://localhost:8080",
            "WEAVIATE_API_KEY": "your-api-key"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available weaviate commands"
```

---

## Environment Variables

- `WEAVIATE_URL`: http://localhost:8080
- `WEAVIATE_API_KEY`: Required - Your api-key

## Available Tools

- `create_object`
- `get_object`
- `search`
- `delete_object`

## Quick Start Examples

### Example 1
```
User: "Help me with weaviate"
```

## Documentation

See @anthropic/mcp-weaviate documentation for more details.



## Author

weaviate

## Version

1.0.0
