---
name: clickup-mcp
description: ClickUp project and task management
---

# clickup-mcp

ClickUp project and task management

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-clickup
```

### Step 2: Get API Credentials

Get your credentials from: https://app.clickup.com/settings/apps

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "clickup": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-clickup"],
      "env": {
            "CLICKUP_API_TOKEN": "pk_your-token"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available clickup commands"
```

---

## Environment Variables

- `CLICKUP_API_TOKEN`: Required - pk_Your token

## Available Tools

- `list_spaces`
- `list_tasks`
- `create_task`
- `update_task`

## Quick Start Examples

### Example 1
```
User: "Help me with clickup"
```

## Documentation

See @anthropic/mcp-clickup documentation for more details.



## Author

clickup

## Version

1.0.0
