---
name: netlify-mcp
description: Netlify site deployment and functions
---

# netlify-mcp

Netlify site deployment and functions

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "netlify-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-netlify"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add netlify-mcp
```

## Quick Start

After configuration, the netlify-mcp tools will be available in Claude Code.

## Features

- netlify
- deployment
- jamstack



## Source

GitHub: https://github.com/netlify/mcp-server

## Author

Netlify

## Version

1.0.0
