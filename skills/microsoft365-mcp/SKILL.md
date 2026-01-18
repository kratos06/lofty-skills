---
name: microsoft365-mcp
description: Microsoft 365 unified integration for Office, Teams, and SharePoint
---

# microsoft365-mcp

Microsoft 365 unified integration for Office, Teams, and SharePoint

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "microsoft365-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-microsoft365"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add microsoft365-mcp
```

## Quick Start

After configuration, the microsoft365-mcp tools will be available in Claude Code.

## Features

- microsoft
- office
- 365



## Source

GitHub: https://github.com/microsoft/mcp-server

## Author

Microsoft

## Version

1.0.0
