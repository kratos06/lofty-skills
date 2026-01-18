---
name: pinecone-mcp
description: Pinecone vector database
---

# pinecone-mcp

Pinecone vector database

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-pinecone
```

### Step 2: Get API Credentials

Get your credentials from: https://app.pinecone.io/

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "pinecone": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-pinecone"],
      "env": {
            "PINECONE_API_KEY": "your-api-key",
            "PINECONE_ENVIRONMENT": "your-environment"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available pinecone commands"
```

---

## Environment Variables

- `PINECONE_API_KEY`: Required - Your api-key
- `PINECONE_ENVIRONMENT`: Required - Your environment

## Available Tools

- `upsert`
- `query`
- `delete`
- `describe_index`

## Quick Start Examples

### Example 1
```
User: "Help me with pinecone"
```

## Documentation

See @anthropic/mcp-pinecone documentation for more details.



## Author

pinecone

## Version

1.0.0
