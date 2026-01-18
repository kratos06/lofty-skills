---
name: graphql-mcp
description: GraphQL query and schema management
---

# graphql-mcp

GraphQL query and schema management

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "graphql-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-graphql"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add graphql-mcp
```

## Quick Start

After configuration, the graphql-mcp tools will be available in Claude Code.

## Features

- graphql
- api
- query





## Author

graphql

## Version

1.0.0
