---
name: snowflake-mcp
description: Snowflake data cloud warehouse
---

# snowflake-mcp

Snowflake data cloud warehouse

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-snowflake
```

### Step 2: Get API Credentials

Configure the required credentials below.

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "snowflake": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-snowflake"],
      "env": {
            "SNOWFLAKE_ACCOUNT": "your-account",
            "SNOWFLAKE_USER": "your-user",
            "SNOWFLAKE_PASSWORD": "your-password",
            "SNOWFLAKE_WAREHOUSE": "your-warehouse",
            "SNOWFLAKE_DATABASE": "your-database"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available snowflake commands"
```

---

## Environment Variables

- `SNOWFLAKE_ACCOUNT`: Required - Your account
- `SNOWFLAKE_USER`: Required - Your user
- `SNOWFLAKE_PASSWORD`: Required - Your password
- `SNOWFLAKE_WAREHOUSE`: Required - Your warehouse
- `SNOWFLAKE_DATABASE`: Required - Your database

## Available Tools

- `query`
- `list_tables`
- `describe_table`

## Quick Start Examples

### Example 1
```
User: "Help me with snowflake"
```

## Documentation

See @anthropic/mcp-snowflake documentation for more details.



## Author

snowflake

## Version

1.0.0
