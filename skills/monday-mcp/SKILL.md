---
name: monday-mcp
description: Monday.com board management with items and team planning
---

# monday-mcp

Monday.com board management with items and team planning

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-monday
```

### Step 2: Get API Credentials

Get your credentials from: https://monday.com/developers/apps

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "monday": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-monday"],
      "env": {
            "MONDAY_API_TOKEN": "your-api-token"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available monday commands"
```

---

## Environment Variables

- `MONDAY_API_TOKEN`: Required - Your api-token

## Available Tools

- `list_boards`
- `list_items`
- `create_item`
- `update_item`

## Quick Start Examples

### Example 1
```
User: "Help me with monday"
```

## Documentation

See @anthropic/mcp-monday documentation for more details.

## Source

GitHub: https://github.com/monday/mcp-server

## Author

Monday.com

## Version

1.0.0
