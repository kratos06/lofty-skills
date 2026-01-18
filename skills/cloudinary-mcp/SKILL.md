---
name: cloudinary-mcp
description: Cloudinary media management
---

# cloudinary-mcp

Cloudinary media management

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "cloudinary-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-cloudinary"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add cloudinary-mcp
```

## Quick Start

After configuration, the cloudinary-mcp tools will be available in Claude Code.

## Features

- cloudinary
- media
- images





## Author

cloudinary

## Version

1.0.0
