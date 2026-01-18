---
name: google-workspace-mcp
description: Google Workspace integration for Docs, Sheets, Drive, and Calendar
---

# google-workspace-mcp

Google Workspace integration for Docs, Sheets, Drive, and Calendar

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-google-workspace
```

### Step 2: Get API Credentials

Get your credentials from: https://console.cloud.google.com/apis/credentials

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "google-workspace": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-google-workspace"],
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
User: "List available google-workspace commands"
```

---

## Environment Variables

- `GOOGLE_CLIENT_ID`: Required - Your client-id
- `GOOGLE_CLIENT_SECRET`: Required - Your client-secret
- `GOOGLE_REFRESH_TOKEN`: Required - Your refresh-token

## Available Tools

- `list_emails`
- `send_email`
- `list_events`
- `create_event`
- `list_files`

## Quick Start Examples

### Example 1
```
User: "Help me with google-workspace"
```

## Documentation

See @anthropic/mcp-google-workspace documentation for more details.

## Source

GitHub: https://github.com/google/mcp-server

## Author

Google

## Version

1.0.0
