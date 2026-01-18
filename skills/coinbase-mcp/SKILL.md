---
name: coinbase-mcp
description: Coinbase cryptocurrency exchange
---

# coinbase-mcp

Coinbase cryptocurrency exchange

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "coinbase-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-coinbase"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add coinbase-mcp
```

## Quick Start

After configuration, the coinbase-mcp tools will be available in Claude Code.

## Features

- coinbase
- crypto
- exchange





## Author

coinbase

## Version

1.0.0
