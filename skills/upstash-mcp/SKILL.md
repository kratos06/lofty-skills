---
name: upstash-mcp
description: Upstash serverless Redis and Kafka
---

# upstash-mcp

Upstash serverless Redis and Kafka

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "upstash-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-upstash"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add upstash-mcp
```

## Quick Start

After configuration, the upstash-mcp tools will be available in Claude Code.

## Features

- upstash
- redis
- kafka





## Author

upstash

## Version

1.0.0
