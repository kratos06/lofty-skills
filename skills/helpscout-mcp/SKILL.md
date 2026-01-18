---
name: helpscout-mcp
description: Help Scout email support and customer communication
---

# helpscout-mcp

Help Scout email support and customer communication

## Prerequisites

### Step 1: Install MCP Server

```bash
npm install -g @anthropic/mcp-helpscout
```

### Step 2: Get API Credentials

Get your credentials from: https://secure.helpscout.net/settings/api/

### Step 3: Configure Claude Code

Add to your Claude settings file (`~/.claude/settings.json` or project `.claude/settings.local.json`):

```json
{
  "mcpServers": {
    "helpscout": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-helpscout"],
      "env": {
            "HELPSCOUT_API_KEY": "your-api-key"
      }
    }
  }
}
```

### Step 4: Verify Installation

Restart Claude Code and test:
```
User: "List available helpscout commands"
```

---

## Environment Variables

- `HELPSCOUT_API_KEY`: Required - Your api-key

## Available Tools

- `list_conversations`
- `get_conversation`
- `create_conversation`

## Quick Start Examples

### Example 1
```
User: "Help me with helpscout"
```

## Documentation

See @anthropic/mcp-helpscout documentation for more details.

## Source

GitHub: https://github.com/helpscout/mcp-server

## Author

Help Scout

## Version

1.0.0
