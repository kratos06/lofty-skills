---
name: stripe-mcp
description: Stripe payment processing, subscriptions, and invoicing
---

# stripe-mcp

Stripe payment processing, subscriptions, and invoicing

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-stripe
```

### Step 2: Get API Credentials

Get your credentials from: https://dashboard.stripe.com/apikeys

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "stripe": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-stripe"],
      "env": {
            "STRIPE_SECRET_KEY": "sk_your-secret-key"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available stripe commands"
```

---

## Environment Variables

- `STRIPE_SECRET_KEY`: Required - sk_Your secret-key

## Available Tools

- `list_customers`
- `create_customer`
- `list_payments`
- `create_payment`

## Quick Start Examples

### Example 1
```
User: "Help me with stripe"
```

## Documentation

See @anthropic/mcp-stripe documentation for more details.

## Source

GitHub: https://github.com/stripe/mcp-server

## Author

Stripe

## Version

1.0.0
