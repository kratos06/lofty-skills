---
name: mongodb-mcp
description: MongoDB database with Atlas, Community, and vector search support (Official)
---

# mongodb-mcp

MongoDB database with Atlas, Community, and vector search support (Official)

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-mongodb
```

### Step 2: Get API Credentials

Configure the required credentials below.

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "mongodb": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-mongodb"],
      "env": {
            "MONGODB_URI": "mongodb://localhost:27017/database"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available mongodb commands"
```

---

## Environment Variables

- `MONGODB_URI`: mongodb://localhost:27017/database

## Available Tools

- `find`
- `insert`
- `update`
- `delete`
- `aggregate`

## Quick Start Examples

### Example 1
```
User: "Help me with mongodb"
```

## Documentation

See @anthropic/mcp-mongodb documentation for more details.

## Source

GitHub: https://github.com/mongodb-js/mongodb-mcp-server

## Author

MongoDB

## Version

1.0.0
