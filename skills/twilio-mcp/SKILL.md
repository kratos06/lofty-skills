---
name: twilio-mcp
description: Twilio SMS and voice communication
---

# twilio-mcp

Twilio SMS and voice communication

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "twilio-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-twilio"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add twilio-mcp
```

## Quick Start

After configuration, the twilio-mcp tools will be available in Claude Code.

## Features

- twilio
- sms
- voice





## Author

Twilio

## Version

1.0.0
