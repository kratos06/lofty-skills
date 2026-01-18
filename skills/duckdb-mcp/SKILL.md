---
name: duckdb-mcp
description: DuckDB analytical database
---

# duckdb-mcp

DuckDB analytical database

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "duckdb-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-duckdb"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add duckdb-mcp
```

## Quick Start

After configuration, the duckdb-mcp tools will be available in Claude Code.

## Features

- duckdb
- analytics
- olap





## Author

duckdb

## Version

1.0.0
