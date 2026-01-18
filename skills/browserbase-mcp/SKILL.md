---
name: browserbase-mcp
description: Browserbase cloud browser automation
---

# browserbase-mcp

Browserbase cloud browser automation

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "browserbase-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-browserbase"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add browserbase-mcp
```

## Quick Start

After configuration, the browserbase-mcp tools will be available in Claude Code.

## Features

- browserbase
- browser
- automation





## Author

Browserbase

## Version

1.0.0
