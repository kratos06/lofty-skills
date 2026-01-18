---
name: snowflake-mcp
description: Snowflake data cloud warehouse
---

# snowflake-mcp

Snowflake data cloud warehouse

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "snowflake-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-snowflake"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add snowflake-mcp
```

## Quick Start

After configuration, the snowflake-mcp tools will be available in Claude Code.

## Features

- snowflake
- warehouse
- analytics





## Author

snowflake

## Version

1.0.0
