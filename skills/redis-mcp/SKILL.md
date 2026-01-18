---
name: redis-mcp
description: Redis key-value store with vector search capabilities (Official)
---

# redis-mcp

Redis key-value store with vector search capabilities (Official)

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-redis
```

### Step 2: Get API Credentials

Configure the required credentials below.

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "redis": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-redis"],
      "env": {
            "REDIS_URL": "redis://localhost:6379"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available redis commands"
```

---

## Environment Variables

- `REDIS_URL`: redis://localhost:6379

## Available Tools

- `get`
- `set`
- `delete`
- `keys`
- `hget`
- `hset`

## Quick Start Examples

### Example 1
```
User: "Help me with redis"
```

## Documentation

See @anthropic/mcp-redis documentation for more details.

## Source

GitHub: https://github.com/redis/mcp-redis

## Author

Redis

## Version

1.0.0
