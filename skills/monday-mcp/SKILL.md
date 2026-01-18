---
name: monday-mcp
description: Monday.com board management with items and team planning
---

# monday-mcp

Monday.com board management with items and team planning

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "monday-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-monday"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add monday-mcp
```

## Quick Start

After configuration, the monday-mcp tools will be available in Claude Code.

## Features

- monday
- boards
- planning



## Source

GitHub: https://github.com/monday/mcp-server

## Author

Monday.com

## Version

1.0.0
