---
name: linear-mcp
description: Linear issue tracking with cycles, projects, and high-velocity workflows
---

# linear-mcp

Linear issue tracking with cycles, projects, and high-velocity workflows

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "linear-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-linear"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add linear-mcp
```

## Quick Start

After configuration, the linear-mcp tools will be available in Claude Code.

## Features

- linear
- issues
- agile



## Source

GitHub: https://github.com/linear/mcp-server

## Author

Linear

## Version

1.0.0
