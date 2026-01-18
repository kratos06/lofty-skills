---
name: microsoft365-mcp
description: Microsoft 365 unified integration for Office, Teams, and SharePoint
---

# microsoft365-mcp

Microsoft 365 unified integration for Office, Teams, and SharePoint

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-microsoft365
```

### Step 2: Get API Credentials

Get your credentials from: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationsListBlade

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "microsoft365": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-microsoft365"],
      "env": {
            "MICROSOFT_CLIENT_ID": "your-client-id",
            "MICROSOFT_CLIENT_SECRET": "your-client-secret",
            "MICROSOFT_TENANT_ID": "your-tenant-id"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available microsoft365 commands"
```

---

## Environment Variables

- `MICROSOFT_CLIENT_ID`: Required - Your client-id
- `MICROSOFT_CLIENT_SECRET`: Required - Your client-secret
- `MICROSOFT_TENANT_ID`: Required - Your tenant-id

## Available Tools

- `list_emails`
- `send_email`
- `list_events`
- `create_event`
- `list_files`

## Quick Start Examples

### Example 1
```
User: "Help me with microsoft365"
```

## Documentation

See @anthropic/mcp-microsoft365 documentation for more details.

## Source

GitHub: https://github.com/microsoft/mcp-server

## Author

Microsoft

## Version

1.0.0
