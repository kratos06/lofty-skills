---
name: npm-mcp
description: NPM package management and registry
---

# npm-mcp

NPM package management and registry

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "npm-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-npm"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add npm-mcp
```

## Quick Start

After configuration, the npm-mcp tools will be available in Claude Code.

## Features

- npm
- packages
- nodejs





## Author

npm

## Version

1.0.0
