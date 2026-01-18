---
name: tavily-mcp
description: Tavily AI search for LLMs
---

# tavily-mcp

Tavily AI search for LLMs

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "tavily-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-tavily"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add tavily-mcp
```

## Quick Start

After configuration, the tavily-mcp tools will be available in Claude Code.

## Features

- tavily
- search
- ai





## Author

tavily

## Version

1.0.0
