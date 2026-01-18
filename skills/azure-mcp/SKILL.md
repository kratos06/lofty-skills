---
name: azure-mcp
description: Azure comprehensive integration with cloud services (Official)
---

# azure-mcp

Azure comprehensive integration with cloud services (Official)

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-azure
```

### Step 2: Get API Credentials

Get your credentials from: https://portal.azure.com/

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "azure": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-azure"],
      "env": {
            "AZURE_SUBSCRIPTION_ID": "your-subscription-id",
            "AZURE_TENANT_ID": "your-tenant-id",
            "AZURE_CLIENT_ID": "your-client-id",
            "AZURE_CLIENT_SECRET": "your-client-secret"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available azure commands"
```

---

## Environment Variables

- `AZURE_SUBSCRIPTION_ID`: Required - Your subscription-id
- `AZURE_TENANT_ID`: Required - Your tenant-id
- `AZURE_CLIENT_ID`: Required - Your client-id
- `AZURE_CLIENT_SECRET`: Required - Your client-secret

## Available Tools

- `list_resources`
- `get_resource`
- `create_resource`

## Quick Start Examples

### Example 1
```
User: "Help me with azure"
```

## Documentation

See @anthropic/mcp-azure documentation for more details.

## Source

GitHub: https://github.com/azure/mcp-server

## Author

Microsoft

## Version

1.0.0
