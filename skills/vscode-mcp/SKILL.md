---
name: vscode-mcp
description: VS Code editor integration and extensions
---

# vscode-mcp

VS Code editor integration and extensions

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "vscode-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-vscode"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add vscode-mcp
```

## Quick Start

After configuration, the vscode-mcp tools will be available in Claude Code.

## Features

- vscode
- editor
- ide





## Author

microsoft

## Version

1.0.0
