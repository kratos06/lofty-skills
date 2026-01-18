---
name: 1password-mcp
description: 1Password password management
---

# 1password-mcp

1Password password management

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "1password-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-1password"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add 1password-mcp
```

## Quick Start

After configuration, the 1password-mcp tools will be available in Claude Code.

## Features

- 1password
- passwords
- security





## Author

1password

## Version

1.0.0
