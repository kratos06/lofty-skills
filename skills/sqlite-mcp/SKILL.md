---
name: sqlite-mcp
description: SQLite local database operations
---

# sqlite-mcp

SQLite local database operations

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "sqlite-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-sqlite"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add sqlite-mcp
```

## Quick Start

After configuration, the sqlite-mcp tools will be available in Claude Code.

## Features

- sqlite
- sql
- embedded



## Source

GitHub: https://github.com/modelcontextprotocol/servers/tree/main/src/sqlite

## Author

Anthropic

## Version

1.0.0
