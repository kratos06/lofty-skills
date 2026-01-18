---
name: pipedrive-mcp
description: Pipedrive sales pipeline management and deal tracking
---

# pipedrive-mcp

Pipedrive sales pipeline management and deal tracking

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "pipedrive-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-pipedrive"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add pipedrive-mcp
```

## Quick Start

After configuration, the pipedrive-mcp tools will be available in Claude Code.

## Features

- pipedrive
- sales
- deals



## Source

GitHub: https://github.com/pipedrive/mcp-server

## Author

Pipedrive

## Version

1.0.0
