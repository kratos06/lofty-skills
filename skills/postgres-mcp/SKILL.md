---
name: postgres-mcp
description: PostgreSQL database with schema inspection and read-only queries (Official Anthropic)
---

# postgres-mcp

PostgreSQL database with schema inspection and read-only queries (Official Anthropic)

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-postgres
```

### Step 2: Get API Credentials

Configure the required credentials below.

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "postgres": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-postgres"],
      "env": {
            "POSTGRES_CONNECTION_STRING": "postgresql://user:password@localhost:5432/database"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available postgres commands"
```

---

## Environment Variables

- `POSTGRES_CONNECTION_STRING`: postgresql://user:password@localhost:5432/database

## Available Tools

- `query`
- `list_tables`
- `describe_table`
- `execute`

## Quick Start Examples

### Example 1
```
User: "Help me with postgres"
```

## Documentation

See @modelcontextprotocol/server-postgres documentation for more details.

## Source

GitHub: https://github.com/modelcontextprotocol/servers/tree/main/src/postgres

## Author

Anthropic

## Version

1.0.0
