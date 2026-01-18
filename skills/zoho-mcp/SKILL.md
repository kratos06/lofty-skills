---
name: zoho-mcp
description: Zoho CRM suite integration for complete business management
---

# zoho-mcp

Zoho CRM suite integration for complete business management

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "zoho-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-zoho"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add zoho-mcp
```

## Quick Start

After configuration, the zoho-mcp tools will be available in Claude Code.

## Features

- zoho
- crm
- business



## Source

GitHub: https://github.com/zoho/mcp-server

## Author

Zoho

## Version

1.0.0
