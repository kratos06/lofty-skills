---
name: mysql-mcp
description: MySQL database operations
---

# mysql-mcp

MySQL database operations

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-mysql
```

### Step 2: Get API Credentials

Configure the required credentials below.

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "mysql": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-mysql"],
      "env": {
            "MYSQL_HOST": "localhost",
            "MYSQL_USER": "root",
            "MYSQL_PASSWORD": "password",
            "MYSQL_DATABASE": "database"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available mysql commands"
```

---

## Environment Variables

- `MYSQL_HOST`: localhost
- `MYSQL_USER`: root
- `MYSQL_PASSWORD`: password
- `MYSQL_DATABASE`: database

## Available Tools

- `query`
- `list_tables`
- `describe_table`
- `execute`

## Quick Start Examples

### Example 1
```
User: "Help me with mysql"
```

## Documentation

See @anthropic/mcp-mysql documentation for more details.



## Author

mysql

## Version

1.0.0
