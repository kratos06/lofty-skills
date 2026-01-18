---
name: pagerduty-mcp
description: PagerDuty incident management
---

# pagerduty-mcp

PagerDuty incident management

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-pagerduty
```

### Step 2: Get API Credentials

Get your credentials from: https://support.pagerduty.com/docs/api-access-keys

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "pagerduty": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-pagerduty"],
      "env": {
            "PAGERDUTY_API_KEY": "your-api-key"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available pagerduty commands"
```

---

## Environment Variables

- `PAGERDUTY_API_KEY`: Required - Your api-key

## Available Tools

- `list_incidents`
- `create_incident`
- `resolve_incident`
- `list_services`

## Quick Start Examples

### Example 1
```
User: "Help me with pagerduty"
```

## Documentation

See @anthropic/mcp-pagerduty documentation for more details.



## Author

pagerduty

## Version

1.0.0
