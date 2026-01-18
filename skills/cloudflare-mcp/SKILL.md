---
name: cloudflare-mcp
description: Cloudflare Workers, KV, R2, and D1 management
---

# cloudflare-mcp

Cloudflare Workers, KV, R2, and D1 management

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "cloudflare-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-cloudflare"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add cloudflare-mcp
```

## Quick Start

After configuration, the cloudflare-mcp tools will be available in Claude Code.

## Features

- cloudflare
- workers
- edge



## Source

GitHub: https://github.com/cloudflare/mcp-server

## Author

Cloudflare

## Version

1.0.0
