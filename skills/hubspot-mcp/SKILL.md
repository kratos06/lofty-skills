---
name: hubspot-mcp
description: HubSpot CRM, marketing, and sales automation
---

# hubspot-mcp

HubSpot CRM, marketing, and sales automation

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-hubspot
```

### Step 2: Get API Credentials

Get your credentials from: https://app.hubspot.com/private-apps/

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "hubspot": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-hubspot"],
      "env": {
            "HUBSPOT_ACCESS_TOKEN": "pat-your-token"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available hubspot commands"
```

---

## Environment Variables

- `HUBSPOT_ACCESS_TOKEN`: Required - pat-Your token

## Available Tools

- `list_contacts`
- `create_contact`
- `list_deals`
- `create_deal`

## Quick Start Examples

### Example 1
```
User: "Help me with hubspot"
```

## Documentation

See @anthropic/mcp-hubspot documentation for more details.



## Author

hubspot

## Version

1.0.0
