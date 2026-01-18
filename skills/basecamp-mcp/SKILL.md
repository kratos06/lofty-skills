---
name: basecamp-mcp
description: Basecamp project collaboration with to-dos and message boards
---

# basecamp-mcp

Basecamp project collaboration with to-dos and message boards

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-basecamp
```

### Step 2: Get API Credentials

Get your credentials from: https://launchpad.37signals.com/integrations

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "basecamp": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-basecamp"],
      "env": {
            "BASECAMP_ACCESS_TOKEN": "your-access-token",
            "BASECAMP_ACCOUNT_ID": "your-account-id"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available basecamp commands"
```

---

## Environment Variables

- `BASECAMP_ACCESS_TOKEN`: Required - Your access-token
- `BASECAMP_ACCOUNT_ID`: Required - Your account-id

## Available Tools

- `list_projects`
- `list_todos`
- `create_todo`
- `list_messages`

## Quick Start Examples

### Example 1
```
User: "Help me with basecamp"
```

## Documentation

See @anthropic/mcp-basecamp documentation for more details.

## Source

GitHub: https://github.com/basecamp/mcp-server

## Author

Basecamp

## Version

1.0.0
