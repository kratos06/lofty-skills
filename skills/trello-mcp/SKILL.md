---
name: trello-mcp
description: Trello boards, lists, and cards management
---

# trello-mcp

Trello boards, lists, and cards management

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "trello-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-trello"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add trello-mcp
```

## Quick Start

After configuration, the trello-mcp tools will be available in Claude Code.

## Features

- trello
- kanban
- boards





## Author

atlassian

## Version

1.0.0
