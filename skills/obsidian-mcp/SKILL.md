---
name: obsidian-mcp
description: Obsidian notes and knowledge base
---

# obsidian-mcp

Obsidian notes and knowledge base

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "obsidian-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-obsidian"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add obsidian-mcp
```

## Quick Start

After configuration, the obsidian-mcp tools will be available in Claude Code.

## Features

- obsidian
- notes
- markdown





## Author

obsidian

## Version

1.0.0
