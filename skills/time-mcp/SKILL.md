---
name: time-mcp
description: Time and timezone operations
---

# time-mcp

Time and timezone operations

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "time-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-time"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add time-mcp
```

## Quick Start

After configuration, the time-mcp tools will be available in Claude Code.

## Features

- time
- timezone
- date





## Author

community

## Version

1.0.0
