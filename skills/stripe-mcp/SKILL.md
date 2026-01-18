---
name: stripe-mcp
description: Stripe payment processing, subscriptions, and invoicing
---

# stripe-mcp

Stripe payment processing, subscriptions, and invoicing

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "stripe-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-stripe"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add stripe-mcp
```

## Quick Start

After configuration, the stripe-mcp tools will be available in Claude Code.

## Features

- stripe
- payments
- billing



## Source

GitHub: https://github.com/stripe/mcp-server

## Author

Stripe

## Version

1.0.0
