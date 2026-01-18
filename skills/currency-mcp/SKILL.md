---
name: currency-mcp
description: Currency exchange rates
---

# currency-mcp

Currency exchange rates

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-currency
```

### Step 2: Get API Credentials

Get your credentials from: https://www.exchangerate-api.com/

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "currency": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-currency"],
      "env": {
            "EXCHANGE_RATE_API_KEY": "your-api-key"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available currency commands"
```

---

## Environment Variables

- `EXCHANGE_RATE_API_KEY`: Required - Your api-key

## Available Tools

- `convert`
- `get_rates`
- `list_currencies`

## Quick Start Examples

### Example 1
```
User: "Help me with currency"
```

## Documentation

See @anthropic/mcp-currency documentation for more details.



## Author

community

## Version

1.0.0
