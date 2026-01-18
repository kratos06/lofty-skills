---
name: resend-mcp
description: Resend developer email API
---

# resend-mcp

Resend developer email API

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "resend-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-resend"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add resend-mcp
```

## Quick Start

After configuration, the resend-mcp tools will be available in Claude Code.

## Features

- resend
- email
- api





## Author

resend

## Version

1.0.0
