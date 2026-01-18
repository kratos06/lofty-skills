---
name: zoho-mcp
description: Zoho CRM suite integration for complete business management
---

# zoho-mcp

Zoho CRM suite integration for complete business management

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-zoho
```

### Step 2: Get API Credentials

Get your credentials from: https://api-console.zoho.com/

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "zoho": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-zoho"],
      "env": {
            "ZOHO_CLIENT_ID": "your-client-id",
            "ZOHO_CLIENT_SECRET": "your-client-secret",
            "ZOHO_REFRESH_TOKEN": "your-refresh-token"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available zoho commands"
```

---

## Environment Variables

- `ZOHO_CLIENT_ID`: Required - Your client-id
- `ZOHO_CLIENT_SECRET`: Required - Your client-secret
- `ZOHO_REFRESH_TOKEN`: Required - Your refresh-token

## Available Tools

- `list_records`
- `get_record`
- `create_record`
- `update_record`

## Quick Start Examples

### Example 1
```
User: "Help me with zoho"
```

## Documentation

See @anthropic/mcp-zoho documentation for more details.

## Source

GitHub: https://github.com/zoho/mcp-server

## Author

Zoho

## Version

1.0.0
