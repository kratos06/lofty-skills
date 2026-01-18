---
name: railway-mcp
description: Railway deployment platform
---

# railway-mcp

Railway deployment platform

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-railway
```

### Step 2: Get API Credentials

Get your credentials from: https://railway.app/account/tokens

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "railway": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-railway"],
      "env": {
            "RAILWAY_TOKEN": "your-token"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available railway commands"
```

---

## Environment Variables

- `RAILWAY_TOKEN`: Required - Your token

## Available Tools

- `list_projects`
- `list_services`
- `deploy`
- `get_logs`

## Quick Start Examples

### Example 1
```
User: "Help me with railway"
```

## Documentation

See @anthropic/mcp-railway documentation for more details.



## Author

railway

## Version

1.0.0
