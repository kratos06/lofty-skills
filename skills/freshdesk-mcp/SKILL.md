---
name: freshdesk-mcp
description: Freshdesk helpdesk ticketing system integration
---

# freshdesk-mcp

Freshdesk helpdesk ticketing system integration

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-freshdesk
```

### Step 2: Get API Credentials

Get your credentials from: https://support.freshdesk.com/support/solutions/articles/215517-how-to-find-your-api-key

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "freshdesk": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-freshdesk"],
      "env": {
            "FRESHDESK_DOMAIN": "your-domain.freshdesk.com",
            "FRESHDESK_API_KEY": "your-api-key"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available freshdesk commands"
```

---

## Environment Variables

- `FRESHDESK_DOMAIN`: Required - Your domain.freshdesk.com
- `FRESHDESK_API_KEY`: Required - Your api-key

## Available Tools

- `list_tickets`
- `get_ticket`
- `create_ticket`
- `update_ticket`

## Quick Start Examples

### Example 1
```
User: "Help me with freshdesk"
```

## Documentation

See @anthropic/mcp-freshdesk documentation for more details.

## Source

GitHub: https://github.com/freshworks/freshdesk-mcp

## Author

Freshworks

## Version

1.0.0
