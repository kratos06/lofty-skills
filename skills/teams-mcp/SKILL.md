---
name: teams-mcp
description: Microsoft Teams messaging and meetings
---

# teams-mcp

Microsoft Teams messaging and meetings

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "teams-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-teams"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add teams-mcp
```

## Quick Start

After configuration, the teams-mcp tools will be available in Claude Code.

## Features

- teams
- microsoft
- meetings





## Author

microsoft

## Version

1.0.0
