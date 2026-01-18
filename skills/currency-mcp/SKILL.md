---
name: currency-mcp
description: Currency exchange rates
---

# currency-mcp

Currency exchange rates

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "currency-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-currency"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add currency-mcp
```

## Quick Start

After configuration, the currency-mcp tools will be available in Claude Code.

## Features

- currency
- exchange
- forex





## Author

community

## Version

1.0.0
