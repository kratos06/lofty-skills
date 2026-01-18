---
name: twilio-mcp
description: Twilio SMS and voice communication
---

# twilio-mcp

Twilio SMS and voice communication

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-twilio
```

### Step 2: Get API Credentials

Get your credentials from: https://console.twilio.com/

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "twilio": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-twilio"],
      "env": {
            "TWILIO_ACCOUNT_SID": "your-account-sid",
            "TWILIO_AUTH_TOKEN": "your-auth-token"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available twilio commands"
```

---

## Environment Variables

- `TWILIO_ACCOUNT_SID`: Required - Your account-sid
- `TWILIO_AUTH_TOKEN`: Required - Your auth-token

## Available Tools

- `send_sms`
- `make_call`
- `list_messages`
- `list_calls`

## Quick Start Examples

### Example 1
```
User: "Help me with twilio"
```

## Documentation

See @anthropic/mcp-twilio documentation for more details.



## Author

Twilio

## Version

1.0.0
