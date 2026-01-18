---
name: sqlite-mcp
description: SQLite local database operations
---

# sqlite-mcp

SQLite local database operations

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-sqlite
```

### Step 2: Get API Credentials

Configure the required credentials below.

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "sqlite": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-sqlite"],
      "env": {
            "SQLITE_DB_PATH": "/path/to/database.db"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available sqlite commands"
```

---

## Environment Variables

- `SQLITE_DB_PATH`: /path/to/database.db

## Available Tools

- `query`
- `list_tables`
- `describe_table`
- `execute`

## Quick Start Examples

### Example 1
```
User: "Help me with sqlite"
```

## Documentation

See @modelcontextprotocol/server-sqlite documentation for more details.

## Source

GitHub: https://github.com/modelcontextprotocol/servers/tree/main/src/sqlite

## Author

Anthropic

## Version

1.0.0
