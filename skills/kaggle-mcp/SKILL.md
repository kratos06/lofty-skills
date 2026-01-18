---
name: kaggle-mcp
description: Kaggle datasets, models, competitions, and notebooks
---

# kaggle-mcp

Kaggle datasets, models, competitions, and notebooks

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "kaggle-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-kaggle"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add kaggle-mcp
```

## Quick Start

After configuration, the kaggle-mcp tools will be available in Claude Code.

## Features

- kaggle
- datasets
- ml



## Source

GitHub: https://github.com/kaggle/mcp-server

## Author

Kaggle

## Version

1.0.0
