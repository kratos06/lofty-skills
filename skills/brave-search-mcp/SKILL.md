---
name: brave-search-mcp
description: Brave Search API integration
---

# brave-search-mcp

Brave Search API integration

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "brave-search-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-brave-search"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add brave-search-mcp
```

## Quick Start

After configuration, the brave-search-mcp tools will be available in Claude Code.

## Features

- brave
- search
- privacy



## Source

GitHub: https://github.com/anthropics/brave-search-mcp

## Author

Brave

## Version

1.0.0
