---
name: playwright-mcp
description: Microsoft Playwright browser automation for testing and scraping (Official)
---

# playwright-mcp

Microsoft Playwright browser automation for testing and scraping (Official)

## Installation

### Option 1: Add to Claude Settings

Add to your Claude Code settings (settings.json or via `claude mcp add`):

```json
{
  "mcpServers": {
    "playwright-mcp": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-playwright"]
    }
  }
}
```

### Option 2: Install as Skill

```bash
claude skill add playwright-mcp
```

## Quick Start

After configuration, the playwright-mcp tools will be available in Claude Code.

## Features

- playwright
- browser
- testing
- automation



## Source

GitHub: https://github.com/microsoft/playwright-mcp

## Author

Microsoft

## Version

1.0.0
