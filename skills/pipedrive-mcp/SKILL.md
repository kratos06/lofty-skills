---
name: pipedrive-mcp
description: Pipedrive sales pipeline management and deal tracking
---

# pipedrive-mcp

Pipedrive sales pipeline management and deal tracking

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-pipedrive
```

### Step 2: Get API Credentials

Get your credentials from: https://app.pipedrive.com/settings/api

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "pipedrive": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-pipedrive"],
      "env": {
            "PIPEDRIVE_API_TOKEN": "your-api-token"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available pipedrive commands"
```

---

## Environment Variables

- `PIPEDRIVE_API_TOKEN`: Required - Your api-token

## Available Tools

- `list_deals`
- `create_deal`
- `list_persons`
- `create_person`

## Quick Start Examples

### Example 1
```
User: "Help me with pipedrive"
```

## Documentation

See @anthropic/mcp-pipedrive documentation for more details.

## Source

GitHub: https://github.com/pipedrive/mcp-server

## Author

Pipedrive

## Version

1.0.0
