---
name: firebase-mcp
description: Firebase platform integration
---

# firebase-mcp

Firebase platform integration

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "firebase-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-firebase"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add firebase-mcp
```

## Quick Start

After configuration, the firebase-mcp tools will be available in Claude Code.

## Features

- firebase
- google
- backend





## Author

google

## Version

1.0.0
