---
name: firecrawl-mcp
description: Firecrawl web scraping and search capabilities (Official)
---

# firecrawl-mcp

Firecrawl web scraping and search capabilities (Official)

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "firecrawl-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-firecrawl"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add firecrawl-mcp
```

## Quick Start

After configuration, the firecrawl-mcp tools will be available in Claude Code.

## Features

- firecrawl
- scraping
- web



## Source

GitHub: https://github.com/firecrawl/mcp-server

## Author

Firecrawl

## Version

1.0.0
