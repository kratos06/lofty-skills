---
name: wolfram-mcp
description: Wolfram Alpha computational knowledge
---

# wolfram-mcp

Wolfram Alpha computational knowledge

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-wolfram
```

### Step 2: Get API Credentials

Get your credentials from: https://developer.wolframalpha.com/portal/myapps/

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "wolfram": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-wolfram"],
      "env": {
            "WOLFRAM_APP_ID": "your-app-id"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available wolfram commands"
```

---

## Environment Variables

- `WOLFRAM_APP_ID`: Required - Your app-id

## Available Tools

- `query`
- `simple_query`

## Quick Start Examples

### Example 1
```
User: "Help me with wolfram"
```

## Documentation

See @anthropic/mcp-wolfram documentation for more details.



## Author

wolfram

## Version

1.0.0
