---
name: zendesk-mcp
description: Zendesk Support API for ticket management and customer service
---

# zendesk-mcp

Zendesk Support API for ticket management and customer service

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-zendesk
```

### Step 2: Get API Credentials

Get your credentials from: https://your-subdomain.zendesk.com/admin/apps-integrations/apis/zendesk-api/settings

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "zendesk": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-zendesk"],
      "env": {
            "ZENDESK_SUBDOMAIN": "your-subdomain",
            "ZENDESK_EMAIL": "your-email@example.com",
            "ZENDESK_API_TOKEN": "your-api-token"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available zendesk commands"
```

---

## Environment Variables

- `ZENDESK_SUBDOMAIN`: Required - Your subdomain
- `ZENDESK_EMAIL`: Required - Your email@example.com
- `ZENDESK_API_TOKEN`: Required - Your api-token

## Available Tools

- `list_tickets`
- `get_ticket`
- `create_ticket`
- `update_ticket`
- `search`

## Quick Start Examples

### Example 1
```
User: "Help me with zendesk"
```

## Documentation

See @anthropic/mcp-zendesk documentation for more details.

## Source

GitHub: https://github.com/zendesk/mcp-server

## Author

Zendesk

## Version

1.0.0
