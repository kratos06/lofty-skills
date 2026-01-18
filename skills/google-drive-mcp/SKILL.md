---
name: google-drive-mcp
description: Google Drive file storage and management
---

# google-drive-mcp

Google Drive file storage and management

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "google-drive-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-google-drive"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add google-drive-mcp
```

## Quick Start

After configuration, the google-drive-mcp tools will be available in Claude Code.

## Features

- google
- drive
- storage



## Source

GitHub: https://github.com/modelcontextprotocol/servers/tree/main/src/gdrive

## Author

Google

## Version

1.0.0
