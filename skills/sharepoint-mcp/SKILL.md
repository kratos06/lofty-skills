---
name: sharepoint-mcp
description: SharePoint document and site management
---

# sharepoint-mcp

SharePoint document and site management

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-sharepoint
```

### Step 2: Get API Credentials

Get your credentials from: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationsListBlade

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "sharepoint": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-sharepoint"],
      "env": {
            "MICROSOFT_CLIENT_ID": "your-client-id",
            "MICROSOFT_CLIENT_SECRET": "your-client-secret",
            "MICROSOFT_TENANT_ID": "your-tenant-id",
            "SHAREPOINT_SITE_URL": "https://your-tenant.sharepoint.com/sites/your-site"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available sharepoint commands"
```

---

## Environment Variables

- `MICROSOFT_CLIENT_ID`: Required - Your client-id
- `MICROSOFT_CLIENT_SECRET`: Required - Your client-secret
- `MICROSOFT_TENANT_ID`: Required - Your tenant-id
- `SHAREPOINT_SITE_URL`: Required - https://Your tenant.sharepoint.com/sites/your-site

## Available Tools

- `list_files`
- `get_file`
- `upload_file`
- `search`

## Quick Start Examples

### Example 1
```
User: "Help me with sharepoint"
```

## Documentation

See @anthropic/mcp-sharepoint documentation for more details.



## Author

microsoft

## Version

1.0.0
