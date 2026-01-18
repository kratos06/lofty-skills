---
name: wolfram-mcp
description: Wolfram Alpha computational knowledge
---

# wolfram-mcp

Wolfram Alpha computational knowledge

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "wolfram-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-wolfram"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add wolfram-mcp
```

## Quick Start

After configuration, the wolfram-mcp tools will be available in Claude Code.

## Features

- wolfram
- computation
- math





## Author

wolfram

## Version

1.0.0
