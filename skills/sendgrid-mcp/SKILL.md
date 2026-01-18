---
name: sendgrid-mcp
description: SendGrid email marketing and delivery
---

# sendgrid-mcp

SendGrid email marketing and delivery

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-sendgrid
```

### Step 2: Get API Credentials

Get your credentials from: https://app.sendgrid.com/settings/api_keys

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "sendgrid": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-sendgrid"],
      "env": {
            "SENDGRID_API_KEY": "your-api-key"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available sendgrid commands"
```

---

## Environment Variables

- `SENDGRID_API_KEY`: Required - Your api-key

## Available Tools

- `send_email`
- `list_templates`
- `get_stats`

## Quick Start Examples

### Example 1
```
User: "Help me with sendgrid"
```

## Documentation

See @anthropic/mcp-sendgrid documentation for more details.



## Author

sendgrid

## Version

1.0.0
