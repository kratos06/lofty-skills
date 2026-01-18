---
name: alpaca-mcp
description: Alpaca stock trading API
---

# alpaca-mcp

Alpaca stock trading API

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "alpaca-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-alpaca"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add alpaca-mcp
```

## Quick Start

After configuration, the alpaca-mcp tools will be available in Claude Code.

## Features

- alpaca
- stocks
- trading





## Author

alpaca

## Version

1.0.0
