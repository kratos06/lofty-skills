---
name: memory-mcp
description: Knowledge graph memory for persistent context across sessions
---

# memory-mcp

Knowledge graph memory for persistent context across sessions

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-memory
```

### Step 2: Get API Credentials

Configure the required credentials below.

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "memory": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-memory"],
      "env": {}
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available memory commands"
```

---

## Environment Variables



## Available Tools

- `store`
- `retrieve`
- `search`
- `delete`

## Quick Start Examples

### Example 1
```
User: "Help me with memory"
```

## Documentation

See @modelcontextprotocol/server-memory documentation for more details.

## Source

GitHub: https://github.com/modelcontextprotocol/servers/tree/main/src/memory

## Author

Anthropic

## Version

1.0.0
