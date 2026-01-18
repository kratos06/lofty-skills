---
name: vercel-mcp
description: Vercel deployment and project management
---

# vercel-mcp

Vercel deployment and project management

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "vercel-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-vercel"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add vercel-mcp
```

## Quick Start

After configuration, the vercel-mcp tools will be available in Claude Code.

## Features

- vercel
- deployment
- hosting



## Source

GitHub: https://github.com/vercel/mcp-server

## Author

Vercel

## Version

1.0.0
