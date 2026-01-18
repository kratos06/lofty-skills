---
name: figma-mcp
description: Figma Dev Mode integration for design-to-code workflows
---

# figma-mcp

Figma Dev Mode integration for design-to-code workflows

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "figma-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-figma"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add figma-mcp
```

## Quick Start

After configuration, the figma-mcp tools will be available in Claude Code.

## Features

- figma
- design
- ui



## Source

GitHub: https://github.com/figma/mcp-server

## Author

Figma

## Version

1.0.0
