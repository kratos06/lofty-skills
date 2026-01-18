---
name: linear-mcp
description: Linear issue tracking with cycles, projects, and high-velocity workflows
---

# linear-mcp

Linear issue tracking with cycles, projects, and high-velocity workflows

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-linear
```

### Step 2: Get API Credentials

Get your credentials from: https://linear.app/settings/api

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "linear": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-linear"],
      "env": {
            "LINEAR_API_KEY": "lin_api_your-key"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available linear commands"
```

---

## Environment Variables

- `LINEAR_API_KEY`: Required - lin_api_Your key

## Available Tools

- `search_issues`
- `create_issue`
- `update_issue`
- `list_projects`

## Quick Start Examples

### Example 1
```
User: "Help me with linear"
```

## Documentation

See @modelcontextprotocol/server-linear documentation for more details.

## Source

GitHub: https://github.com/linear/mcp-server

## Author

Linear

## Version

1.0.0
