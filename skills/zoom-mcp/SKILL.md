---
name: zoom-mcp
description: Zoom meetings and webinar management
---

# zoom-mcp

Zoom meetings and webinar management

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-zoom
```

### Step 2: Get API Credentials

Get your credentials from: https://marketplace.zoom.us/develop/create

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "zoom": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-zoom"],
      "env": {
            "ZOOM_CLIENT_ID": "your-client-id",
            "ZOOM_CLIENT_SECRET": "your-client-secret",
            "ZOOM_ACCOUNT_ID": "your-account-id"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available zoom commands"
```

---

## Environment Variables

- `ZOOM_CLIENT_ID`: Required - Your client-id
- `ZOOM_CLIENT_SECRET`: Required - Your client-secret
- `ZOOM_ACCOUNT_ID`: Required - Your account-id

## Available Tools

- `list_meetings`
- `create_meeting`
- `get_meeting`
- `list_recordings`

## Quick Start Examples

### Example 1
```
User: "Help me with zoom"
```

## Documentation

See @anthropic/mcp-zoom documentation for more details.



## Author

zoom

## Version

1.0.0
