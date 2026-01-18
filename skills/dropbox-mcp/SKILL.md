---
name: dropbox-mcp
description: Dropbox cloud storage integration
---

# dropbox-mcp

Dropbox cloud storage integration

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "dropbox-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-dropbox"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add dropbox-mcp
```

## Quick Start

After configuration, the dropbox-mcp tools will be available in Claude Code.

## Features

- dropbox
- storage
- sync





## Author

dropbox

## Version

1.0.0
