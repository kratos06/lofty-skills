---
name: azure-mcp
description: Azure comprehensive integration with cloud services (Official)
---

# azure-mcp

Azure comprehensive integration with cloud services (Official)

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "azure-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-azure"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add azure-mcp
```

## Quick Start

After configuration, the azure-mcp tools will be available in Claude Code.

## Features

- azure
- microsoft
- cloud



## Source

GitHub: https://github.com/azure/mcp-server

## Author

Microsoft

## Version

1.0.0
