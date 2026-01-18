---
name: paypal-mcp
description: PayPal payment integration
---

# paypal-mcp

PayPal payment integration

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-paypal
```

### Step 2: Get API Credentials

Get your credentials from: https://developer.paypal.com/dashboard/applications/sandbox

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "paypal": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-paypal"],
      "env": {
            "PAYPAL_CLIENT_ID": "your-client-id",
            "PAYPAL_CLIENT_SECRET": "your-client-secret"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available paypal commands"
```

---

## Environment Variables

- `PAYPAL_CLIENT_ID`: Required - Your client-id
- `PAYPAL_CLIENT_SECRET`: Required - Your client-secret

## Available Tools

- `list_transactions`
- `create_payment`
- `capture_payment`

## Quick Start Examples

### Example 1
```
User: "Help me with paypal"
```

## Documentation

See @anthropic/mcp-paypal documentation for more details.



## Author

paypal

## Version

1.0.0
