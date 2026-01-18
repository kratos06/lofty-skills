---
name: exa-mcp
description: Exa AI-powered search engine
---

# exa-mcp

Exa AI-powered search engine

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "exa-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-exa"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add exa-mcp
```

## Quick Start

After configuration, the exa-mcp tools will be available in Claude Code.

## Features

- exa
- search
- ai





## Author

Exa

## Version

1.0.0
