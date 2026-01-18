---
name: screenshot-mcp
description: Website screenshot capture
---

# screenshot-mcp

Website screenshot capture

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-screenshot
```

### Step 2: Get API Credentials

Configure the required credentials below.

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "screenshot": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-screenshot"],
      "env": {}
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available screenshot commands"
```

---

## Environment Variables



## Available Tools

- `capture_url`
- `capture_element`
- `capture_fullpage`

## Quick Start Examples

### Example 1
```
User: "Help me with screenshot"
```

## Documentation

See @anthropic/mcp-screenshot documentation for more details.



## Author

community

## Version

1.0.0
