---
name: google-drive-mcp
description: Google Drive file storage and management
---

# google-drive-mcp

Google Drive file storage and management

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-google-drive
```

### Step 2: Get API Credentials

Get your credentials from: https://console.cloud.google.com/apis/credentials

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "google-drive": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-google-drive"],
      "env": {
            "GOOGLE_CLIENT_ID": "your-client-id",
            "GOOGLE_CLIENT_SECRET": "your-client-secret",
            "GOOGLE_REFRESH_TOKEN": "your-refresh-token"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available google-drive commands"
```

---

## Environment Variables

- `GOOGLE_CLIENT_ID`: Required - Your client-id
- `GOOGLE_CLIENT_SECRET`: Required - Your client-secret
- `GOOGLE_REFRESH_TOKEN`: Required - Your refresh-token

## Available Tools

- `list_files`
- `get_file`
- `upload_file`
- `search`

## Quick Start Examples

### Example 1
```
User: "Help me with google-drive"
```

## Documentation

See @anthropic/mcp-google-drive documentation for more details.

## Source

GitHub: https://github.com/modelcontextprotocol/servers/tree/main/src/gdrive

## Author

Google

## Version

1.0.0
