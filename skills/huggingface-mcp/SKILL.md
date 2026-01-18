---
name: huggingface-mcp
description: Hugging Face models, datasets, and inference API
---

# huggingface-mcp

Hugging Face models, datasets, and inference API

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "huggingface-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-huggingface"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add huggingface-mcp
```

## Quick Start

After configuration, the huggingface-mcp tools will be available in Claude Code.

## Features

- huggingface
- ml
- models



## Source

GitHub: https://github.com/huggingface/mcp-server

## Author

Hugging Face

## Version

1.0.0
