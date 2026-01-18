---
name: upstash-mcp
description: Upstash serverless Redis and Kafka
---

# upstash-mcp

Upstash serverless Redis and Kafka

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-upstash
```

### Step 2: Get API Credentials

Get your credentials from: https://console.upstash.com/

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "upstash": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-upstash"],
      "env": {
            "UPSTASH_REDIS_REST_URL": "https://your-endpoint.upstash.io",
            "UPSTASH_REDIS_REST_TOKEN": "your-token"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available upstash commands"
```

---

## Environment Variables

- `UPSTASH_REDIS_REST_URL`: Required - https://Your endpoint.upstash.io
- `UPSTASH_REDIS_REST_TOKEN`: Required - Your token

## Available Tools

- `get`
- `set`
- `delete`
- `keys`

## Quick Start Examples

### Example 1
```
User: "Help me with upstash"
```

## Documentation

See @anthropic/mcp-upstash documentation for more details.



## Author

upstash

## Version

1.0.0
