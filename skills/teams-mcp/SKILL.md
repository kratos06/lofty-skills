---
name: teams-mcp
description: Microsoft Teams messaging and meetings
---

# teams-mcp

Microsoft Teams messaging and meetings

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-teams
```

### Step 2: Get API Credentials

Get your credentials from: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationsListBlade

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "teams": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-teams"],
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
User: "List available teams commands"
```

---

## Environment Variables

- `MICROSOFT_CLIENT_ID`: Required - Your client-id
- `MICROSOFT_CLIENT_SECRET`: Required - Your client-secret
- `MICROSOFT_TENANT_ID`: Required - Your tenant-id

## Available Tools

- `list_teams`
- `list_channels`
- `send_message`
- `get_messages`

## Quick Start Examples

### Example 1
```
User: "Help me with teams"
```

## Documentation

See @anthropic/mcp-teams documentation for more details.



## Author

microsoft

## Version

1.0.0
