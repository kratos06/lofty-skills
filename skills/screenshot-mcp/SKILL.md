---
name: screenshot-mcp
description: Website screenshot capture
---

# screenshot-mcp

Website screenshot capture

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "screenshot-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-screenshot"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add screenshot-mcp
```

## Quick Start

After configuration, the screenshot-mcp tools will be available in Claude Code.

## Features

- screenshot
- capture
- images





## Author

community

## Version

1.0.0
