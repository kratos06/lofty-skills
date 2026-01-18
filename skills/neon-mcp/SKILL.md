---
name: neon-mcp
description: Neon serverless PostgreSQL
---

# neon-mcp

Neon serverless PostgreSQL

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-neon
```

### Step 2: Get API Credentials

Get your credentials from: https://console.neon.tech/

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "neon": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-neon"],
      "env": {
            "NEON_CONNECTION_STRING": "postgresql://user:password@ep-xxx.region.aws.neon.tech/database"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available neon commands"
```

---

## Environment Variables

- `NEON_CONNECTION_STRING`: postgresql://user:password@ep-xxx.region.aws.neon.tech/database

## Available Tools

- `query`
- `list_tables`
- `describe_table`

## Quick Start Examples

### Example 1
```
User: "Help me with neon"
```

## Documentation

See @anthropic/mcp-neon documentation for more details.



## Author

neon

## Version

1.0.0
