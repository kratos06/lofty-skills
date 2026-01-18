---
name: postgres-mcp
description: PostgreSQL database with schema inspection and read-only queries (Official Anthropic)
---

# postgres-mcp

PostgreSQL database with schema inspection and read-only queries (Official Anthropic)

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "postgres-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-postgres"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add postgres-mcp
```

## Quick Start

After configuration, the postgres-mcp tools will be available in Claude Code.

## Features

- postgresql
- database
- sql



## Source

GitHub: https://github.com/modelcontextprotocol/servers/tree/main/src/postgres

## Author

Anthropic

## Version

1.0.0
