---
name: salesforce-mcp
description: Salesforce CRM data and operations integration
---

# salesforce-mcp

Salesforce CRM data and operations integration

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-salesforce
```

### Step 2: Get API Credentials

Get your credentials from: https://help.salesforce.com/s/articleView?id=sf.connected_app_create_api_integration.htm

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "salesforce": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-salesforce"],
      "env": {
            "SALESFORCE_INSTANCE_URL": "https://your-instance.salesforce.com",
            "SALESFORCE_ACCESS_TOKEN": "your-access-token"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available salesforce commands"
```

---

## Environment Variables

- `SALESFORCE_INSTANCE_URL`: Required - https://Your instance.salesforce.com
- `SALESFORCE_ACCESS_TOKEN`: Required - Your access-token

## Available Tools

- `query`
- `create_record`
- `update_record`
- `delete_record`

## Quick Start Examples

### Example 1
```
User: "Help me with salesforce"
```

## Documentation

See @anthropic/mcp-salesforce documentation for more details.

## Source

GitHub: https://github.com/salesforce/mcp-server

## Author

salesforce

## Version

1.0.0
