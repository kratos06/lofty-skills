---
name: paypal-mcp
description: PayPal payment integration
---

# paypal-mcp

PayPal payment integration

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "paypal-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-paypal"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add paypal-mcp
```

## Quick Start

After configuration, the paypal-mcp tools will be available in Claude Code.

## Features

- paypal
- payments
- checkout





## Author

paypal

## Version

1.0.0
