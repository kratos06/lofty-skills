---
name: coinbase-mcp
description: Coinbase cryptocurrency exchange
---

# coinbase-mcp

Coinbase cryptocurrency exchange

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-coinbase
```

### Step 2: Get API Credentials

Get your credentials from: https://www.coinbase.com/settings/api

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "coinbase": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-coinbase"],
      "env": {
            "COINBASE_API_KEY": "your-api-key",
            "COINBASE_API_SECRET": "your-api-secret"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available coinbase commands"
```

---

## Environment Variables

- `COINBASE_API_KEY`: Required - Your api-key
- `COINBASE_API_SECRET`: Required - Your api-secret

## Available Tools

- `list_accounts`
- `get_price`
- `create_transaction`

## Quick Start Examples

### Example 1
```
User: "Help me with coinbase"
```

## Documentation

See @anthropic/mcp-coinbase documentation for more details.



## Author

coinbase

## Version

1.0.0
