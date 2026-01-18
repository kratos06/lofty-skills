---
name: resend-mcp
description: Resend developer email API
---

# resend-mcp

Resend developer email API

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-resend
```

### Step 2: Get API Credentials

Get your credentials from: https://resend.com/api-keys

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "resend": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-resend"],
      "env": {
            "RESEND_API_KEY": "re_your-api-key"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available resend commands"
```

---

## Environment Variables

- `RESEND_API_KEY`: Required - re_Your api-key

## Available Tools

- `send_email`
- `list_emails`
- `get_email`

## Quick Start Examples

### Example 1
```
User: "Help me with resend"
```

## Documentation

See @anthropic/mcp-resend documentation for more details.



## Author

resend

## Version

1.0.0
