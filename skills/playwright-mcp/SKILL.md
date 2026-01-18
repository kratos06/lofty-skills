---
name: playwright-mcp
description: Microsoft Playwright browser automation for testing and scraping (Official)
---

# playwright-mcp

Microsoft Playwright browser automation for testing and scraping (Official)

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-playwright
```

### Step 2: Get API Credentials

Configure the required credentials below.

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "playwright": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-playwright"],
      "env": {}
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available playwright commands"
```

---

## Environment Variables



## Available Tools

- `navigate`
- `click`
- `fill`
- `screenshot`
- `evaluate`

## Quick Start Examples

### Example 1
```
User: "Help me with playwright"
```

## Documentation

See @anthropic/mcp-playwright documentation for more details.

## Source

GitHub: https://github.com/microsoft/playwright-mcp

## Author

Microsoft

## Version

1.0.0
