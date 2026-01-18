---
name: duckdb-mcp
description: DuckDB analytical database
---

# duckdb-mcp

DuckDB analytical database

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-duckdb
```

### Step 2: Get API Credentials

Configure the required credentials below.

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "duckdb": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-duckdb"],
      "env": {
            "DUCKDB_PATH": "/path/to/database.duckdb"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available duckdb commands"
```

---

## Environment Variables

- `DUCKDB_PATH`: /path/to/database.duckdb

## Available Tools

- `query`
- `list_tables`
- `describe_table`

## Quick Start Examples

### Example 1
```
User: "Help me with duckdb"
```

## Documentation

See @anthropic/mcp-duckdb documentation for more details.



## Author

duckdb

## Version

1.0.0
