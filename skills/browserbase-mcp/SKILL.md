---
name: browserbase-mcp
description: Browserbase cloud browser automation
---

# browserbase-mcp

Browserbase cloud browser automation

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-browserbase
```

### Step 2: Get API Credentials

Get your credentials from: https://www.browserbase.com/settings

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "browserbase": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-browserbase"],
      "env": {
            "BROWSERBASE_API_KEY": "your-api-key"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available browserbase commands"
```

---

## Environment Variables

- `BROWSERBASE_API_KEY`: Required - Your api-key

## Available Tools

- `create_session`
- `navigate`
- `click`
- `screenshot`

## Quick Start Examples

### Example 1
```
User: "Help me with browserbase"
```

## Documentation

See @anthropic/mcp-browserbase documentation for more details.



## Author

Browserbase

## Version

1.0.0
