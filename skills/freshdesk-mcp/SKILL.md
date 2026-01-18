---
name: freshdesk-mcp
description: Freshdesk helpdesk ticketing system integration
---

# freshdesk-mcp

Freshdesk helpdesk ticketing system integration

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "freshdesk-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-freshdesk"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add freshdesk-mcp
```

## Quick Start

After configuration, the freshdesk-mcp tools will be available in Claude Code.

## Features

- freshdesk
- helpdesk
- tickets



## Source

GitHub: https://github.com/freshworks/freshdesk-mcp

## Author

Freshworks

## Version

1.0.0
