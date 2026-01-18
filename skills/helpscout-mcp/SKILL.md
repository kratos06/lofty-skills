---
name: helpscout-mcp
description: Help Scout email support and customer communication
---

# helpscout-mcp

Help Scout email support and customer communication

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "helpscout-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-helpscout"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add helpscout-mcp
```

## Quick Start

After configuration, the helpscout-mcp tools will be available in Claude Code.

## Features

- helpscout
- email
- support



## Source

GitHub: https://github.com/helpscout/mcp-server

## Author

Help Scout

## Version

1.0.0
