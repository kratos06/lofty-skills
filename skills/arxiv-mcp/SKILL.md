---
name: arxiv-mcp
description: arXiv academic papers search
---

# arxiv-mcp

arXiv academic papers search

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "arxiv-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-arxiv"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add arxiv-mcp
```

## Quick Start

After configuration, the arxiv-mcp tools will be available in Claude Code.

## Features

- arxiv
- papers
- research





## Author

arxiv

## Version

1.0.0
