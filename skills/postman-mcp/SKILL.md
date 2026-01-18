---
name: postman-mcp
description: Postman API testing and collection management
---

# postman-mcp

Postman API testing and collection management

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "postman-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-postman"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add postman-mcp
```

## Quick Start

After configuration, the postman-mcp tools will be available in Claude Code.

## Features

- postman
- api
- testing





## Author

postman

## Version

1.0.0
