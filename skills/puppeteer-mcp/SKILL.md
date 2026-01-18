---
name: puppeteer-mcp
description: Puppeteer headless browser control
---

# puppeteer-mcp

Puppeteer headless browser control

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-puppeteer
```

### Step 2: Get API Credentials

Configure the required credentials below.

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "puppeteer": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-puppeteer"],
      "env": {}
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available puppeteer commands"
```

---

## Environment Variables



## Available Tools

- `navigate`
- `click`
- `type`
- `screenshot`
- `evaluate`

## Quick Start Examples

### Example 1
```
User: "Help me with puppeteer"
```

## Documentation

See @anthropic/mcp-puppeteer documentation for more details.

## Source

GitHub: https://github.com/nicholasbrooks/puppeteer-mcp

## Author

nicholasbrooks

## Version

1.0.0
