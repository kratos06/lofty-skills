---
name: intercom-mcp
description: Intercom customer conversations and messaging platform
---

# intercom-mcp

Intercom customer conversations and messaging platform

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-intercom
```

### Step 2: Get API Credentials

Get your credentials from: https://app.intercom.com/a/apps/_/developer-hub

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "intercom": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-intercom"],
      "env": {
            "INTERCOM_ACCESS_TOKEN": "your-access-token"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available intercom commands"
```

---

## Environment Variables

- `INTERCOM_ACCESS_TOKEN`: Required - Your access-token

## Available Tools

- `list_conversations`
- `get_conversation`
- `reply_to_conversation`
- `search_contacts`

## Quick Start Examples

### Example 1
```
User: "Help me with intercom"
```

## Documentation

See @anthropic/mcp-intercom documentation for more details.

## Source

GitHub: https://github.com/intercom/mcp-server

## Author

Intercom

## Version

1.0.0
