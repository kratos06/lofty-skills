---
name: memory-mcp
description: Knowledge graph memory for persistent context across sessions
---

# memory-mcp

Knowledge graph memory for persistent context across sessions

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "memory-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-memory"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add memory-mcp
```

## Quick Start

After configuration, the memory-mcp tools will be available in Claude Code.

## Features

- memory
- knowledge-graph
- context



## Source

GitHub: https://github.com/modelcontextprotocol/servers/tree/main/src/memory

## Author

Anthropic

## Version

1.0.0
