---
name: vercel-mcp
description: Vercel deployment and project management
---

# vercel-mcp

Vercel deployment and project management

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-vercel
```

### Step 2: Get API Credentials

Get your credentials from: https://vercel.com/account/tokens

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "vercel": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-vercel"],
      "env": {
            "VERCEL_TOKEN": "your-token"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available vercel commands"
```

---

## Environment Variables

- `VERCEL_TOKEN`: Required - Your token

## Available Tools

- `list_projects`
- `list_deployments`
- `create_deployment`
- `get_logs`

## Quick Start Examples

### Example 1
```
User: "Help me with vercel"
```

## Documentation

See @anthropic/mcp-vercel documentation for more details.

## Source

GitHub: https://github.com/vercel/mcp-server

## Author

Vercel

## Version

1.0.0
