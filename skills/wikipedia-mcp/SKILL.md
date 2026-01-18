---
name: wikipedia-mcp
description: Wikipedia knowledge base access
---

# wikipedia-mcp

Wikipedia knowledge base access

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-wikipedia
```

### Step 2: Get API Credentials

Configure the required credentials below.

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "wikipedia": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-wikipedia"],
      "env": {}
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available wikipedia commands"
```

---

## Environment Variables



## Available Tools

- `search`
- `get_page`
- `get_summary`

## Quick Start Examples

### Example 1
```
User: "Help me with wikipedia"
```

## Documentation

See @anthropic/mcp-wikipedia documentation for more details.



## Author

wikipedia

## Version

1.0.0
