---
name: e2b-mcp
description: E2B code sandbox execution
---

# e2b-mcp

E2B code sandbox execution

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "e2b-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-e2b"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add e2b-mcp
```

## Quick Start

After configuration, the e2b-mcp tools will be available in Claude Code.

## Features

- e2b
- sandbox
- code





## Author

E2B

## Version

1.0.0
