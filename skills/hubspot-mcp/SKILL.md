---
name: hubspot-mcp
description: HubSpot CRM, marketing, and sales automation
---

# hubspot-mcp

HubSpot CRM, marketing, and sales automation

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "hubspot-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-hubspot"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add hubspot-mcp
```

## Quick Start

After configuration, the hubspot-mcp tools will be available in Claude Code.

## Features

- hubspot
- crm
- marketing





## Author

hubspot

## Version

1.0.0
