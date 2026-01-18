---
name: asana-mcp
description: Asana task management with project tracking and team collaboration
---

# asana-mcp

Asana task management with project tracking and team collaboration

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "asana-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-asana"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add asana-mcp
```

## Quick Start

After configuration, the asana-mcp tools will be available in Claude Code.

## Features

- asana
- tasks
- project-management



## Source

GitHub: https://github.com/asana/mcp-server

## Author

Asana

## Version

1.0.0
