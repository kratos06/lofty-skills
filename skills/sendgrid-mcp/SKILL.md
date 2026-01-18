---
name: sendgrid-mcp
description: SendGrid email marketing and delivery
---

# sendgrid-mcp

SendGrid email marketing and delivery

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "sendgrid-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-sendgrid"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add sendgrid-mcp
```

## Quick Start

After configuration, the sendgrid-mcp tools will be available in Claude Code.

## Features

- sendgrid
- email
- marketing





## Author

sendgrid

## Version

1.0.0
