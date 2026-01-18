---
name: mysql-mcp
description: MySQL database operations
---

# mysql-mcp

MySQL database operations

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "mysql-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-mysql"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add mysql-mcp
```

## Quick Start

After configuration, the mysql-mcp tools will be available in Claude Code.

## Features

- mysql
- sql
- database





## Author

mysql

## Version

1.0.0
