---
name: salesforce-mcp
description: Salesforce CRM data and operations integration
---

# salesforce-mcp

Salesforce CRM data and operations integration

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "salesforce-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-salesforce"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add salesforce-mcp
```

## Quick Start

After configuration, the salesforce-mcp tools will be available in Claude Code.

## Features

- salesforce
- crm
- sales



## Source

GitHub: https://github.com/salesforce/mcp-server

## Author

salesforce

## Version

1.0.0
