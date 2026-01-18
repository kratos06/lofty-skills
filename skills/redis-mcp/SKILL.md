---
name: redis-mcp
description: Redis key-value store with vector search capabilities (Official)
---

# redis-mcp

Redis key-value store with vector search capabilities (Official)

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "redis-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-redis"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add redis-mcp
```

## Quick Start

After configuration, the redis-mcp tools will be available in Claude Code.

## Features

- redis
- cache
- key-value



## Source

GitHub: https://github.com/redis/mcp-redis

## Author

Redis

## Version

1.0.0
