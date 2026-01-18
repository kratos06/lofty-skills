---
name: time-mcp
description: Time and timezone operations
---

# time-mcp

Time and timezone operations

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-time
```

### Step 2: Get API Credentials

Configure the required credentials below.

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "time": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-time"],
      "env": {}
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available time commands"
```

---

## Environment Variables



## Available Tools

- `get_current_time`
- `convert_timezone`
- `parse_date`

## Quick Start Examples

### Example 1
```
User: "Help me with time"
```

## Documentation

See @modelcontextprotocol/server-time documentation for more details.



## Author

community

## Version

1.0.0
