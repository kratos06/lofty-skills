---
name: puppeteer-mcp
description: Puppeteer headless browser control
---

# puppeteer-mcp

Puppeteer headless browser control

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "puppeteer-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-puppeteer"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add puppeteer-mcp
```

## Quick Start

After configuration, the puppeteer-mcp tools will be available in Claude Code.

## Features

- puppeteer
- browser
- scraping



## Source

GitHub: https://github.com/nicholasbrooks/puppeteer-mcp

## Author

nicholasbrooks

## Version

1.0.0
