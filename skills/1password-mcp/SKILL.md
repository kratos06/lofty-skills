---
name: 1password-mcp
description: 1Password password management
---

# 1password-mcp

1Password password management

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-1password
```

### Step 2: Get API Credentials

Get your credentials from: https://developer.1password.com/docs/service-accounts/

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "1password": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-1password"],
      "env": {
            "OP_SERVICE_ACCOUNT_TOKEN": "your-token"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available 1password commands"
```

---

## Environment Variables

- `OP_SERVICE_ACCOUNT_TOKEN`: Required - Your token

## Available Tools

- `get_item`
- `list_items`
- `list_vaults`

## Quick Start Examples

### Example 1
```
User: "Help me with 1password"
```

## Documentation

See @anthropic/mcp-1password documentation for more details.



## Author

1password

## Version

1.0.0
