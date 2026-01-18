---
name: zendesk-mcp
description: Zendesk Support API for ticket management and customer service
---

# zendesk-mcp

Zendesk Support API for ticket management and customer service

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "zendesk-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-zendesk"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add zendesk-mcp
```

## Quick Start

After configuration, the zendesk-mcp tools will be available in Claude Code.

## Features

- zendesk
- support
- tickets



## Source

GitHub: https://github.com/zendesk/mcp-server

## Author

Zendesk

## Version

1.0.0
