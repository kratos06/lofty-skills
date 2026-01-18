---
name: gcp-mcp
description: Google Cloud Platform integration for compute, storage, and AI services
---

# gcp-mcp

Google Cloud Platform integration for compute, storage, and AI services

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "gcp-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-gcp"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add gcp-mcp
```

## Quick Start

After configuration, the gcp-mcp tools will be available in Claude Code.

## Features

- gcp
- google
- cloud



## Source

GitHub: https://github.com/google/gcp-mcp

## Author

Google

## Version

1.0.0
