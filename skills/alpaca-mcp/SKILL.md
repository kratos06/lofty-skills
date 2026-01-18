---
name: alpaca-mcp
description: Alpaca stock trading API
---

# alpaca-mcp

Alpaca stock trading API

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-alpaca
```

### Step 2: Get API Credentials

Get your credentials from: https://app.alpaca.markets/paper/dashboard/overview

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "alpaca": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-alpaca"],
      "env": {
            "ALPACA_API_KEY": "your-api-key",
            "ALPACA_API_SECRET": "your-api-secret"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available alpaca commands"
```

---

## Environment Variables

- `ALPACA_API_KEY`: Required - Your api-key
- `ALPACA_API_SECRET`: Required - Your api-secret

## Available Tools

- `get_account`
- `list_positions`
- `create_order`
- `get_bars`

## Quick Start Examples

### Example 1
```
User: "Help me with alpaca"
```

## Documentation

See @anthropic/mcp-alpaca documentation for more details.



## Author

alpaca

## Version

1.0.0
