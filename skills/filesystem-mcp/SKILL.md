---
name: filesystem-mcp
description: Local filesystem navigation, search, and file operations (Official)
---

# filesystem-mcp

Local filesystem navigation, search, and file operations (Official)

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "filesystem-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-filesystem"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add filesystem-mcp
```

## Quick Start

After configuration, the filesystem-mcp tools will be available in Claude Code.

## Features

- filesystem
- files
- local



## Source

GitHub: https://github.com/modelcontextprotocol/servers/tree/main/src/filesystem

## Author

Anthropic

## Version

1.0.0
