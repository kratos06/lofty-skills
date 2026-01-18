---
name: mongodb-mcp
description: MongoDB database with Atlas, Community, and vector search support (Official)
---

# mongodb-mcp

MongoDB database with Atlas, Community, and vector search support (Official)

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "mongodb-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-mongodb"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add mongodb-mcp
```

## Quick Start

After configuration, the mongodb-mcp tools will be available in Claude Code.

## Features

- mongodb
- nosql
- database



## Source

GitHub: https://github.com/mongodb-js/mongodb-mcp-server

## Author

MongoDB

## Version

1.0.0
