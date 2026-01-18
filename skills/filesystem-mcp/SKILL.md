---
name: filesystem-mcp
description: Local filesystem navigation, search, and file operations (Official)
---

# filesystem-mcp

Local filesystem navigation, search, and file operations (Official)

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @modelcontextprotocol/server-filesystem
```

### Step 2: Get API Credentials

Configure the required credentials below.

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "filesystem": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-filesystem"],
      "env": {
            "ALLOWED_DIRECTORIES": "/path/to/allowed/dir"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available filesystem commands"
```

---

## Environment Variables

- `ALLOWED_DIRECTORIES`: /path/to/allowed/dir

## Available Tools

- `read_file`
- `write_file`
- `list_directory`
- `create_directory`

## Quick Start Examples

### Example 1
```
User: "Help me with filesystem"
```

## Documentation

See @modelcontextprotocol/server-filesystem documentation for more details.

## Source

GitHub: https://github.com/modelcontextprotocol/servers/tree/main/src/filesystem

## Author

Anthropic

## Version

1.0.0
