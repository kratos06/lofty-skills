---
name: asana-mcp
description: Asana task management with project tracking and team collaboration
---

# asana-mcp

Asana task management with project tracking and team collaboration

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-asana
```

### Step 2: Get API Credentials

Get your credentials from: https://app.asana.com/0/developer-console

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "asana": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-asana"],
      "env": {
            "ASANA_ACCESS_TOKEN": "your-access-token"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available asana commands"
```

---

## Environment Variables

- `ASANA_ACCESS_TOKEN`: Required - Your access-token

## Available Tools

- `list_workspaces`
- `list_projects`
- `create_task`
- `get_task`

## Quick Start Examples

### Example 1
```
User: "Help me with asana"
```

## Documentation

See @anthropic/mcp-asana documentation for more details.

## Source

GitHub: https://github.com/asana/mcp-server

## Author

Asana

## Version

1.0.0
