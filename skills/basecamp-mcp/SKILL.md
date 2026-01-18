---
name: basecamp-mcp
description: Basecamp project collaboration with to-dos and message boards
---

# basecamp-mcp

Basecamp project collaboration with to-dos and message boards

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "basecamp-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-basecamp"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add basecamp-mcp
```

## Quick Start

After configuration, the basecamp-mcp tools will be available in Claude Code.

## Features

- basecamp
- collaboration
- todos



## Source

GitHub: https://github.com/basecamp/mcp-server

## Author

Basecamp

## Version

1.0.0
