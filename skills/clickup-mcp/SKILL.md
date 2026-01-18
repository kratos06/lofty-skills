---
name: clickup-mcp
description: ClickUp project and task management
---

# clickup-mcp

ClickUp project and task management

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "clickup-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-clickup"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add clickup-mcp
```

## Quick Start

After configuration, the clickup-mcp tools will be available in Claude Code.

## Features

- clickup
- productivity
- tasks





## Author

clickup

## Version

1.0.0
